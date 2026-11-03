---
title: "Worklog Tuần 3"
date: 2026-09-28
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Hiểu chiến lược hiện đại hóa ứng dụng và phương pháp phân rã kiến trúc Monolith sang Microservices.
* Nắm vững mô hình quản trị dữ liệu phân tán (Database-per-Service, Polyglot Persistence, Eventual Consistency).
* Tìm hiểu kiến trúc Microservices chuẩn trên AWS sử dụng API Gateway, Lambda, ECS và các dịch vụ truyền thông điệp (SQS, SNS).
* Bao quát hệ sinh thái các dịch vụ AWS cốt lõi phục vụ thiết kế và vận hành hệ thống Production.
* Phân tích kiến trúc dự án Ownword, thiết kế mô hình AWS Serverless mục tiêu, tối ưu phạm vi MVP và thiết lập cơ chế phòng thủ chi phí.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Phân rã Monolith sang Microservices: <br>&emsp; + Tìm hiểu chiến lược phân rã và xác định ranh giới nghiệp vụ <br>&emsp; + Áp dụng Domain-Driven Design (DDD) & Bounded Contexts <br>&emsp; + Mẫu thiết kế Strangler Fig phục vụ chuyển đổi từng phần <br>&emsp; + Tách rời logic ứng dụng và cơ sở dữ liệu nguyên khối | 28/09/2026 | 28/09/2026 | <https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-decomposing-monoliths/introduction.html> |
| 3   | - Quản trị CSDL phân tán & Hiện đại hóa lưu trữ dữ liệu: <br>&emsp; + Mô hình Database-per-Service và quyền sở hữu dữ liệu độc lập <br>&emsp; + Nguyên tắc Polyglot Persistence (RDS/Aurora, DynamoDB, ElastiCache, DocumentDB) <br>&emsp; + Xử lý ranh giới giao dịch, Eventual Consistency và Saga Pattern <br>&emsp; + Các mẫu đồng bộ dữ liệu (CQRS, Transactional Outbox, CDC với AWS DMS) | 29/09/2026 | 29/09/2026 | <https://docs.aws.amazon.com/whitepapers/latest/microservices-on-aws/data-store.html> <br> <https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-data-persistence/introduction.html> |
| 4   | - Kiến trúc Microservices & Các dịch vụ AWS cốt lõi cho Production: <br>&emsp; + Single Entry Point với Amazon API Gateway (Routing, Throttling, Auth) <br>&emsp; + Tầng Compute: Serverless (Lambda) & Containers (ECS/Fargate) <br>&emsp; + Giao tiếp bất đồng bộ và giảm phụ thuộc với Amazon SQS, SNS & EventBridge <br>&emsp; + Nhóm dịch vụ hạ tầng thực tế: Edge/CDN (CloudFront, Route 53), Security (WAF, Cognito) | 30/09/2026 | 30/09/2026 | <https://docs.aws.amazon.com/whitepapers/latest/microservices-on-aws/simple-microservices-architecture-on-aws.html> <br> <https://youtu.be/n28iOV_Y_tQ?si=p4dBo5Qh_cATC62E> |
| 5   | - Phân tích kiến trúc Ownword & Thiết kế chuyển đổi Serverless: <br>&emsp; + Phân tích công nghệ hiện tại: Bóc tách và giải thích các công nghệ lõi của Ownword (Next.js, D1, Drizzle, Gemini API) dưới góc nhìn của sinh viên AI <br>&emsp; + Vẽ sơ đồ kiến trúc: Tạo sơ đồ Mermaid trực quan hóa hệ thống Cloudflare hiện tại và kiến trúc AWS Serverless mục tiêu <br>&emsp; + Tối ưu phạm vi MVP: Đánh giá tài liệu kiến trúc để chủ động lược bỏ các dịch vụ chưa cần thiết (S3, SQS, EventBridge, CloudFront) để tránh rủi ro chi phí | 01/10/2026 | 01/10/2026 | <https://docs.aws.amazon.com/serverless/> |
| 6   | - Thiết lập phòng vệ chi phí & Tổng hợp chiến lược triển khai: <br>&emsp; + Thiết lập bảo vệ chi phí: Lên phương án cấu hình AWS Budgets 1 USD/tháng và cảnh báo tức thời CloudWatch Billing Alarms để ngăn ngừa phát sinh chi phí ngoài ý muốn <br>&emsp; + Xác thực biểu giá Free Tier: Phân tích chi tiết định mức miễn phí và cách cấu hình an toàn tuyệt đối cho Amplify, Cognito, Lambda, API Gateway và RDS PostgreSQL <br>&emsp; + Tổng hợp chiến lược triển khai: Đóng gói toàn bộ kiến thức kỹ thuật và kế hoạch phòng thủ chi phí vào tài liệu tổng hợp | 02/10/2026 | 02/10/2026 | <https://aws.amazon.com/free/> <br> <https://aws.amazon.com/aws-cost-management/aws-budgets/> |

### Kết quả đạt được tuần 3:

* **Tư duy kiến trúc Microservices**: Nắm vững phương pháp phân rã hệ thống monolithic theo từng giai đoạn thông qua Domain-Driven Design (DDD), Bounded Contexts và Strangler Fig pattern nhằm giảm thiểu rủi ro vận hành.
* **Quản trị dữ liệu phân tán**: Nắm vững nguyên lý Database-per-Service để cô lập dữ liệu theo từng microservice, loại bỏ các nút thắt cổ chai của CSDL dùng chung (*shared database*) và duy trì tính *loose coupling*.
* **Polyglot Persistence**: Sử dụng linh hoạt các dịch vụ cơ sở dữ liệu chuyên biệt trên AWS (Amazon DynamoDB, Amazon RDS/Aurora, Amazon ElastiCache) tối ưu cho từng loại dữ liệu và mục đích truy vấn.
* **Xử lý nhất quán dữ liệu phân tán**: Hiểu rõ các cơ chế quản lý giao dịch phân tán và đảm bảo Eventual Consistency thông qua Saga pattern, Event Sourcing và kỹ thuật Change Data Capture (CDC).
* **Thiết kế Microservices trên AWS**: Nắm bắt kiến trúc kết hợp Amazon API Gateway làm cổng giao tiếp tập trung (định tuyến, kiểm soát truy cập, bảo mật) với các dịch vụ tính toán co giãn (AWS Lambda, ECS/Fargate) và truyền thông điệp (SQS, SNS).
* **Bao quát hệ sinh thái AWS Production**: Nhận diện rõ vai trò và cách liên kết của nhóm ~10% dịch vụ AWS cốt lõi nhất phục vụ thiết kế hạ tầng, bảo mật và vận hành ứng dụng trong môi trường thực tế.
* **Bóc tách kiến trúc Ownword & Thiết kế Serverless**: Phân tích toàn diện tech stack hiện tại (Next.js, Cloudflare D1, Drizzle, Gemini API) và hoàn thiện sơ đồ Mermaid minh họa mô hình AWS Serverless mục tiêu.
* **Phòng thủ chi phí chủ động & Tối ưu hóa MVP**: Thiết lập hàng rào cảnh báo chi phí nghiêm ngặt (AWS Budgets 1 USD/tháng, CloudWatch Billing Alarms), thu gọn phạm vi MVP nhằm tối ưu Free Tier và hoàn thiện tài liệu chiến lược triển khai.
