---
title: "Week 7 Worklog"
date: 2026-07-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# 7. Triển khai Frontend S3/CloudFront & Nghiệm thu Hệ thống (Hạn chót 31/07)

### Mục tiêu trong tuần:

* Triển khai hoàn tất giao diện React Frontend lên S3 Website Hosting và bảo mật HTTPS qua CloudFront CDN.
* Ánh xạ tên miền riêng và phối hợp kiểm thử tự động hóa quy trình CI/CD từ GitHub Actions.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Thực hiện build bản chính thức Frontend và đồng bộ hóa các tệp tin lên S3 Frontend Bucket. | 27/07/2026 | 27/07/2026 |
| 2 | Thiết lập CloudFront CDN, cấu hình Custom Error Pages (định tuyến lỗi 404 về `/index.html`) hỗ trợ React Router. | 28/07/2026 | 28/07/2026 |
| 3 | Trỏ tên miền phụ CNAME `www` trên Tenten.vn về tên miền phân phối của CloudFront. | 29/07/2026 | 29/07/2026 |
| 4 | Phối hợp với Nguyễn Hồng Sơn cấu hình GitHub Secrets và chạy thử nghiệm quy trình tự động deploy Frontend/Backend. | 30/07/2026 | 30/07/2026 |
| 5 | Kiểm thử bảo mật toàn diện trên cổng HTTPS thực tế, hoàn thiện tài liệu báo cáo thực tập. | 31/07/2026 | 31/07/2026 |

### Các kết quả đạt được:

* Giao diện tĩnh Frontend được triển khai thành công tại tên miền riêng bảo mật: **`https://www.learnsphere.id.vn`**.
* Quy trình CI/CD tích hợp mượt mà (tự động đồng bộ file tĩnh lên S3 và xóa cache CloudFront `/*` khi có code mới).
* Nghiệm thu toàn diện hệ thống LearnSphere và nộp báo cáo đúng hạn chót 31/07.
