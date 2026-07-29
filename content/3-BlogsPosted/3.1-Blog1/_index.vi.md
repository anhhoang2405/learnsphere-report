---
title: "Blog 1"
date: 2026-07-26
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Triển khai Docker Container Backend lên AWS EC2 an toàn với IAM Instance Profile

#### 1. Giới thiệu
Khi đưa một ứng dụng web full-stack lên môi trường cloud như AWS, việc tối ưu hóa hiệu năng và bảo mật hệ thống Backend luôn là ưu tiên hàng đầu. Trong bài viết này, mình sẽ chia sẻ trải nghiệm thực tế khi đóng gói ứng dụng Node.js/Express của dự án **LearnSphere** bằng Docker và triển khai nó lên máy chủ EC2 mà không cần lưu khóa bảo mật tĩnh (Keyless Security).

![Triển khai Docker EC2](/images/3-BlogsPosted/blog1.png)

---

#### 2. Tại sao nên chọn Container hóa?
Trong quá trình code, chắc chắn ai cũng từng gặp lỗi "chạy được trên máy tôi nhưng lỗi trên server". Sự lệch pha về phiên bản Node.js, thư viện phụ thuộc (dependencies) hay hệ điều hành có thể khiến backend bị crash khi deploy lên EC2.

Bằng cách đóng gói mã nguồn vào Docker container, toàn bộ code và môi trường chạy sẽ được đóng gói thành một "ảnh" (Image) duy nhất, đảm bảo tính nhất quán tuyệt đối khi chạy thử nghiệm local cũng như khi đưa lên máy chủ thật của AWS.

---

#### 3. Viết Dockerfile tối ưu
Đối với môi trường chạy thực tế, tối ưu dung lượng và bảo mật là yếu tố sống còn. Chúng ta sử dụng mô hình **multi-stage build** để lọc bỏ file rác, chỉ giữ lại code chạy và thư viện chạy thực tế. Đồng thời, cấu hình chạy dưới quyền **user hạn chế (non-root)** để bảo vệ máy chủ EC2.

```dockerfile
# Stage 1: Cài đặt thư viện production
FROM node:20-alpine AS base
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production

# Stage 2: Sao chép mã nguồn & Khởi chạy
COPY src/ ./src/

# Thực hành bảo mật: chạy bằng tài khoản giới hạn
RUN addgroup -g 1001 -S nodejs && \
    adduser -S nodejs -u 1001
USER nodejs

EXPOSE 5000
ENV NODE_ENV=production

CMD ["node", "src/server.js"]
```

---

#### 4. Sức mạnh của AWS IAM Role cho EC2
Một trong những sai lầm bảo mật kinh điển của sinh viên khi làm đồ án là lưu các khóa AWS Access Key (`AWS_ACCESS_KEY_ID` và `AWS_SECRET_ACCESS_KEY`) trực tiếp trong file cấu hình `.env` trên EC2. Nếu máy chủ bị tấn công hoặc lỡ tay commit file `.env` lên GitHub, toàn bộ tài khoản AWS của bạn sẽ bị hack.

**Giải pháp**: Sử dụng **IAM Instance Profile** gắn trực tiếp cho EC2.
1. Tạo một IAM Role có liên kết tin cậy với dịch vụ EC2 (`ec2.amazonaws.com`).
2. Cấp các quyền truy cập cần thiết như ghi file vào S3 (`AmazonS3FullAccess`) và gọi AI Bedrock (`AmazonBedrockFullAccess`).
3. Gắn Role này cho máy chủ EC2 của bạn.
4. AWS SDK chạy trong code Backend sẽ tự động lấy các thông tin xác thực tạm thời từ hệ thống AWS mà không cần khai báo khóa tĩnh nào trong file `.env` của máy chủ.

---

#### 5. Kết luận
Sự kết hợp giữa **Docker** và **AWS IAM Role** đem lại một mô hình vận hành vô cùng sạch sẽ, an toàn và dễ di chuyển. Dự án hoạt động độc lập hoàn toàn với hệ điều hành của EC2 và các kết nối tới tài nguyên AWS được xác thực tự động dưới quyền bảo mật cao nhất của Amazon.

---

### Minh chứng chia sẻ Cộng đồng (Bài đăng Facebook)
Dưới đây là hình ảnh minh chứng bài viết kỹ thuật đã được chia sẻ công khai tại nhóm cộng đồng Facebook AWS Study Group:

![Minh chứng bài đăng Facebook](/images/3-BlogsPosted/fb_post1.png)