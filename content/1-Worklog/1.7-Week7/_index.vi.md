---
title: "Worklog Tuần 7"
date: 2026-07-13
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# 7. Cấu hình Cân bằng tải ALB, CloudFront HTTPS & Domain

### Mục tiêu trong tuần:

* Đăng ký chứng chỉ SSL/TLS trên ACM và cấu hình HTTPS bảo mật.
* Thiết lập ALB làm cổng trung chuyển traffic an toàn cho Backend.
* Phân phối Frontend qua CloudFront CDN và trỏ tên miền chính thức.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Đăng ký chứng chỉ SSL/TLS miễn phí trên AWS Certificate Manager (ACM) cho tên miền `learnspherev2.id.vn`. | 13/07/2026 | 13/07/2026 | https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html |
| **Thứ 3** | - Khởi tạo Application Load Balancer (ALB) nằm ở phân vùng Public Subnet, trỏ listener HTTPS về EC2 Backend. | 14/07/2026 | 14/07/2026 | https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html |
| **Thứ 4** | - Nhận bản build tĩnh Frontend từ Sơn, đẩy lên S3 và tạo CloudFront Distribution phân phối qua HTTPS. | 15/07/2026 | 16/07/2026 | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html |
| **Thứ 5** | - Cấu hình DNS trên trang quản trị Tenten trỏ bản ghi `www` về CloudFront và `api` về ALB. | 16/07/2026 | 17/07/2026 | https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html |
| **Thứ 6** | - Xử lý triệt để lỗi Mixed Content khi giao tiếp HTTPS bằng cách đổi tất cả link API sang domain phụ `api.learnspherev2.id.vn`. | 17/07/2026 | 17/07/2026 | https://aws.amazon.com/security/ |

### Kết quả đạt được tuần 7:

* Mã hóa HTTPS thành công cho toàn bộ hệ thống web LearnSphere.
* Hệ thống định tuyến traffic an toàn từ ALB đến Backend chạy trong Private Subnet.
* Kết nối tên miền chính thức thành công, trang web hiển thị đúng giao diện và gọi API mượt mà.
