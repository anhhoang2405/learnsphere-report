---
title: "Worklog Tuần 6"
date: 2026-07-06
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# 6. Đóng gói Container Backend & Triển khai EC2

### Mục tiêu trong tuần:

* Tối ưu hóa Dockerfile phân tầng để đảm bảo an toàn thông tin và giảm dung lượng.
* Cài đặt và thiết lập môi trường vận hành Backend trên máy chủ EC2.
* Viết kịch bản bash shell tự động hóa quy trình cập nhật container.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Viết Dockerfile tối ưu phân tầng (Multi-stage build) sử dụng alpine image nhẹ, chạy dưới user non-root. | 06/07/2026 | 06/07/2026 | https://docs.docker.com/develop/develop-images/multistage-build/ |
| **Thứ 3** | - Khởi tạo máy chủ EC2 (`t3.small`) trong phân vùng Private Subnet của VPC để cô lập máy chủ backend. | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html |
| **Thứ 5** | - Cài đặt Docker trên EC2 và cấu hình thêm 2GB bộ nhớ ảo Swap để tránh tràn RAM. | 09/07/2026 | 09/07/2026 | https://docs.docker.com/engine/install/ |
| **Thứ 6** | - Kéo image Backend từ ECR về máy chủ EC2 và viết script bash tự động hóa quy trình pull image mới và khởi động lại container. | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/AmazonECR/latest/userguide/image-pull-ecr.html |

### Kết quả đạt được tuần 6:

* Dockerfile hoàn thiện giúp giảm dung lượng image Backend từ 900MB xuống còn 150MB.
* Khởi dựng máy EC2 và cấu hình Swap thành công, đảm bảo hệ thống chạy ổn định.
* Backend chạy trơn tru trong container Docker trên máy chủ EC2 và kết nối thành công tới MongoDB Atlas.
