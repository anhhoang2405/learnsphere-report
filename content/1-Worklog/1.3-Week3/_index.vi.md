---
title: "Week 3 Worklog"
date: 2026-07-25
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# 3. Tích hợp lưu trữ Amazon S3

### Mục tiêu trong tuần:

* Cấu hình AWS SDK S3 trong Backend LearnSphere để quản lý tài liệu học tập.
* Xây dựng tính năng tải lên an toàn bằng đường dẫn S3 Presigned URL.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Tìm hiểu kiến trúc lưu trữ S3: Presigned URL và tải lên trực tiếp. | 29/06/2026 | 29/06/2026 |
| 2 | Viết helper xử lý file trong file.service.js. | 30/06/2026 | 30/06/2026 |
| 3 | Viết logic tạo chữ ký GET/PUT của S3 thông qua AWS SDK v3. | 01/07/2026 | 01/07/2026 |
| 4 | Thêm các điều kiện ràng buộc định dạng file tải lên. | 02/07/2026 | 02/07/2026 |
| 5 | Kiểm thử chu trình upload-download từ S3 cục bộ. | 03/07/2026 | 03/07/2026 |

### Các kết quả đạt được:

* Tích hợp thành công AWS SDK v3 S3 client.
* Hoàn thành các APIs tạo đường dẫn tải lên (`PresignedUpload`) và tải xuống (`PresignedDownload`).
* Tăng cường bảo mật S3 bằng cách chỉ sinh chữ ký có thời hạn ngắn (Presigned URL) cho học sinh.
