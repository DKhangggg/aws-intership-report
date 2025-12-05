---
title: "Worklog Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4: Khả năng mở rộng, Giám sát và Mạng phân phối (29/09 – 03/10)

Tự động hóa khả năng mở rộng hệ thống, thiết lập giám sát toàn diện và tối ưu hóa việc phân phối nội dung toàn cầu.

### Các công việc triển khai trong tuần:

| Ngày    | Công việc chính                                                                                                                                        | Ngày thực hiện                                                                                                                      | Trạng thái | Nguồn tài liệu                            |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------- | ---------- | ----------------------------------------- |
| Thứ Hai | **EC2 Auto Scaling**<br>- Tạo Launch Templates<br>- Cấu hình Auto Scaling Group (Min=2, Max=4)<br>- Thiết lập Target Tracking Scaling Policy (CPU 50%) | 29/09/2025                                                                                                                          | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Ba  | **Amazon CloudWatch**<br>- Theo dõi Metrics chuẩn<br>- Cài đặt CloudWatch Agent cho Memory Usage<br>- Tạo Alarms và gửi thông báo qua SNS              | 30/09/2025                                                                                                                          | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Tư  | **Route 53 & CloudFront**<br>- Quản lý DNS với Route 53<br>- Cấu hình Failover Routing<br>- Triển khai CloudFront CDN với OAC                          | 01/10/2025                                                                                                                          | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Năm | **AWS CLI & VPC Peering**<br>- Automation với AWS CLI scripts<br>- Thiết lập VPC Peering<br>- Cập nhật Route Tables                                    | 02/10/2025                                                                                                                          | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Sáu | **Lambda@Edge**<br>- Triển khai edge computing<br>- Viết Lambda functions cho CloudFront<br>- Thực hiện A/B testing                                    | 03/10/2025                                                                                                                          | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.3    | 3                                                                                                                                                      | **S3 - Public Policy:** <br> - Tắt "Block Public Access" <br> - Viết Bucket Policy (JSON) cho phép s3:GetObject                     | 30/09/2025 | 01/10/2025                                | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.4    | 4                                                                                                                                                      | **RDS - Subnet Group:** <br> - Tạo DB Subnet Group <br> - Bao gồm 2 Private Subnets đã tạo ở Tuần 2                                 | 01/10/2025 | 01/10/2025                                | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.5    | 4                                                                                                                                                      | **RDS - Launch DB:** <br> - Khởi chạy RDS MySQL (Free Tier) <br> - Tắt Multi-AZ <br> - Tắt Public Accessibility                     | 01/10/2025 | 02/10/2025                                | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.6    | 5                                                                                                                                                      | **Security - Security Chaining:** <br> - Cấu hình Security Group của RDS <br> - Chỉ cho phép Inbound Port 3306 từ SG của Cloud9/EC2 | 02/10/2025 | 03/10/2025                                | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.7    | 6                                                                                                                                                      | **Database - Connection Test:** <br> - Sử dụng terminal trên Cloud9 <br> - Kết nối MySQL: `mysql -h <endpoint> -u admin -p`         | 03/10/2025 | 05/10/2025                                | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 4:

- **Web:**

  - Website tĩnh đã hoạt động tại S3 Endpoint URL
  - Hiểu rõ cách S3 có thể host website mà không cần server
  - Nắm vững cách viết Bucket Policy cho public access an toàn

- **Database:**

  - DB instance hoạt động biệt lập trong mạng nội bộ
  - Không thể truy cập DB trực tiếp từ Internet (đúng chuẩn bảo mật)
  - Hiểu về RDS Managed Service và lợi ích của nó

- **Kỹ năng:**

  - Đã nắm vững cú pháp JSON cho S3 Policy
  - Hiểu khái niệm "Security Group Referencing" (tham chiếu SG lồng nhau)
  - Kỹ thuật quan trọng để xây dựng kiến trúc N-tier năng động

- **Kiến trúc:**
  - Hoàn thiện mô hình "3-Tier Web Architecture" sơ khai:
    - Presentation Tier (S3)
    - Application Tier (Cloud9/EC2)
    - Data Tier (RDS)
  - Hiểu về separation of concerns trong cloud architecture
