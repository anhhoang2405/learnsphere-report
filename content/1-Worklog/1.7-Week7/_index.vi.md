---
title: "Week 7 Worklog"
date: 2026-07-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# 7. Cân bằng tải ALB, CloudFront & Tự động hóa CI/CD

### Mục tiêu trong tuần:

* Cấu hình CloudFront CDN cho Frontend và định tuyến Application Load Balancer (ALB) cho EC2 Backend dưới giao thức bảo mật HTTPS.
* Thiết lập tự động hóa quy trình CI/CD qua GitHub Actions (OIDC) và chạy nghiệm thu sản phẩm thực tế.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Nhận bản build Frontend tĩnh từ Sơn, tải lên S3 và cấu hình CloudFront CDN kết hợp OAC để bảo mật truy cập S3. | 27/07/2026 | 27/07/2026 |
| 2 | Đăng ký SSL trên ACM cho tên miền `learnspherev2.id.vn`, dựng ALB nghe cổng 443 và chuyển tiếp traffic tới cổng 5000 của EC2. | 28/07/2026 | 28/07/2026 |
| 3 | Cấu hình bản ghi CNAME trên Tenten: trỏ `www` về CloudFront CDN, và `api` về ALB để giải quyết triệt để lỗi Mixed Content. | 29/07/2026 | 29/07/2026 |
| 4 | Viết và hoàn thiện file GitHub Actions workflow (`deploy.yml`), thiết lập OIDC xác thực an toàn không dùng access key tĩnh. | 30/07/2026 | 30/07/2026 |
| 5 | Chạy kiểm thử tự động hóa CI/CD (push code -> tự động deploy); cùng Sơn và Dũng nghiệm thu hệ thống thực tế và nộp báo cáo. | 31/07/2026 | 31/07/2026 |

### Các kết quả đạt được:

* Hệ thống LearnSphere được triển khai chạy thực tế bảo mật HTTPS hoàn toàn dưới tên miền `https://www.learnspherev2.id.vn`.
* Hoàn thiện pipeline CI/CD tự động hóa quy trình deploy Backend lên EC2 và Frontend lên S3 trong vòng chưa đầy 3 phút.
* Hoàn thành kỳ thực tập và bàn giao báo cáo nghiệm thu đúng thời hạn chót 31/07.
