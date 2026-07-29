---
title: "Week 3 Worklog"
date: 2026-07-25
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# 3. Tích hợp Luồng tải tệp tin lên S3 ở Frontend

### Mục tiêu trong tuần:

* Cấu hình và tích hợp luồng tải file bảo mật trực tiếp từ React Frontend lên Amazon S3 thông qua Presigned URL.
* Xây dựng giao diện upload tài liệu học tập thân thiện.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Tìm hiểu cơ chế bảo mật upload S3: Frontend gửi trực tiếp tệp lên S3 qua chữ ký số từ Backend. | 29/06/2026 | 29/06/2026 |
| 2 | Lập trình component giao diện Upload tài liệu kéo thả (Drag & Drop) ở Frontend. | 30/06/2026 | 30/06/2026 |
| 3 | Viết hàm gọi API (Fetch) đến Backend để yêu cầu cấp link GET/PUT Presigned URL. | 01/07/2026 | 01/07/2026 |
| 4 | Lập trình luồng gửi dữ liệu nhị phân (Binary PUT) trực tiếp từ client React lên S3 Bucket. | 02/07/2026 | 02/07/2026 |
| 5 | Chạy thử nghiệm và gỡ lỗi upload các tệp video bài học (.mp4) và tài liệu PDF. | 03/07/2026 | 03/07/2026 |

### Các kết quả đạt được:

* Hoàn thành Module Upload ở phía client, cho phép truyền file trực tiếp lên S3 mà không cần đi qua trung gian backend.
* Tối ưu hóa hiệu năng tải file lớn nhờ tận dụng băng thông trực tiếp của AWS S3.
