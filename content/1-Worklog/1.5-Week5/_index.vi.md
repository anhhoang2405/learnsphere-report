---
title: "Worklog Tuần 5"
date: 2026-06-29
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# 5. Tích hợp Trí tuệ nhân tạo Generative AI

### Mục tiêu trong tuần:

* Tích hợp mô hình ngôn ngữ lớn (LLM) qua Groq API phục vụ trợ lý học tập.
* Hiện thực hóa tính năng tóm tắt tài liệu tự động và sinh câu hỏi trắc nghiệm bằng AI.
* Tối ưu hóa thời gian phản hồi (latency) và chất lượng kết quả trả về của AI.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Nghiên cứu tài liệu Groq API và thiết lập kết nối Client với mô hình Llama-3. | 29/06/2026 | 29/06/2026 | https://docs.groq.com/ |
| **Thứ 3** | - Phát triển API AI Assistant trả lời câu hỏi của học viên bám sát ngữ cảnh bài học. | 30/06/2026 | 30/06/2026 | https://docs.aws.amazon.com/bedrock/ |
| **Thứ 5** | - Xây dựng tính năng tự động tóm tắt tài liệu PDF/Word tải lên và xuất kết quả dạng Markdown. | 02/07/2026 | 02/07/2026 | https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html |
| **Thứ 6** | - Viết API trích xuất văn bản từ tài liệu scan (OCR) và sinh tự động bộ câu hỏi kiểm tra (Quiz Generator) qua định dạng Prompt JSON. | 03/07/2026 | 03/07/2026 | https://docs.groq.com/docs/openai |

### Kết quả đạt được tuần 5:

* Tích hợp thành công Trợ lý AI Assistant trả lời thông minh theo thời gian thực trên web.
* Hoàn thành các API tóm tắt tài liệu và tự động sinh quiz kiểm tra kiến thức bài học.
* Tối ưu hóa tốc độ phản hồi của AI trung bình dưới 3 giây.
