---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10: Kubernetes trên AWS - EKS (10/11 – 14/11)

Quản lý ứng dụng microservices quy mô lớn với EKS và Kubernetes.

### Mục tiêu tuần 10:

- Xây dựng API: Tạo RESTful API cho ứng dụng quản lý sách (Book Store).
- Logic Serverless: Viết các hàm Lambda thực hiện CRUD (Create, Read, Update, Delete).
- Lưu trữ NoSQL: Thiết kế bảng DynamoDB hiệu năng cao.
- Tích hợp: Kết nối API Gateway -> Lambda -> DynamoDB.

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                                                | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T10.1      | 2   | **Lambda - Basic Function:** <br> - Viết Lambda function Python xử lý business logic <br> - Cấu hình environment variables và timeout                                                    | 10/11/2025   | 10/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.2      | 2   | **DynamoDB - NoSQL Table:** <br> - Tạo DynamoDB table với Partition + Sort Key <br> - Kích hoạt Streams cho event-driven processing                                                      | 10/11/2025   | 11/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.3      | 3   | **Lambda - DynamoDB Integration:** <br> - Viết Lambda CRUD operations với boto3 <br> - Test với sample data và verify results                                                            | 11/11/2025   | 12/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.4      | 4   | **API Gateway - REST API:** <br> - Tạo REST API với multiple resources <br> - Configure Lambda proxy integration                                                                         | 12/11/2025   | 13/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.5      | 5   | **Cognito - Authentication:** <br> - Tạo Cognito User Pool làm authorizer <br> - Bảo vệ API endpoints với JWT tokens                                                                     | 13/11/2025   | 14/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.6      | 6   | **Step Functions - Workflow:** <br> - Thiết kế state machine cho complex workflow <br> - Orchestrate multiple Lambda functions                                                           | 14/11/2025   | 14/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Admin Dashboard (Phụ trách)**                                                                                                                                       |              |                 |            |                                           |
| VG10.1     | 2-3 | **Web Setup - Next.js:** <br> - Init Next.js 14 project với App Router <br> - Setup Tailwind CSS và shadcn/ui components <br> - Project structure: app/(admin), app/(staff), components/ | 10/11/2025   | 11/11/2025      | Hoàn thành | VoltGo Web Docs                           |
| VG10.2     | 4-5 | **Admin Layout:** <br> - Sidebar navigation cho admin routes <br> - Header với role-based menu <br> - Protected routes middleware                                                        | 12/11/2025   | 13/11/2025      | Hoàn thành | VoltGo Figma Design                       |
| VG10.3     | 6   | **Admin Dashboard:** <br> - Overview stats (Revenue, Users, Trips, Stations) <br> - Charts: Revenue trends, Trip analytics <br> - System health monitoring                               | 14/11/2025   | 14/11/2025      | Hoàn thành | VoltGo Web Docs                           |

### Kết quả đạt được tuần 10:

- **Sản phẩm:**

  - Một backend API hoàn chỉnh hoạt động
  - Không cần bất kỳ máy chủ nào (No EC2)
  - Truly serverless architecture

- **Hiệu năng:**

  - Tốc độ phản hồi cực nhanh (< 100ms)
  - Khả năng chịu tải hàng nghìn request/giây mặc định
  - Auto scaling không cần cấu hình

- **Chi phí:**

  - Gần như $0 trong giai đoạn phát triển
  - Nhờ Free Tier của Lambda và DynamoDB
  - Pay-per-request model

- **Kiến trúc:**
  - Hiểu về Microservices architecture
  - Event-driven programming
  - API-first design
  - NoSQL data modeling
