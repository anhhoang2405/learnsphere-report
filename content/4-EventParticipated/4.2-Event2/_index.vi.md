---
title: "Sự kiện 2"
date: 2026-07-25
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch: Tham dự Demo Day - ASEAN Agentic AI Buildathon (AABW)

### 1. Thông tin chung về sự kiện
*   **Tên sự kiện:** ASEAN Agentic AI Buildathon (AABW) - Demo Day & Project Showcase
*   **Thời gian diễn ra:** 09:00 - 12:00 ngày 25/07/2026
*   **Địa điểm:** Hội trường AWS Việt Nam, TP. Hồ Chí Minh
*   **Vai trò tham gia:** Người tham gia

---

### 2. Mục tiêu tham gia sự kiện
*   Tìm hiểu xu hướng phát triển và ứng dụng của Agentic AI (Trí tuệ nhân tạo dạng tác nhân) trong thực tế thông qua các sản phẩm công nghệ của các đội thi.
*   Nghiên cứu kiến trúc giải pháp Cloud của các dự án lớn, cách kết hợp dịch vụ AWS (Bedrock, SageMaker, Lambda) với các mô hình AI tiên tiến.
*   Thu thập kiến thức thực tế về quy trình phát triển sản phẩm công nghệ dưới áp lực thời gian (Hackathon 24 giờ) và cách trình bày sản phẩm (Pitching) trước hội đồng ban giám khảo AWS.

---

### 3. Phân tích các dự án tiêu biểu tại sự kiện
Trong buổi Demo Day, tôi đã có cơ hội lắng nghe và phân tích kiến trúc hạ tầng của các dự án xuất sắc:

#### A. Dự án S.H.E.P.H.E.R.D (Nhóm 3KA)
*   **Mục tiêu:** Hệ thống thông minh giám sát mật độ đám đông, xếp hàng và dự báo tắc nghẽn thời gian thực tại các sự kiện.
*   **Kiến trúc kỹ thuật:** 
    *   Sử dụng **YOLO + ByteTrack** để phát hiện và theo dõi chuyển động người qua camera.
    *   Hạ tầng AI chạy trên máy chủ **Amazon SageMaker Endpoint** để xử lý suy luận hình ảnh.
    *   Kết hợp **Amazon Bedrock AgentCore + Strands Agent** để ra quyết định và gửi cảnh báo tự động về bảng điều khiển React.

#### B. Dự án Signal Scout (Nhóm Signal Scout)
*   **Mục tiêu:** AI Agent tự động thu thập và phân tích các tín hiệu thay đổi chiến lược của doanh nghiệp để đưa ra cảnh báo rủi ro sớm.
*   **Kiến trúc kỹ thuật:** 
    *   Sử dụng **Apify & TinyFish** để tự động cào (crawl) thông tin từ internet.
    *   Luồng xử lý tự động hóa thông qua **API Gateway -> AWS Lambda** để điều phối và ghi nhận dữ liệu vào **DynamoDB**.
    *   Tích hợp **AgentCore Runtime** kết hợp với **Amazon Bedrock** và **Bedrock Guardrails** để phân tích dữ liệu chuyên sâu và bảo mật thông tin đầu ra.

#### C. Dự án KFC Bot Agent (Nhóm One Team)
*   **Mục tiêu:** Trợ lý AI hội thoại đặt món ăn đa kênh tự động (Zalo OA, Messenger, WhatsApp) không cần tải ứng dụng hay đăng ký tài khoản rườm rà.
*   **Kiến trúc kỹ thuật:** 
    *   Tin nhắn người dùng qua Zalo được tiếp nhận qua **WAF & API Gateway**, đưa vào hàng đợi **Amazon SQS** để điều phối tải.
    *   Xử lý logic và ra quyết định bằng **Bedrock Agentcore** kết hợp với **OpenSearch Service** để tìm kiếm món ăn nhanh chóng.
    *   Giúp cắt giảm **60% lượng code hạ tầng** nhờ tận dụng tối đa kiến trúc AgentCore của AWS.

---

### 4. Bài học và Giá trị tích lũy
*   **Hiểu biết sâu sắc về Agentic AI:** Hiểu rõ sự khác biệt giữa Chatbot thông thường (chỉ trả lời câu hỏi) và AI Agent thực thụ (có khả năng lập kế hoạch, gọi công cụ - Tool Call, tự động đưa ra hành động và quản lý bộ nhớ dài/ngắn hạn).
*   **Kinh nghiệm thiết kế Serverless:** Học tập cách các nhóm thiết kế hệ thống tối ưu hóa chi phí (ví dụ như bài toán tối ưu chi phí hạ tầng Bedrock và Lambda của nhóm Signal Scout giảm giá chạy từ $130 xuống còn $35/tháng).
*   **Động lực phát triển bản thân:** Thấy được cách các nhóm vượt qua các thử thách khó khăn như thiếu hụt thời gian ngủ, lỗi code vào 3 giờ sáng để tạo nên các ứng dụng MVP hoàn chỉnh. Điều này tạo động lực to lớn cho việc hoàn thiện đồ án LearnSphere của tôi.

---

### 5. Hình ảnh minh chứng tham gia sự kiện
Dưới đây là hình ảnh ghi nhận không khí buổi chia sẻ và trình diễn công nghệ cực kỳ sôi động tại Demo Day:

![Minh chứng tham gia AABW Demo Day 1](/images/4-EventParticipated/event2a.jpg)
![Minh chứng tham gia AABW Demo Day 2](/images/4-EventParticipated/event2b.jpg)
