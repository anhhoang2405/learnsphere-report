---
title: "Worklog Tuần 9"
date: 2026-07-27
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# 9. Tự động hóa CI/CD Pipeline & Nghiệm thu Báo cáo

### Mục tiêu trong tuần:

* Xây dựng pipeline CI/CD tự động hóa quy trình đóng gói và triển khai ứng dụng.
* Quản lý an toàn các thông tin cấu hình nhạy cảm thông qua AWS Systems Manager.
* Nghiệm thu toàn bộ tính năng và bàn giao báo cáo thực tập.

### Công việc thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| **Thứ 2** | - Cấu hình GitHub Actions CI/CD sử dụng AWS OIDC giả định vai trò IAM Role, loại bỏ việc lưu access key tĩnh. | 27/07/2026 | 28/07/2026 | https://docs.github.com/en/actions |
| **Thứ 3** | - Viết mã nguồn pipeline tự động build, tag và push Docker image lên ECR, tự động gọi script deploy trên EC2. | 28/07/2026 | 29/07/2026 | https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services |
| **Thứ 4** | - Cấu hình lưu các biến môi trường nhạy cảm (`MONGO_URI`, `JWT_SECRET`, `GROQ_API_KEY`) trên AWS SSM Parameter Store. | 29/07/2026 | 29/07/2026 | https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html |
| **Thứ 5** | - Chạy thử nghiệm toàn bộ quy trình CI/CD từ khâu push code sửa lỗi đến khi cập nhật thành công trên production. | 30/07/2026 | 30/07/2026 | https://docs.github.com/en/actions/automating-builds-and-tests/about-continuous-integration |
| **Thứ 6** | - Tổng hợp lại dữ liệu, chụp màn hình minh chứng cấu hình AWS và hoàn thiện báo cáo thực tập đúng hạn chót. | 31/07/2026 | 31/07/2026 | https://aws.amazon.com/blogs/devops/ |

### Kết quả đạt được tuần 9:

* Pipeline CI/CD hoạt động ổn định, tự động cập nhật Backend và Frontend lên AWS trong vòng dưới 3 phút.
* Bảo mật tuyệt đối thông tin cấu hình và credentials nhờ OIDC và SSM Parameter Store.
* Hoàn thành xuất sắc kỳ thực tập, nghiệm thu toàn bộ tính năng của đồ án LearnSphere.
