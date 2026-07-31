---
title: "Worklog Tuần 2"
date: 2026-06-08
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

# 2. Quản lý định danh IAM & Cấu hình mạng Amazon VPC

### Mục tiêu trong tuần:

* Nghiên cứu về cơ chế phân quyền, bảo mật của AWS Identity and Access Management (IAM).
* Thiết kế và cấu hình phân vùng mạng VPC tùy chỉnh cho hệ thống LearnSphere.
* Xác lập các quy tắc tường lửa (Security Group, Network ACL) để bảo vệ tài nguyên.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Nghiên cứu cơ chế IAM (User, Group, Role, Policy) và thực hành phân quyền theo đặc quyền tối thiểu. | 08/06/2026 | 08/06/2026 | https://000002.awsstudygroup.com/ |
| **Thứ 3** | - Sử dụng AWS Pricing Calculator để dự toán chi phí cho hạ tầng LearnSphere dự kiến triển khai trên Cloud. | 09/06/2026 | 09/06/2026 | https://000007.awsstudygroup.com/ |
| **Thứ 5** | - Tạo VPC tùy chỉnh cho dự án gồm các phân vùng Public Subnet và Private Subnet ở các AZ khác nhau. | 11/06/2026 | 11/06/2026 | https://000003.awsstudygroup.com/ |
| **Thứ 6** | - Cấu hình Internet Gateway, Route Tables và Security Groups cho EC2 để mở các cổng cần thiết. | 12/06/2026 | 12/06/2026 | https://000004.awsstudygroup.com/<br>https://000057.awsstudygroup.com/ |

### Kết quả đạt được tuần 2:

* Nắm vững nguyên tắc bảo mật IAM và cấu hình MFA bảo vệ tài khoản.
* Tạo thành công bản dự toán chi phí vận hành hệ thống LearnSphere trên AWS.
* Triển khai hoàn chỉnh sơ đồ mạng VPC bảo mật với các phân vùng subnet tách biệt.
