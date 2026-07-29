---
title: "Blog 3"
date: 2026-07-26
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Tự động hóa CI/CD với GitHub Actions: Từ Commit đến Production chỉ trong 3 phút

#### 1. Giới thiệu
Trong một đội ngũ phát triển phần mềm hiện đại, tốc độ và độ tin cậy là chìa khóa thành công. Việc chạy lệnh build cục bộ, kéo thả file tĩnh thủ công lên S3, rồi kết nối SSH vào EC2 để gõ lệnh khởi động lại Docker mỗi khi có một thay đổi nhỏ về giao diện là cực kỳ kém hiệu quả và dễ gây lỗi. Trong bài viết này, mình sẽ chia sẻ cách chúng mình tự động hóa toàn bộ quy trình này bằng **CI/CD Pipeline với GitHub Actions** cho dự án **LearnSphere**.

![Quy trình tự động hóa CI/CD](/images/3-BlogsPosted/blog3.png)

---

#### 2. Kiến trúc Quy trình CI/CD
Chúng mình xây dựng một **quy trình tách biệt (decoupled workflow)** được kích hoạt hoàn toàn tự động mỗi khi có một commit mới được push hoặc merge vào nhánh chính `main` trên GitHub. Quy trình được phân làm 2 nhánh chạy song song:

1. **Triển khai Backend (deploy-backend)**:
   - Tải mã nguồn về máy chạy của GitHub.
   - Đăng nhập bảo mật vào kho Amazon ECR.
   - Biên dịch và đóng gói Docker image với thẻ định danh (tag) theo mã commit (SHA) và tag `latest`.
   - Đẩy (push) ảnh container lên Amazon ECR.
   - Kết nối SSH vào EC2, kéo ảnh mới về, tắt container cũ và bật container mới nạp file môi trường của server.
2. **Triển khai Frontend (deploy-frontend)**:
   - Cài đặt thư viện dependencies và biên dịch ứng dụng React bằng Vite Compiler.
   - Kết nối và đồng bộ (sync) các tệp tĩnh đã build lên Amazon S3 bucket.
   - Gọi API xóa bộ nhớ đệm (Invalidate cache) của CloudFront CDN để người dùng nhận được giao diện mới lập tức.

---

#### 3. Thực hành Bảo mật: Chính sách Phân quyền Tối thiểu
Một trong những nguy cơ bảo mật lớn nhất khi dùng CI/CD là phân quyền. Việc cấp thẳng quyền quản trị cao nhất (`AdministratorAccess`) cho tài khoản chạy GitHub Actions là vô cùng nguy hiểm. Nếu kho chứa GitHub của bạn bị hack, kẻ tấn công sẽ có quyền xóa sạch mọi tài nguyên trên tài khoản AWS của bạn.

Để giải quyết vấn đề này, chúng mình tự thiết kế một **Custom IAM Policy** giới hạn quyền tối đa cho GitHub Actions:
* Chỉ cho phép đọc/ghi vào đúng duy nhất S3 bucket tĩnh của Frontend.
* Chỉ cho phép đẩy ảnh Docker lên đúng kho lưu trữ ECR `learnsphere-be`.
* Chỉ cho phép thực hiện lệnh xóa cache trên đúng ID phân phối CloudFront của dự án.

---

#### 4. Kích hoạt thông qua GitHub Secrets
Tất cả các thông số nhạy cảm như AWS Access Key, địa chỉ IP của EC2, và khóa bảo mật SSH `.pem` đều không được viết trong file code. Chúng được lưu trữ trong mục **GitHub Secrets** của kho chứa mã nguồn. Khi quy trình chạy, GitHub sẽ tự động nạp các biến này một cách mã hóa và an toàn tuyệt đối.

---

#### 5. Kết luận
Với việc triển khai thành công quy trình CI/CD tự động, đội ngũ của chúng mình đã đạt được quy trình phát triển **không thời gian chết (zero-downtime)**. Các lập trình viên giờ đây không cần truy cập trực tiếp vào AWS console hay máy chủ EC2 nữa. Họ chỉ cần tập trung viết code, push lên Git và theo dõi thay đổi tự động hiển thị trên môi trường thực tế chỉ sau chưa đầy 3 phút!

---

### Minh chứng chia sẻ Cộng đồng (Bài đăng Facebook)
Dưới đây là hình ảnh minh chứng bài viết kỹ thuật đã được chia sẻ công khai tại nhóm cộng đồng Facebook AWS Study Group:

![Minh chứng bài đăng Facebook](/images/3-BlogsPosted/fb_post3.png)