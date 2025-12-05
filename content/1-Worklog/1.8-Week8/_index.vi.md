---
title: "Worklog Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8: Tối ưu hóa Chi phí và Mạng Nâng cao (27/10 – 31/10)

Kiểm soát dòng tiền đám mây (FinOps) và kết nối mạng quy mô lớn.

### Mục tiêu tuần 8:

- Tự động hóa Hạ tầng: Tái tạo lại kiến trúc mạng (VPC) và máy chủ (EC2) bằng code.
- Hiểu bản chất: Nắm vững cấu trúc CloudFormation (Parameters, Resources, Outputs).
- Công cụ Hiện đại: Làm quen với AWS CDK và quy trình cdk init, cdk synth, cdk deploy.
- Quản lý Vòng đời: Thực hành xóa sạch (Destroy) và tạo lại (Deploy) toàn bộ stack trong vài phút.

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T8.1       | 2   | **Cost Explorer - Deep Dive:** <br> - Phân tích chi phí theo Service và Region <br> - Xác định top 5 services tốn kém nhất                                 | 27/10/2025   | 27/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.2       | 2   | **Compute Optimizer - Right-Sizing:** <br> - Review recommendations cho EC2 instances <br> - Áp dụng right-sizing suggestions (downgrade over-provisioned) | 27/10/2025   | 28/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.3       | 3   | **Savings Plans - Analysis:** <br> - Đánh giá Savings Plans vs Reserved Instances <br> - Mua Compute Savings Plan 1-year commitment                        | 28/10/2025   | 28/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.4       | 4   | **Budgets - Advanced Alerts:** <br> - Tạo Budget với forecast-based alerts <br> - Cấu hình SNS cho multi-threshold notifications                           | 29/10/2025   | 29/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.5       | 5   | **Transit Gateway - Hub Architecture:** <br> - Thiết lập Transit Gateway làm hub <br> - Kết nối multiple VPCs qua TGW                                      | 30/10/2025   | 30/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.6       | 5   | **TGW - Route Tables:** <br> - Cấu hình TGW Route Tables cho isolation <br> - Test connectivity giữa các VPC attachments                                   | 30/10/2025   | 31/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.7       | 6   | **Cost Optimization Report:** <br> - Tổng hợp recommendations và savings achieved <br> - Lập kế hoạch FinOps cho tháng tới                                 | 31/10/2025   | 31/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Rental Flow & QR Scanner**                                                                                                            |              |                 |            |                                           |
| VG8.1      | 2-3 | **QR Code Scanner:** <br> - Implement QR Scanner với expo-camera <br> - Request camera permission <br> - Parse QR code và extract vehicle ID               | 27/10/2025   | 28/10/2025      | Hoàn thành | VoltGo Internal Docs                      |
| VG8.2      | 4-5 | **Unlock Flow:** <br> - Vehicle preview screen before unlock <br> - Confirm unlock action <br> - API call để unlock vehicle và start trip                  | 29/10/2025   | 30/10/2025      | Hoàn thành | VoltGo API Docs                           |
| VG8.3      | 6   | **Active Trip Screen:** <br> - Real-time timer hiển thị trip duration <br> - Live cost calculation <br> - End trip button với confirmation                 | 31/10/2025   | 31/10/2025      | Hoàn thành | VoltGo Figma Design                       |

### Kết quả đạt được tuần 8:

- **Tốc độ:**

  - Có thể dựng lại toàn bộ môi trường mạng chỉ trong 2 phút chạy lệnh
  - Thay vì 30 phút click chuột thủ công
  - Giảm thiểu human errors

- **Kiểm soát:**

  - Code hạ tầng được lưu trong Git
  - Xem lại lịch sử thay đổi (Ai đã sửa Subnet? Tại sao?)
  - Code review cho infrastructure changes
  - Version control cho infrastructure

- **Trải nghiệm:**

  - CDK trực quan và viết ít code hơn CloudFormation thuần túy
  - Nhờ các Construct cấp cao (L2, L3)
  - Có type checking và autocomplete
  - Dễ test infrastructure code

- **Kỹ năng:**

  - Hiểu về Infrastructure as Code (IaC)
  - Nắm vững CloudFormation template structure
  - Thành thạo AWS CDK với TypeScript
  - Biết cách sử dụng Drift Detection

- Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  - Kiểm tra thông tin tài khoản & cấu hình
  - Lấy danh sách region
  - Xem dịch vụ EC2
  - Tạo và quản lý key pair
  - Kiểm tra thông tin dịch vụ đang chạy
  - ...

- Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
- ...
