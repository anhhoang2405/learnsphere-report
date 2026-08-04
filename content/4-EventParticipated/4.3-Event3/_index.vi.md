---
title: "Sự kiện 3"
date: 2026-08-01
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch: Workshop "Amazon Bedrock AgentCore - Foundations & Agent Setup"

### 1. Thông tin chung về sự kiện
*   **Tên sự kiện:** Workshop: Introduction to Amazon Bedrock AgentCore
*   **Thời gian diễn ra:** 09:00 - 12:00 ngày 01/08/2026
*   **Địa điểm:** Hội trường AWS Việt Nam, TP. Hồ Chí Minh
*   **Vai trò tham gia:** Người tham gia

---

### 2. Nội dung chi tiết chương trình (01/08 - Day 1)

#### 🕐 Khung thời gian: 09:00 – 10:00
*   **Chủ đề chính:** Giới thiệu tổng quan & Thiết lập nền tảng (Foundations & Agent Setup)
*   **Nội dung chi tiết:**
    *   Giới thiệu nội dung, mục tiêu của buổi Workshop.
    *   Nghiên cứu tổng quan về **Amazon Bedrock AgentCore**: Khám phá kiến trúc cốt lõi của tác nhân AI trên nền tảng AWS.
    *   Tìm hiểu về 3 thành phần chính:
        *   **Runtime:** Môi trường thực thi của Agent để xử lý request và điều phối luồng suy nghĩ.
        *   **Gateway:** Cổng kết nối trung gian để định tuyến các cuộc hội thoại và tích hợp dịch vụ.
        *   **Identity:** Cơ chế quản lý định danh và bảo mật cho phép Agent tương tác an toàn với các API nội bộ.
    *   Lý thuyết cơ bản và chuẩn bị tài nguyên cho phần Hands-on Lab.

#### 🕐 Khung thời gian: 10:00 – 11:00
*   **Chủ đề chính:** Thực hành triển khai & Tích hợp (Hands-on Lab & Integration)
*   **Các hoạt động thực hiện:**
    *   **Deploy a basic agent:** Thực hành khởi tạo và triển khai một tác nhân AI (AI Agent) cơ bản trong hệ thống AgentCore.
    *   **Connect external tools & Knowledge Bases:** Tích hợp công cụ mở rộng (Action Groups) và liên kết các cơ sở tri thức (Knowledge Bases) vào Agent để tăng cường khả năng truy xuất dữ liệu chính xác (RAG).
    *   **Build a Web UI & Cognito Integration:** Xây dựng giao diện web tương tác (Web UI) dạng chatbot và tích hợp dịch vụ quản lý định danh **Amazon Cognito** để xác thực người dùng bảo mật.

#### 🕐 Khung thời gian: 11:00 – 12:00
*   **Chủ đề chính:** Kiểm thử, Hỏi đáp & Dọn dẹp tài nguyên
*   **Các hoạt động thực hiện:**
    *   Thực hiện kiểm thử đầu cuối (End-to-End Testing) quy trình đăng nhập qua Cognito và chat với Agent trực tiếp trên Web UI.
    *   Phiên thảo luận (Q&A Session) với các chuyên gia giải pháp AWS để tháo gỡ các vướng mắc kỹ thuật trong quá trình lab.
    *   Thực hiện quy trình dọn dẹp tài nguyên (Resource Cleanup) đã khởi tạo trên tài khoản AWS để tránh phát sinh chi phí phát sinh ngoài ý muốn.

---

### 3. Hình ảnh minh chứng tham gia sự kiện

Dưới đây là sơ đồ kiến trúc hệ thống Bedrock AgentCore và giao diện quản trị Agent tích hợp Cognito được triển khai trực quan tại buổi workshop:

![Sơ đồ kiến trúc Amazon Bedrock AgentCore](/images/4-EventParticipated/event3a.jpg)

![Giao diện Web UI Agent tích hợp Amazon Cognito](/images/4-EventParticipated/event3b.jpg)
