---
title: "Worklog Tuần 2"
date: 2026-09-21
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần này:

* Quản lý chi phí và thiết lập ngân sách để giám sát tài nguyên AWS bằng AWS Budgets.
* Giám sát toàn diện hạ tầng và ứng dụng với Amazon CloudWatch (Metrics, Logs, Alarms, Dashboards).
* Triển khai cơ sở dữ liệu quan hệ Amazon RDS tích hợp với máy chủ web EC2 và ứng dụng Node.js.
* Xây dựng kiến trúc Độ sẵn sàng cao (High Availability) và Tự động mở rộng (Auto Scaling) bằng Elastic Load Balancing (ELB) và Auto Scaling Group (ASG).
* Cấu hình kiến trúc Hybrid DNS kết nối On-Premise Active Directory và Amazon Route 53 Resolver.

### Các công việc cần triển khai:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Quản lý chi phí với AWS Budgets: <br>&emsp; + Tạo Cost Budget để kiểm soát chi phí định kỳ <br>&emsp; + Tạo Usage Budget để giám sát số giờ sử dụng tài nguyên <br>&emsp; + Tìm hiểu về Reservation Budget & Savings Plans Budget <br>&emsp; + Thiết lập ngưỡng cảnh báo qua Email <br>&emsp; + Thực hiện dọn dẹp tài nguyên Ngân sách | 21/09/2026 | 21/09/2026 | <https://000007.awsstudygroup.com/> |
| 3 | - Giám sát hệ thống với Amazon CloudWatch: <br>&emsp; + Khởi tạo hạ tầng lab bằng CloudFormation Template <br>&emsp; + Trực quan hóa Metrics sử dụng Search Expressions & Math Expressions <br>&emsp; + Cấu hình Dynamic Labels tự động <br>&emsp; + Quản lý CloudWatch Logs & truy vấn với Logs Insights Engine <br>&emsp; + Tạo Metric Filters & cấu hình CloudWatch Alarms <br>&emsp; + Xây dựng CloudWatch Dashboard tập trung | 22/09/2026 | 22/09/2026 | <https://000008.awsstudygroup.com/> |
| 4 | - Triển khai Cơ sở dữ liệu Amazon RDS & Ứng dụng Web: <br>&emsp; + Thiết lập hạ tầng mạng VPC, Security Groups (ec2-sg, rds-sg) & DB Subnet Group <br>&emsp; + Khởi tạo Amazon RDS MySQL Instance với cấu hình Multi-AZ <br>&emsp; + Khởi tạo web server EC2 Amazon Linux 2023 và SSH qua MobaXterm <br>&emsp; + Triển khai Ứng dụng Web Node.js, quản lý tiến trình chạy ngầm bằng PM2 <br>&emsp; + Khởi tạo cơ sở dữ liệu MySQL và thực hiện các thao tác CRUD <br>&emsp; + Thực hành quy trình Backup, Snapshots và Khôi phục Database | 23/09/2026 | 24/09/2026 | <https://000005.awsstudygroup.com/> |
| 5 | - Auto Scaling với Load Balancer & Auto Scaling Group: <br>&emsp; + Thiết lập Multi-AZ VPC, Security Groups (fcaj-sg, fcaj-db-sg) <br>&emsp; + Tạo AMI từ EC2 Instance và cấu hình Launch Template <br>&emsp; + Tạo Application Load Balancer (ALB) & Target Group <br>&emsp; + Cấu hình Auto Scaling Group (ASG) tích hợp với ALB và Thông báo SNS <br>&emsp; + Kiểm thử các chiến lược mở rộng: Manual Scaling, Scheduled Scaling, Dynamic Scaling (Target Tracking) & Predictive Scaling bằng JMeter | 25/09/2026 | 25/09/2026 | <https://000006.awsstudygroup.com/> |
| 6 | - Thiết lập Kiến trúc Hybrid DNS với Route 53 Resolver: <br>&emsp; + Triển khai hạ tầng mạng sử dụng AWS Quick Start & CloudFormation <br>&emsp; + Khởi tạo AWS Managed Microsoft Active Directory mô phỏng DNS On-premise <br>&emsp; + Cấu hình Route 53 Outbound Endpoints & Inbound Endpoints <br>&emsp; + Thiết lập Route 53 Resolver Rules để chuyển tiếp truy vấn tên miền <br>&emsp; + Kiểm thử phân giải tên miền hai chiều giữa On-premise và Route 53 <br>&emsp; + Dọn dẹp toàn bộ tài nguyên đã triển khai | 26/09/2026 | 26/09/2026 | <https://000010.awsstudygroup.com/> |

### Kết quả đạt được:

* **Thao tác với công cụ quản lý chi phí AWS Budgets**: Nắm vững cách thiết lập các loại ngân sách (Cost, Usage, RI, Savings Plans) và cấu hình cảnh báo tự động qua email để chủ động kiểm soát chi phí vận hành trên AWS.
* **Thao tác với Amazon CloudWatch**: Sử dụng thành thạo CloudWatch Logs Insights để truy vấn log sâu, tạo Metric Filters từ log lỗi, cấu hình Alarms và xây dựng Dashboard theo dõi tập trung.
* **Triển khai ứng dụng Web với Amazon RDS**: Nắm vững quy trình tạo VPC multi-AZ, phân tách Security Groups giữa Web Tier và Database Tier, khởi tạo RDS MySQL Multi-AZ instances và chạy ứng dụng Node.js chạy ngầm với PM2.
* **Sao lưu & Khôi phục dữ liệu**: Quản lý thành thạo DB Snapshots và khôi phục cơ sở dữ liệu RDS về thời điểm mong muốn (Point-in-time recovery).
* **Tự động hóa mở rộng hạ tầng với ELB & ASG**: Xây dựng thành công hệ thống có độ sẵn sàng cao, phân phối lưu lượng qua Application Load Balancer và tự động điều chỉnh số lượng EC2 instance dựa trên nhu cầu tải thực tế.
* **Hiểu rõ các chiến lược Scaling**: So sánh và đánh giá hiệu năng giữa các phương pháp mở rộng: Manual Scaling, Scheduled Scaling, Dynamic Scaling (Target Tracking), và Predictive Scaling thông qua mô phỏng kiểm thử tải bằng JMeter.
* **Xây dựng hạ tầng Hybrid DNS**: Cấu hình thành công Inbound/Outbound Endpoints và Resolver Rules trên Route 53 Resolver, cho phép phân giải tên miền liền mạch giữa On-premise AD và các tài nguyên trên AWS Cloud.