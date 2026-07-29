---
title: "Week 6 Worklog"
date: 2026-07-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# 6. Đóng gói Docker & Cài đặt máy chủ EC2

### Mục tiêu trong tuần:

* Đóng gói Backend bằng Docker sử dụng kiến trúc multi-stage chạy bằng user giới hạn.
* Khởi chạy máy chủ EC2, tạo S3 buckets và kho chứa ECR.
* Thiết lập IAM Role kết nối an toàn không sử dụng khóa bảo mật tĩnh.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Viết Dockerfile multi-stage tối ưu phân tầng cho backend Node.js. | 20/07/2026 | 20/07/2026 |
| 2 | Cấu hình non-root user và test chạy container cục bộ. | 21/07/2026 | 21/07/2026 |
| 3 | Tạo S3 buckets cho Frontend static hosting và kho ECR. | 22/07/2026 | 22/07/2026 |
| 4 | Khởi chạy máy chủ EC2 và cài đặt công cụ Docker. | 23/07/2026 | 23/07/2026 |
| 5 | Thiết lập IAM Role gán vào EC2 và test chạy container thủ công trên server. | 24/07/2026 | 24/07/2026 |

### Các kết quả đạt được:

* Viết thành công Dockerfile tối ưu phân tầng chạy dưới quyền user giới hạn.
* Khởi chạy máy chủ EC2, cài đặt Docker và cấu hình ECR registry.
* Gắn IAM Instance Profile `learnsphere-ec2-role` cho EC2 để xác thực S3/Bedrock không dùng key.
