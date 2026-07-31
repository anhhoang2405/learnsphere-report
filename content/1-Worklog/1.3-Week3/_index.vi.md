---
title: "Worklog Tuần 3"
date: 2026-06-15
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# 3. Lưu trữ Amazon S3, CDN CloudFront & Đóng gói Docker

### Mục tiêu trong tuần:

* Tìm hiểu và cấu hình dịch vụ lưu trữ đối tượng Amazon S3 để lưu trữ media đồ án.
* Tích hợp CloudFront CDN phân phối tài nguyên tĩnh qua HTTPS an toàn.
* Làm quen với Docker và thực hành đóng gói ứng dụng container cơ bản.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Tạo Amazon S3 Buckets cho Frontend và Media; cấu hình Block Public Access để bảo mật dữ liệu. | 15/06/2026 | 15/06/2026 | https://000005.awsstudygroup.com/ |
| **Thứ 3** | - Cấu hình CloudFront Distribution trỏ origin về S3 Bucket, thiết lập OAC để bảo vệ dữ liệu trong S3. | 16/06/2026 | 16/06/2026 | https://000094.awsstudygroup.com/ |
| **Thứ 5** | - Nghiên cứu Dockerfile, viết kịch bản build Docker image và chạy thử ứng dụng Node.js cục bộ. | 18/06/2026 | 18/06/2026 | https://000015.awsstudygroup.com/ |
| **Thứ 6** | - Khởi tạo Amazon ECR repository, push Docker image lên ECR và cấu hình IAM Role cho EC2 kéo image. | 19/06/2026 | 19/06/2026 | https://000017.awsstudygroup.com/ |

### Kết quả đạt được tuần 3:

* Cấu hình thành công CloudFront phân phối tài nguyên từ S3 và chặn truy cập trực tiếp vào bucket.
* Nắm vững quy trình viết Dockerfile và đóng gói container ứng dụng.
* Đẩy thành công bản build Docker đầu tiên lên Amazon ECR lưu trữ tập trung.
