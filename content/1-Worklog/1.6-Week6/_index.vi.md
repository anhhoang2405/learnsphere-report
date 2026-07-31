---
title: "Week 6 Worklog"
date: 2026-07-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# 6. Đóng gói Docker, ECR & Cài đặt máy chủ EC2

### Mục tiêu trong tuần:

* Đóng gói mã nguồn Backend bằng Dockerfile phân tầng (Multi-stage) để tối ưu hóa kích thước và bảo mật.
* Tạo AWS ECR, khởi dựng máy chủ EC2, cấu hình bộ nhớ ảo Swap và thiết lập phân quyền IAM Instance Profile.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Viết Dockerfile tối ưu hóa phân tầng sử dụng base image `node:24-alpine`, cấu hình chạy container dưới quyền user non-root. | 20/07/2026 | 20/07/2026 |
| 2 | Khởi tạo Amazon ECR repository để lưu trữ các bản build Docker image của backend. | 21/07/2026 | 21/07/2026 |
| 3 | Launch máy chủ EC2 (`t3.small`) trên AWS, cài đặt Docker và cấu hình 2GB Swap đề phòng tràn RAM khi chạy container. | 22/07/2026 | 22/07/2026 |
| 4 | Cấu hình Security Group cho EC2: khóa chặt cổng SSH 22, chỉ cho phép nhận các kết nối web an toàn. | 23/07/2026 | 23/07/2026 |
| 5 | Tạo và gán IAM Role cho EC2 (`learnsphere-ec2-role`) giúp máy chủ tự cấp quyền pull image ECR và đẩy log về CloudWatch. | 24/07/2026 | 24/07/2026 |

### Các kết quả đạt được:

* Đóng gói Backend thành công với Docker image dung lượng nhỏ và chạy dưới quyền non-root bảo mật.
* Hoàn thiện môi trường hạ tầng máy chủ EC2, sẵn sàng chạy container và liên kết với CloudWatch Logs.
