---
title: "Week 4 Worklog"
date: 2026-07-25
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

# 4. Phát triển API Backend Core & Middleware JWT

### Mục tiêu trong tuần:

* Xây dựng hệ thống API quản lý khóa học, bài học và cơ sở dữ liệu bài thi trắc nghiệm (Quiz).
* Thiết lập cơ chế xác thực bảo mật JWT và phân quyền vai trò người dùng (Tutor/Student/Admin).

### Các đầu việc đã thực hiện trong tuần:

| Thứ | Công việc thực hiện | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | Cài đặt và cấu hình thư viện `jsonwebtoken` và `bcryptjs` để xử lý xác thực bảo mật tài khoản. | 06/07/2026 | 06/07/2026 |
| 2 | Phối hợp viết API Đăng ký & Đăng nhập, kiểm tra và lưu dữ liệu người dùng mã hóa vào MongoDB. | 07/07/2026 | 07/07/2026 |
| 3 | Xây dựng middleware xác thực token JWT (`authMiddleware`) bảo vệ các routes riêng tư của hệ thống. | 08/07/2026 | 08/07/2026 |
| 4 | Lập trình các middleware phân quyền (`roleMiddleware`) để kiểm tra quyền hạn thao tác (Học viên/Giáo viên/Admin). | 09/07/2026 | 09/07/2026 |
| 5 | Kết nối và hỗ trợ Dũng phát triển bộ API CRUD quản lý khóa học (chuyển đổi trạng thái Draft/Published) và bài học. | 10/07/2026 | 10/07/2026 |

### Các kết quả đạt được:

* Hệ thống xác thực JWT và cơ chế phân quyền vai trò được hoàn tất bảo mật ở Backend.
* Hoàn thành bộ API CRUD lõi quản lý thông tin các khóa học và cấu trúc bài học động.
