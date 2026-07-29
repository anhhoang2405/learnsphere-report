---
title: "Week 5 Worklog"
date: 2026-07-25
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# 5. Tích hợp dịch vụ AI cốt lõi & Test liên kết

### Mục tiêu trong tuần:

* Lập trình các tính năng AI (Chatbot trợ lý, Tóm tắt bài học, Tạo câu hỏi kiểm tra).
* Viết mã tích hợp API của Groq (Llama-3) và AWS Bedrock.
* Kiểm thử toàn diện cục bộ và xử lý các lỗi CORS và xác thực JWT.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Tìm hiểu cấu trúc request của API Groq và AWS Bedrock. | 13/07/2026 | 13/07/2026 |
| 2 | Lập trình APIs chat, tóm tắt bài học và bộ tự sinh câu hỏi trắc nghiệm. | 14/07/2026 | 14/07/2026 |
| 3 | Cấu hình API Groq và chuẩn bị hàm dự phòng Bedrock. | 15/07/2026 | 15/07/2026 |
| 4 | Gỡ lỗi cấu hình CORS trong ứng dụng Express và gán middlewares. | 16/07/2026 | 16/07/2026 |
| 5 | Kiểm thử toàn diện hệ thống cục bộ với dữ liệu giả định. | 17/07/2026 | 17/07/2026 |

### Các kết quả đạt được:

* Xây dựng tầng dịch vụ `ai-provider.service.js` hỗ trợ đồng thời APIs của Groq và Bedrock.
* Giải quyết triệt để lỗi CORS kết nối và kiểm thử sinh trắc nghiệm thành công.
* Hoàn thành kiểm thử liên kết cục bộ toàn diện trước khi đưa lên đám mây.
