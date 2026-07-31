---
title: "Worklog Tuần 4"
date: 2026-06-22
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

# 4. Thiết kế Database & Xây dựng API S3 Presigned URL

### Mục tiêu trong tuần:

* Thiết kế cấu trúc dữ liệu MongoDB Atlas cho đồ án LearnSphere.
* Phát triển các API backend hỗ trợ tải lên tệp tin media an toàn trực tiếp từ trình duyệt.
* Cấu hình giao thức CORS bảo vệ ứng dụng.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Thiết kế Schema cơ sở dữ liệu MongoDB Atlas (Khóa học, Học viên, Video, Bài học...). | 22/06/2026 | 22/06/2026 | https://mongoosejs.com/docs/guide.html |
| **Thứ 3** | - Hỗ trợ Dũng viết API đăng ký, đăng nhập và cấu hình JWT Authentication middleware bảo mật. | 23/06/2026 | 24/06/2026 | https://jwt.io/introduction |
| **Thứ 4** | - Cấu hình MongoDB Atlas IP Access List, cho phép địa chỉ IP của EC2 truy cập cơ sở dữ liệu. | 24/06/2026 | 24/06/2026 | https://docs.atlas.mongodb.com/security/ |
| **Thứ 5** | - Viết API sinh S3 Presigned URL để Frontend tải ảnh đại diện, thumbnail trực tiếp lên S3 mà không qua Backend. | 25/06/2026 | 25/06/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html |
| **Thứ 6** | - Cấu hình CORS allowlist trên Express Backend để kết nối trơn tru với cổng React Frontend. | 26/06/2026 | 26/06/2026 | https://expressjs.com/en/resources/middleware/cors.html |

### Kết quả đạt được tuần 4:

* Hoàn thiện 11 Mongoose Schemas đáp ứng đầy đủ các nghiệp vụ của LearnSphere.
* Phát triển thành công tính năng upload file an toàn qua S3 Presigned URL.
* Giải quyết hoàn toàn các lỗi chặn request CORS giữa Frontend và Backend.
