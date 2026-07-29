---
title: "Worklog"
date: 2026-07-25
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

# Nhật ký Thực tập Tổng quan

Phần này ghi lại nhật ký công việc hàng tuần của sinh viên **Nguyễn Hoàng Anh** trong chương trình thực tập **First Cloud AI Journey (FCAJ)**.

Kỳ thực tập chính thức kéo dài từ ngày **15/06/2026 đến ngày 14/08/2026**, trong đó thời gian tập trung phát triển đồ án **LearnSphere** diễn ra trong 7 tuần (hoàn thành ngày **31/07/2026**). Báo cáo ghi nhận quá trình nghiên cứu các dịch vụ AWS, phát triển mã nguồn, đóng gói container Docker, triển khai bảo mật EC2, lưu trữ tĩnh S3/CloudFront và cấu hình CI/CD tự động.

#### Tóm tắt tiến trình 7 tuần thực tập

1. **[Tuần 1: Giới thiệu & Cơ bản về AWS](1.1-week1/)** - Nhập học bootcamp, làm quen AWS CLI và khởi tạo tài khoản.
2. **[Tuần 2: Kiến trúc Backend & Thiết lập Database](1.2-week2/)** - Phát triển các routes API Express và liên kết MongoDB Atlas.
3. **[Tuần 3: Tích hợp lưu trữ S3](1.3-week3/)** - Lập trình upload file qua cơ chế chữ ký bảo mật S3 Presigned URL.
4. **[Tuần 4: Phát triển giao diện Frontend](1.4-week4/)** - Khởi tạo dự án Vite React, lập trình trang học sinh và giáo viên.
5. **[Tuần 5: Tích hợp dịch vụ AI cốt lõi & Test liên kết](1.5-week5/)** - Tích hợp APIs của Groq và AWS Bedrock Converse, gỡ lỗi CORS kết nối và test hệ thống local.
6. **[Tuần 6: Đóng gói Docker & Cài đặt máy chủ EC2](1.6-week6/)** - Đóng gói dự án Backend bằng Dockerfile phân tầng, tạo ECR, cài đặt Docker trên EC2 và gán IAM Role bảo mật.
7. **[Tuần 7: Cân bằng tải ALB, CloudFront & Tự động hóa CI/CD (Hạn chót 31/07)](1.7-week7/)** - Đăng ký chứng chỉ ACM SSL, cấu hình ALB nghe cổng 443, CloudFront CDN cho Frontend, trỏ tên miền phụ Tenten, viết pipeline deploy.yml tự động và nghiệm thu hoàn thành dự án.