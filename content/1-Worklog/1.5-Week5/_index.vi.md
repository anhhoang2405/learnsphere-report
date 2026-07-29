---
title: "Week 5 Worklog"
date: 2026-07-25
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# 5. Tích hợp Dịch vụ AI & Kiểm thử Liên kết cục bộ

### Mục tiêu trong tuần:

* Tích hợp giao diện Trợ lý AI (AI Tutor) và trình làm bài kiểm tra trắc nghiệm (Quiz System) ở Frontend.
* Chạy kiểm thử liên kết toàn diện (End-to-End) cục bộ giữa Frontend và Backend.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Tìm hiểu luồng truyền nhận dữ liệu của API AI Chatbot và API tự sinh câu hỏi Quiz. | 13/07/2026 | 13/07/2026 |
| 2 | Lập trình giao diện khung chat Trợ lý AI (AI Tutor) dạng trượt (sidebar) ở Frontend. | 14/07/2026 | 14/07/2026 |
| 3 | Lập trình giao diện làm bài Quiz tương tác của học sinh (nhận dữ liệu JSON sinh ra từ AI). | 15/07/2026 | 15/07/2026 |
| 4 | Phối hợp với Nguyễn Hồng Sơn xử lý lỗi CORS kết nối và cấu hình tự động đính kèm Token JWT vào Header. | 16/07/2026 | 16/07/2026 |
| 5 | Chạy thử nghiệm chuỗi luồng nghiệp vụ: Đăng nhập -> Tạo khóa học -> Upload tệp -> Tự động sinh Quiz -> Làm bài -> Chat AI giải đáp lỗi. | 17/07/2026 | 17/07/2026 |

### Các kết quả đạt được:

* Hoàn thành giao diện tương tác AI đắc lực cho học viên (Khung chat AI và Trình làm bài tập Quiz).
* Giải quyết triệt để lỗi kết nối CORS và mã hóa an toàn token đăng nhập client.
* Toàn bộ hệ thống LearnSphere vận hành mượt mà, sẵn sàng chuyển giao lên môi trường đám mây AWS.
