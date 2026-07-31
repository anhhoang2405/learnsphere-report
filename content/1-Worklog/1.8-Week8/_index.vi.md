---
title: "Worklog Tuần 8"
date: 2026-07-20
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

# 8. Thiết lập Giám sát CloudWatch Logs & Cảnh báo Amazon SNS

### Mục tiêu trong tuần:

* Cấu hình đẩy log container tập trung về AWS CloudWatch phục vụ truy vết.
* Thiết lập cảnh báo tự động khi máy chủ gặp sự cố hoặc quá tải tài nguyên.
* Tối ưu hóa các chính sách vòng đời lưu trữ trên S3 Media Bucket.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Cấu hình Docker log driver trên EC2 để tự động đẩy nhật ký hoạt động của Backend về CloudWatch Logs. | 20/07/2026 | 20/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html |
| **Thứ 3** | - Thiết lập CloudWatch Alarms theo dõi chỉ số sử dụng CPU (`CPUUtilization`) và sự cố máy chủ (`StatusCheckFailed`). | 21/07/2026 | 22/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| **Thứ 5** | - Khởi tạo Amazon SNS Topic và thêm địa chỉ email của quản trị viên để tự động nhận thông báo cảnh báo. | 24/07/2026 | 24/07/2026 | https://docs.aws.amazon.com/sns/latest/dg/welcome.html |
| **Thứ 6** | - Thiết lập S3 Lifecycle Policies tự động chuyển các file media cũ sang lớp lưu trữ giá rẻ hoặc xóa tệp rác sau 30 ngày. | 24/07/2026 | 24/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html |

### Kết quả đạt được tuần 8:

* Log ứng dụng backend được lưu trữ tập trung trên CloudWatch, dễ dàng debug.
* Hệ thống cảnh báo tự động qua Email hoạt động tốt khi giả lập sự cố EC2.
* Tối ưu hóa dung lượng lưu trữ trên S3 và kiểm soát chi phí hiệu quả.
