---
title: "Worklog Tuần 1"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu Tuần 1: Quản trị Định danh và Kiến trúc Mạng (08/09 – 12/09)

Thiết lập tài khoản AWS chuẩn doanh nghiệp và xây dựng mạng đám mây ảo (VPC) bảo mật. Đây là giai đoạn quan trọng nhất, vì các lỗi cấu hình trong giai đoạn này thường dẫn đến các lỗ hổng bảo mật và nợ kỹ thuật khó khắc phục sau này.

### Các công việc triển khai trong tuần:

| Ngày    | Công việc chính                                                                                                                                                                                                                                                                                                 | Ngày thực hiện | Trạng thái | Nguồn tài liệu                            |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ---------- | ----------------------------------------- |
| Thứ Hai | **Khởi tạo Tài khoản và Quản lý Chi phí**<br>- Khởi tạo AWS Account và bảo mật Root User với MFA<br>- Thiết lập AWS Budgets (Cost & Usage Budget)<br>- Cấu hình Amazon SNS cho cảnh báo ngân sách (80% threshold)<br>- Nghiên cứu các gói AWS Support và SLA                                                    | 08/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Ba  | **IAM - Quản lý Định danh (Phần 1)**<br>- Áp dụng nguyên tắc Đặc quyền Tối thiểu (Least Privilege)<br>- Tạo IAM User cho quản trị viên<br>- Tạo Groups: Admins, Developers, Auditors<br>- Gán Managed Policies (AdministratorAccess, PowerUserAccess)<br>- Thiết lập Account Password Policy theo CIS Benchmark | 09/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Tư  | **IAM - Quản lý Định danh (Phần 2)**<br>- Tạo IAM Role cho EC2 truy cập S3<br>- Hiểu Instance Metadata Service (IMDS)<br>- Viết Custom Policy JSON (granular permissions)<br>- Thực hành giới hạn quyền theo bucket và thời gian                                                                                | 10/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Năm | **VPC - Lý thuyết & Thiết kế**<br>- Nghiên cứu Networking Essentials with Amazon VPC<br>- Phân biệt Default VPC vs Custom VPC<br>- Quy hoạch IP: Thiết kế CIDR 10.0.0.0/16 (65,536 IPs)<br>- Thiết kế Multi-AZ: Public Subnets và Private Subnets                                                               | 11/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Sáu | **VPC - Triển khai & Bảo mật**<br>- Tạo Custom VPC, Subnets và Internet Gateway<br>- Cấu hình Route Tables và NAT Gateway<br>- Cấu hình Security Groups và NACL<br>- Áp dụng Defense in Depth                                                                                                                   | 12/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được Tuần 1:

**Hạ tầng Bảo mật:**

- Tài khoản AWS được bảo vệ bằng MFA cho Root User
- Hệ thống IAM phân cấp rõ ràng (Users, Groups, Roles)
- Áp dụng nguyên tắc Least Privilege trong mọi policy
- Password Policy tuân thủ tiêu chuẩn CIS Benchmark

**Kiến trúc Mạng:**

- Custom VPC hoàn chỉnh với CIDR 10.0.0.0/16
- Thiết kế Multi-AZ với Public và Private Subnets
- Internet Gateway và NAT Gateway được cấu hình đúng
- Route Tables phân định rõ ràng traffic flows

**Kiểm soát Truy cập:**

- Security Groups thiết lập theo mô hình nhiều lớp
- Hiểu rõ sự khác biệt giữa Security Groups (Stateful) và NACL (Stateless)
- IAM Roles cho EC2 thay vì hard-coded credentials

**Quản trị Tài chính:**

- AWS Budgets với cảnh báo tự động qua SNS
- Hiểu rõ mô hình FinOps ngay từ đầu
- Nắm vững các gói Support và SLA

**Kỹ năng Vận hành:**

- Thành thạo AWS Console cho các dịch vụ cơ bản
- Hiểu cơ chế IMDS và tạm thời credentials
- Troubleshooting mạng cơ bản
- Môi trường biệt lập, an toàn sẵn sàng cho triển khai ứng dụng

- Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
- ...
