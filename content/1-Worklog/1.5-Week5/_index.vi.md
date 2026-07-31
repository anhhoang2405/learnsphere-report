---
title: "Week 5 Worklog"
date: 2026-07-25
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# 5. Tích hợp Dịch vụ AI & Kiểm thử Liên kết cục bộ

### Mục tiêu trong tuần:

* Yêu cầu quyền truy cập mô hình trên AWS Bedrock và tích hợp Bedrock Converse API, Groq API vào Backend.
* Thực hiện kiểm thử liên kết toàn diện (End-to-End) local và gỡ các lỗi kết nối CORS.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Truy cập AWS Console gửi yêu cầu kích hoạt Model Access cho mô hình Anthropic Claude trên AWS Bedrock. | 13/07/2026 | 13/07/2026 |
| 2 | Viết service `ai-provider.service.js` ở Backend làm cổng tích hợp chung cho cả AWS Bedrock SDK và Groq API. | 14/07/2026 | 14/07/2026 |
| 3 | Lập trình các API route phục vụ Trợ lý AI (`/api/ai/chat`) và sinh bộ câu hỏi trắc nghiệm tự động từ AI. | 15/07/2026 | 15/07/2026 |
| 4 | Hỗ trợ Sơn kết nối React Frontend với các API AI, cấu hình chi tiết middleware CORS trên Express để tránh lỗi preflight. | 16/07/2026 | 16/07/2026 |
| 5 | Chạy thử nghiệm chuỗi luồng nghiệp vụ E2E cục bộ: Đăng nhập -> Tạo khóa học -> Upload tệp S3 -> Sinh Quiz -> Hỏi đáp AI giải đáp bài học. | 17/07/2026 | 17/07/2026 |

### Các kết quả đạt được:

* Tích hợp thành công lõi xử lý AI (AWS Bedrock Claude & Groq), các API sinh câu hỏi và chat phản hồi nhanh dưới 2s.
* Giải quyết triệt để lỗi kết nối CORS preflight khi client React gửi kèm Auth Token trong Header lên Backend.
* Hệ thống LearnSphere vận hành mượt mà trên local, sẵn sàng cho việc đóng gói và đưa lên AWS cloud.
