---
title: "Week 7 Worklog"
date: 2026-07-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# 7. Cân bằng tải ALB, CloudFront & Tự động hóa CI/CD (Hạn chót 31/07)

### Mục tiêu trong tuần:

* Thiết lập Application Load Balancer và chứng chỉ ACM SSL cho Backend.
* Triển khai Frontend lên S3 website hosting, bảo mật HTTPS qua CloudFront CDN tên miền riêng.
* Lập trình quy trình CI/CD tự động qua GitHub Actions và nghiệm thu toàn hệ thống.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Đăng ký chứng chỉ ACM SSL và thiết lập bộ cân bằng tải ALB cổng 443. | 27/07/2026 | 27/07/2026 |
| 2 | Cấu hình CloudFront CDN phân phối S3 và trỏ các bản ghi CNAME trên Tenten.vn. | 28/07/2026 | 28/07/2026 |
| 3 | Lập trình file deploy.yml, cấu hình Secrets và kiểm thử tự động hóa CI/CD. | 29/07/2026 | 29/07/2026 |
| 4 | Sửa lỗi tham số Bedrock và lập trình cơ chế AI tự động đổi nhà cung cấp dự phòng. | 30/07/2026 | 30/07/2026 |
| 5 | Cấu hình rate limits, gắn Custom IAM Policy tối thiểu quyền và nộp bài báo cáo. | 31/07/2026 | 31/07/2026 |

### Các kết quả đạt được:

* Hoàn thành mã hóa HTTPS toàn phần cho tên miền Frontend và API Backend.
* Lập trình và kiểm thử cơ chế tự động chuyển vùng dự phòng AI (Groq ⇄ Bedrock) an toàn.
* Thiết lập thành công quy trình CI/CD tự động qua GitHub Actions sử dụng Custom IAM Policy.
* Nghiệm thu toàn diện hệ thống LearnSphere và hoàn thiện báo cáo đúng thời hạn chót 31/07.
