---
title: "Week 6 Worklog"
date: 2026-07-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# 6. Đóng gói mã nguồn & Phối hợp Thiết lập môi trường AWS

### Mục tiêu trong tuần:

* Đóng gói mã nguồn tĩnh Frontend (Vite build) và hỗ trợ viết Dockerfile tối ưu phân tầng cho Backend.
* Phối hợp thiết lập hạ tầng AWS (S3, ECR, EC2, IAM Role) an toàn bảo mật.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Thử nghiệm biên dịch tĩnh mã nguồn Frontend (React build) bằng trình biên dịch Vite. | 20/07/2026 | 20/07/2026 |
| 2 | Viết file cấu hình `.dockerignore` và hỗ trợ Nguyễn Hồng Sơn kiểm thử giảm kích thước file build Docker. | 21/07/2026 | 21/07/2026 |
| 3 | Khởi tạo AWS S3 Bucket `learnsphere-fe-static` phục vụ lưu trữ giao diện tĩnh Frontend. | 22/07/2026 | 22/07/2026 |
| 4 | Phối hợp cấu hình Security Group cho EC2, mở cổng 80, 443 và giới hạn cổng 5000 cục bộ. | 23/07/2026 | 23/07/2026 |
| 5 | Thiết kế các chính sách phân quyền (Policy) của IAM Role gán cho EC2 (`learnsphere-ec2-role`). | 24/07/2026 | 24/07/2026 |

### Các kết quả đạt được:

* Giao diện tĩnh Frontend được tối ưu hóa dung lượng (dưới 5MB) giúp tải trang nhanh chóng.
* Thiết lập thành công S3 Frontend Bucket, cấu hình phân quyền Security Group cho EC2 bảo mật.
* Hoàn thiện thiết kế IAM Instance Profile cho phép EC2 tương tác an toàn không dùng AWS access key tĩnh.
