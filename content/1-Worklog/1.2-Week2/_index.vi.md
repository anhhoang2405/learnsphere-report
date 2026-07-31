---
title: "Week 2 Worklog"
date: 2026-07-25
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

# 2. Phối hợp Thiết lập Kiến trúc Backend & Database Schema

### Mục tiêu trong tuần:

* Xác định mô hình kiến trúc và phối hợp thiết lập cơ sở dữ liệu MongoDB Atlas.
* Khởi tạo dự án Express.js Backend làm nền tảng API cho toàn hệ thống.

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Họp bàn cùng nhóm phác thảo luồng nghiệp vụ của ứng dụng; khởi tạo khung mã nguồn Express.js Backend. | 22/06/2026 | 22/06/2026 |
| 2 | Phối hợp cùng Dũng (chịu trách nhiệm backend chính) thiết kế các Schema Mongoose (User, Course, Lesson, Quiz). | 23/06/2026 | 23/06/2026 |
| 3 | Thống nhất với Sơn (chịu trách nhiệm frontend) về cấu trúc JSON đầu ra/vào của API để FE và BE ăn khớp. | 24/06/2026 | 24/06/2026 |
| 4 | Cấu hình cấu trúc Express routing và cài đặt các middleware cơ bản như CORS, body-parser, morgan. | 25/06/2026 | 25/06/2026 |
| 5 | Tạo cluster MongoDB Atlas trên hạ tầng AWS, cấu hình whitelist IP và tài khoản kết nối bảo mật. | 26/06/2026 | 26/06/2026 |

### Các kết quả đạt được:

* Dựng xong khung server Express chạy thử local ổn định và sẵn sàng cho các API nghiệp vụ.
* Thống nhất thiết kế Database Schema phù hợp với yêu cầu lưu trữ và tương thích với UI của Frontend.
