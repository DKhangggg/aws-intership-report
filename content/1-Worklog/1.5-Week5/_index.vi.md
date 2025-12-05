---
title: "Worklog Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5: Quản lý Hệ thống và Hạ tầng dưới dạng Mã (06/10 – 10/10)

Loại bỏ thao tác thủ công, quản lý hạm đội máy chủ quy mô lớn và mã hóa hạ tầng.

### Mục tiêu tuần 5:

- VPS Nhanh: Triển khai ứng dụng WordPress hoàn chỉnh trong 5 phút sử dụng Amazon Lightsail.
- Container hóa: Đóng gói ứng dụng nhỏ thành Docker Image và triển khai trên Lightsail Container Service.
- Tính Đàn hồi: Thiết lập kiến trúc tự phục hồi (Self-healing) và tự mở rộng với EC2 Auto Scaling Group.
- Cân bằng Tải: Phân phối traffic người dùng thông qua Application Load Balancer (ALB).

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T5.1       | 2   | **SSM - Quản lý Fleet:** <br> - Cấu hình IAM Role cho EC2 với policy AmazonSSMManagedInstanceCore <br> - Sử dụng Run Command để update packages trên nhiều instance                | 06/10/2025   | 06/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.2       | 3   | **Session Manager - Truy cập An toàn:** <br> - Đóng port SSH (22) trên Security Group <br> - Truy cập EC2 qua Session Manager thay vì SSH truyền thống                             | 07/10/2025   | 07/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.3       | 4   | **CloudFormation - IaC Cơ bản:** <br> - Viết template YAML định nghĩa VPC và EC2 <br> - Tạo Stack và quan sát tài nguyên được provision tự động                                    | 08/10/2025   | 08/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.4       | 4   | **CloudFormation - Stack Management:** <br> - Thực hiện Update Stack với Change Sets <br> - Test tính năng Drift Detection để phát hiện thay đổi thủ công                          | 08/10/2025   | 09/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.5       | 5   | **AWS CDK - Khởi tạo Project:** <br> - Cài đặt AWS CDK CLI <br> - Init project TypeScript: `cdk init app --language typescript`                                                    | 09/10/2025   | 09/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.6       | 5   | **AWS CDK - Define Infrastructure:** <br> - Sử dụng L2 Construct để tạo S3 Bucket <br> - Bật versioning và encryption trong code                                                   | 09/10/2025   | 10/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.7       | 6   | **AWS CDK - Deploy & Test:** <br> - Chạy `cdk deploy` để triển khai stack <br> - Quan sát CloudFormation ChangeSet và verify resources                                             | 10/10/2025   | 10/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - React Native Setup**                                                                                                                                          |              |                 |            |                                           |
| VG5.1      | 2-6 | **Project Initialization:** <br> - Init Expo project với Expo Router <br> - Setup NativeWind (Tailwind for RN) <br> - Install dependencies: Lucide React Native, expo-secure-store | 06/10/2025   | 10/10/2025      | Hoàn thành | VoltGo Internal Docs                      |
| VG5.2      | 2-6 | **Folder Structure:** <br> - Tạo folder structure: app/(tabs), app/(auth), app/(rental), components/ <br> - Setup tsconfig với absolute imports (@/)                               | 06/10/2025   | 10/10/2025      | Hoàn thành | VoltGo Internal Docs                      |

### Kết quả đạt được tuần 5:

- **So sánh:**

  - Lightsail cực kỳ nhanh để triển khai nhưng thiếu tính tùy biến sâu về mạng
  - VPC Peering của Lightsail có hạn chế
  - Phù hợp cho các dự án nhỏ, blog, prototype

- **Hệ thống Đàn hồi:**

  - Đã xây dựng hệ thống Web có khả năng chịu lỗi (Fault Tolerant)
  - Khi Terminate 1 instance thủ công, ASG lập tức khởi tạo instance mới thay thế
  - Hệ thống tự động scale up/down theo nhu cầu

- **Cân bằng tải:**

  - ALB phân phối đều request giữa các instance
  - Đảm bảo người dùng không bị gián đoạn dịch vụ khi một máy chủ chết
  - Hiểu về Health Checks và Drain Connection

- **Kiến trúc:**
  - Nắm vững khái niệm Stateless Architecture
  - Không được lưu file upload hay session trên ổ cứng EC2
  - Kết hợp S3 (file) và RDS (dữ liệu) cho hệ thống Cloud-Native
  - User Data để Bootstrapping là kỹ thuật then chốt tự động hóa
