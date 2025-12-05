---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3: Cơ sở dữ liệu và Các dịch vụ quản lý (15/09 – 21/09)

Chuyển dịch từ việc tự quản lý cơ sở dữ liệu trên EC2 sang sử dụng các dịch vụ Managed Database (RDS, DynamoDB) để giảm tải vận hành.

### Các công việc cần triển khai trong tuần này:

| Ngày    | Công việc chính                                                                                                                                                             | Ngày thực hiện | Trạng thái | Nguồn tài liệu                            |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ---------- | ----------------------------------------- |
| Thứ Hai | **Amazon RDS - Cơ sở dữ liệu Quan hệ**<br>- Triển khai RDS với MySQL/PostgreSQL<br>- Kích hoạt Multi-AZ Deployment<br>- Hiểu Synchronous Replication và Automatic Failover  | 22/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Ba  | **RDS - Kết nối và Vận hành**<br>- Cấu hình Security Group (chỉ từ Web-SG)<br>- Tùy chỉnh Parameter Groups<br>- Automated Backups và Manual Snapshot<br>- Thực hiện Restore | 23/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Tư  | **DynamoDB - NoSQL Database**<br>- Tạo bảng Users với Partition Key<br>- Thực hành PutItem, GetItem, Query, Scan<br>- So sánh Provisioned vs On-Demand                      | 24/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Năm | **ElastiCache và HA Architecture**<br>- Triển khai Redis cluster<br>- Áp dụng Lazy Loading pattern<br>- Xây dựng kiến trúc 3-tier với ALB                                   | 25/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Sáu | **Directory Services**<br>- Tìm hiểu AWS Managed Microsoft AD<br>- Tích hợp Windows EC2 vào domain<br>- Quản lý tập trung qua GPO                                           | 26/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 3:

- **Hạ tầng hoạt động:**

  - Máy chủ Web đầu tiên đã online, có Public IP
  - Truy cập được qua SSH an toàn
  - Hiểu rõ sự khác biệt giữa các Instance Types (T3, C5, R5)

- **Bảo mật Ứng dụng:**

  - Đã chứng minh EC2 có thể truy cập S3 Buckets mà không cần `aws configure`
  - Không cần lưu Access Keys trên server
  - Áp dụng cơ chế "Temporary Credentials" thông qua IAM Role

- **Lưu trữ:**

  - Hiểu sự khác biệt giữa EBS (bền vững) và Instance Store (tạm thời)
  - Thực hành gắn và mount EBS volume
  - Biết cách format và sử dụng ổ đĩa mới

- **Khắc phục sự cố:**

  - Ban đầu gặp lỗi "Connection Timeout" khi SSH
  - Nguyên nhân: Quên thêm rule Inbound Port 22 trong Security Group
  - Đã khắc phục và rút kinh nghiệm về troubleshooting

- **Kỹ năng:**
  - Thành thạo việc khởi chạy và quản lý EC2 instances
  - Hiểu về vòng đời instance (Launch, Stop, Start, Terminate)
  - Nắm vững khái niệm Instance Profiles và IAM Roles for EC2
