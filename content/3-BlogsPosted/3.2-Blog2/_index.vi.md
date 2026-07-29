---
title: "Blog 2"
date: 2026-07-26
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Giải quyết lỗi Mixed Content: Đồng bộ hóa HTTPS toàn phần với CloudFront & Application Load Balancer

#### 1. Giới thiệu
Khi triển khai một ứng dụng web thực tế lên cloud, một trong những tình huống gây ức chế nhất là hệ thống chạy local cực tốt bằng HTTP, nhưng ngay khi đưa lên mạng và cấu hình bảo mật, nút Đăng nhập lập tức bị liệt và trả về lỗi mạng bí ẩn `Failed to fetch`. Trong bài viết này, mình sẽ làm rõ nguyên lý lỗi **Mixed Content** và cách giải quyết triệt để sử dụng bộ đôi CloudFront, Application Load Balancer và chứng chỉ SSL ACM.

![Kiến trúc bảo mật HTTPS](/images/3-BlogsPosted/blog2.png)

---

#### 2. Lỗi "Mixed Content" là gì?
Các trình duyệt hiện đại áp dụng quy tắc bảo mật rất nghiêm ngặt. Nếu giao diện chính của trang web chạy trên giao thức mã hóa an toàn (**HTTPS**), trình duyệt sẽ chủ động chặn toàn bộ các yêu cầu gọi dữ liệu từ trang này tới các tài nguyên không bảo mật chạy trên giao thức thông thường (**HTTP**).

Ở giai đoạn đầu triển khai, Frontend React được phân phối bảo mật qua CloudFront bằng HTTPS. Tuy nhiên, Backend chạy trong EC2 vẫn gọi trực tiếp qua địa chỉ IP và giao thức HTTP thô (`http://18.143.151.54:5000`).
Khi người dùng nhập thông tin và nhấn Đăng nhập trên trang `https://www.learnsphere.id.vn`, trình duyệt sẽ chặn đứng yêu cầu gửi mật khẩu về cổng API `http://.../api/auth/login` để tránh bị đánh cắp dữ liệu, gây ra lỗi `Failed to fetch` trên màn hình.

---

#### 3. Khắc phục lỗi bằng AWS Application Load Balancer
Để trình duyệt chấp nhận kết nối, cả Frontend và Backend đều phải chạy trên HTTPS. Do địa chỉ IP thô không thể đăng ký chứng chỉ SSL, chúng ta bắt buộc phải sử dụng tên miền riêng và định tuyến dữ liệu qua bộ cân bằng tải.

Chúng ta dựng **Application Load Balancer (ALB)** đứng trước EC2 để làm nhiệm vụ giải mã bảo mật:
```
User (Browser) ───► HTTPS:443 ──► AWS ALB (Giải mã SSL) ──► HTTP:5000 ──► EC2 Backend
```
1. **Yêu cầu Chứng chỉ**: Sử dụng AWS Certificate Manager (ACM) đăng ký chứng chỉ SSL miễn phí cho tên miền riêng: `learnsphere.id.vn` và `*.learnsphere.id.vn` (tại vùng Singapore).
2. **Cấu hình Listener**: Thiết lập ALB lắng nghe cổng HTTPS 443, gắn chứng chỉ SSL ACM vừa tạo và chuyển tiếp dữ liệu về cổng 5000 của EC2.
3. **Trỏ DNS**: Tại trang Tenten.vn, tạo bản ghi CNAME trỏ tên miền phụ `api.learnsphere.id.vn` về địa chỉ DNS của ALB.

Nhờ đó, API Backend đã có đường dẫn bảo mật chính chủ: `https://api.learnsphere.id.vn/api/`!

---

#### 4. Đồng bộ HTTPS phía Frontend qua CloudFront
Ở phía Frontend, chúng ta cũng cần cấu hình tên miền riêng thay vì dùng link mặc định:
1. Đăng ký chứng chỉ SSL ACM cho tên miền `learnsphere.id.vn` tại vùng **N. Virginia (us-east-1)** (yêu cầu bắt buộc của CDN CloudFront).
2. Gắn tên miền phụ `www.learnsphere.id.vn` và chứng chỉ SSL Mỹ vừa tạo vào CloudFront Distribution.
3. Kích hoạt tính năng **Redirect HTTP to HTTPS** để tự động bảo vệ người truy cập.
4. Trỏ CNAME `www` trên Tenten về CloudFront.

---

#### 5. Kết luận
Khi cả Frontend (`https://www.learnsphere.id.vn`) và API Backend (`https://api.learnsphere.id.vn`) đều được đồng bộ hoạt động trên giao thức HTTPS bảo mật, lỗi Mixed Content sẽ được giải quyết triệt để. Mọi thông tin truyền tải qua lại trên hệ thống LearnSphere đều được mã hóa an toàn, nâng tầm chất lượng đồ án lên chuẩn môi trường thực tế.

---

### Minh chứng chia sẻ Cộng đồng (Bài đăng Facebook)
Dưới đây là hình ảnh minh chứng bài viết kỹ thuật đã được chia sẻ công khai tại nhóm cộng đồng Facebook AWS Study Group:

![Minh chứng bài đăng Facebook](/images/3-BlogsPosted/fb_post2.png)