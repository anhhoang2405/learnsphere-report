---
title: "Week 3 Worklog"
date: 2026-07-25
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# 3. Cấu hình Amazon S3 & API Presigned URL

### Mục tiêu trong tuần:

* Khởi tạo và cấu hình Amazon S3 Bucket phục vụ lưu trữ tài nguyên học tập (Video bài giảng, PDF).
* Thiết lập phân quyền IAM và viết API cấp S3 Presigned URL ở Backend để client upload/stream trực tiếp bảo mật.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Tìm hiểu cơ chế bảo mật upload S3: client gửi tệp trực tiếp lên S3 thông qua chữ ký số do Backend cung cấp. | 29/06/2026 | 29/06/2026 |
| 2 | Khởi tạo Amazon S3 Bucket và cấu hình chính sách CORS để cho phép Frontend React gọi API upload trực tiếp. | 30/06/2026 | 30/06/2026 |
| 3 | Tạo tài khoản IAM User, thiết lập Access Keys và gắn Policy chỉ cho phép thao tác đọc/ghi trên bucket chỉ định. | 01/07/2026 | 01/07/2026 |
| 4 | Lập trình các endpoint ở Backend để sinh link Presigned URL (chữ ký PUT để upload, GET để stream video). | 02/07/2026 | 02/07/2026 |
| 5 | Dùng Postman chạy thử nghiệm yêu cầu cấp URL và đẩy file nhị phân (.mp4, .pdf) trực tiếp lên S3 thành công. | 03/07/2026 | 03/07/2026 |

### Các kết quả đạt được:

* Cấu hình xong S3 Media Bucket đạt chuẩn bảo mật và tích hợp thành công bộ SDK AWS S3 Client v3 vào Backend.
* Hoàn thành API cấp link upload/stream, tối ưu hiệu năng truyền tải các file bài học có dung lượng lớn.
