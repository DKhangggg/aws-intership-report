---
title: "Worklog Tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6: Kiến trúc Bảo mật Đa lớp (13/10 – 17/10)

Xây dựng pháo đài số bảo vệ dữ liệu và ứng dụng trước các mối đe dọa mạng hiện đại.

### Mục tiêu tuần 6:

- Khả năng Quan sát (Observability): Xây dựng Dashboard tập trung để theo dõi sức khỏe hệ thống.
- Cảnh báo Chủ động: Thiết lập hệ thống cảnh báo qua Email/SMS khi tài nguyên gặp sự cố.
- Tự động hóa: Viết hàm Lambda (Python/Node.js) để tương tác với tài nguyên AWS.
- Lập lịch: Sử dụng Amazon EventBridge để kích hoạt Lambda theo lịch trình (Cron job).

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T6.1       | 2   | **AWS WAF - Tường lửa Ứng dụng:** <br> - Tạo Web ACL và gắn vào ALB <br> - Cấu hình rules chặn SQL Injection và XSS attacks                                           | 13/10/2025   | 13/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.2       | 2   | **WAF - Rate Limiting:** <br> - Thiết lập Rate-based rule <br> - Chặn IP gửi quá 100 requests/5 phút để chống DDoS                                                    | 13/10/2025   | 14/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.3       | 3   | **KMS - Quản lý Khóa:** <br> - Tạo Customer Managed Key (CMK) <br> - Cấu hình Key Policy để kiểm soát quyền mã hóa/giải mã                                            | 14/10/2025   | 14/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.4       | 4   | **KMS - Encryption Integration:** <br> - Bật encryption cho EBS Volume bằng CMK <br> - Kích hoạt S3 Bucket encryption với KMS key                                     | 15/10/2025   | 15/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.5       | 4   | **Secrets Manager - Setup:** <br> - Lưu trữ RDS password vào Secrets Manager <br> - Cấu hình automatic rotation với Lambda                                            | 15/10/2025   | 16/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.6       | 5   | **GuardDuty - Threat Detection:** <br> - Kích hoạt GuardDuty để phân tích CloudTrail/VPC Flow Logs <br> - Cấu hình EventBridge để gửi alert khi phát hiện threat      | 16/10/2025   | 16/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.7       | 6   | **Cognito - User Authentication:** <br> - Tạo User Pool cho ứng dụng web <br> - Test tính năng đăng ký/đăng nhập người dùng                                           | 17/10/2025   | 17/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Authentication & Core UI**                                                                                                                       |              |                 |            |                                           |
| VG6.1      | 2-3 | **Auth Screens:** <br> - Implement Login screen (NativeWind styling) <br> - Implement Register screen <br> - OTP Verification screen                                  | 13/10/2025   | 14/10/2025      | Hoàn thành | VoltGo Figma Design                       |
| VG6.2      | 4-5 | **Auth Context & Storage:** <br> - Create AuthContext với React Context API <br> - Implement SecureStore cho token management <br> - Auth guard logic in \_layout.tsx | 15/10/2025   | 16/10/2025      | Hoàn thành | VoltGo Internal Docs                      |
| VG6.3      | 6   | **Tab Navigation:** <br> - Setup 5 tabs: Explore, Messages, Trips, Support, Profile <br> - Dynamic Profile tab (Guest vs User)                                        | 17/10/2025   | 17/10/2025      | Hoàn thành | VoltGo Internal Docs                      |

### Kết quả đạt được tuần 6:

- **Tầm nhìn:**

  - Có cái nhìn thời gian thực về hiệu năng hệ thống
  - Không còn phải SSH vào từng máy để gõ lệnh `top`
  - Dashboard tập trung cho toàn bộ tài nguyên

- **Phản ứng:**

  - Nhận email cảnh báo ngay lập tức khi CPU cao
  - Đã test lại với Stress Test từ Tuần 5
  - Hệ thống cảnh báo hoạt động tốt

- **FinOps:**

  - Tự động tắt môi trường Development vào cuối ngày
  - Tiết kiệm khoảng 65% chi phí EC2 (8h thay vì 24h)
  - Lambda chạy với chi phí gần như $0

- **Kỹ năng:**
  - Viết Lambda function với Python và boto3
  - Hiểu về Event-Driven Architecture
  - Cấu hình EventBridge (CloudWatch Events)
  - Tích hợp SNS cho notification system
