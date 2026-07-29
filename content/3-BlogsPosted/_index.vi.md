---
title: "Các bài blog đã đăng"
date: 2026-07-26
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

# Các bài viết chia sẻ Kỹ thuật (Blogs)

Mục này thống kê các bài viết chia sẻ kinh nghiệm kỹ thuật thực hành được đăng tải lên cộng đồng tại [Nhóm Facebook AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj) trong thời gian thực tập. Các bài viết tập trung vào các chủ đề container hóa, bảo mật giao thức HTTPS và quy trình tự động hóa CI/CD:

---

### [Blog 1: Triển khai Docker Container Backend lên AWS EC2 an toàn với IAM Instance Profile](3.1-blog1/)
Bài viết hướng dẫn cách đóng gói ứng dụng Node.js/Express bằng Dockerfile phân tầng tối ưu dung lượng, cách chạy dưới quyền user giới hạn (non-root) và cơ chế kết nối an toàn không lưu khóa tĩnh (Keyless) sử dụng IAM Role gán cho EC2.

### [Blog 2: Giải quyết lỗi Mixed Content: Đồng bộ hóa HTTPS toàn phần với CloudFront & Application Load Balancer](3.2-blog2/)
Bài viết chia sẻ kinh nghiệm thực tế gỡ lỗi Mixed Content khi trình duyệt chặn các yêu cầu gửi dữ liệu từ trang HTTPS về HTTP. Bài viết hướng dẫn cấu hình AWS ACM SSL Certificate, thiết lập ALB cho Backend và CloudFront CDN cho Frontend.

### [Blog 3: Tự động hóa CI/CD với GitHub Actions: Từ Commit đến Production chỉ trong 3 phút](3.3-blog3/)
Bài viết giới thiệu chi tiết cách xây dựng luồng triển khai tự động hoàn toàn. Khi nhà phát triển push code, hệ thống tự động chạy tests, build và sync Frontend lên S3, build và push ảnh Docker lên ECR, SSH cập nhật máy chủ EC2 và xóa bộ nhớ đệm CloudFront.