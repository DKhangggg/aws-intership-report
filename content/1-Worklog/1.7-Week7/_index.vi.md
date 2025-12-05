---
title: "Worklog Tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7: Chiến lược Di chuyển và Khôi phục Thảm họa (20/10 – 24/10)

Chuyển đổi tải công việc từ On-Premise lên AWS và đảm bảo tính liên tục trong kinh doanh.

### Mục tiêu tuần 7:

- Bảo mật Truy cập: Loại bỏ nhu cầu sử dụng SSH Key và Port 22 bằng SSM Session Manager.
- Quản lý Tài nguyên: Tổ chức tài nguyên bằng Resource Groups và Tagging Strategy.
- Vận hành Quy mô lớn: Thực thi lệnh trên nhiều máy chủ đồng thời không cần đăng nhập từng máy.
- Vá lỗi: Tự động hóa quy trình cập nhật bản vá bảo mật.

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T7.1       | 2   | **VM Migration - Preparation:** <br> - Đánh giá VM on-premise cần migrate <br> - Chuẩn bị VM Import/Export với AWS CLI                                                                | 20/10/2025   | 20/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.2       | 2   | **Application Migration Service:** <br> - Thiết lập AWS Application Migration Service (MGN) <br> - Cài đặt Replication Agent trên source server                                       | 20/10/2025   | 21/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.3       | 3   | **Database Migration - DMS Setup:** <br> - Tạo Database Migration Service endpoints <br> - Cấu hình source và target database connections                                             | 21/10/2025   | 22/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.4       | 4   | **DMS - Replication Task:** <br> - Tạo Replication Task cho full load + CDC <br> - Monitor migration progress và data validation                                                      | 22/10/2025   | 23/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.5       | 5   | **Disaster Recovery - Backup Plan:** <br> - Thiết lập AWS Backup plan cho EC2 và RDS <br> - Cấu hình retention policy và backup window                                                | 23/10/2025   | 24/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.6       | 6   | **DR Testing - Pilot Light:** <br> - Thiết kế Pilot Light architecture <br> - Test failover scenario và RTO/RPO metrics                                                               | 24/10/2025   | 25/10/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Map & Station Features**                                                                                                                                         |              |                 |            |                                           |
| VG7.1      | 2-3 | **Explore Tab - Map View:** <br> - Integrate react-native-maps (Native) / Google Maps (Web) <br> - Request location permission với expo-location <br> - Display user current location | 20/10/2025   | 21/10/2025      | Hoàn thành | VoltGo Figma Design                       |
| VG7.2      | 4-5 | **Station Markers:** <br> - Fetch stations data từ API <br> - Render custom markers cho stations trên map <br> - Show available bikes count on marker                                 | 22/10/2025   | 23/10/2025      | Hoàn thành | VoltGo API Docs                           |
| VG7.3      | 6   | **Station Details Screen:** <br> - Bottom sheet/Modal hiển thị station info <br> - List available vehicles <br> - Navigation button to station                                        | 24/10/2025   | 24/10/2025      | Hoàn thành | VoltGo Figma Design                       |

### Kết quả đạt được tuần 7:

- **Tăng cường Bảo mật:**

  - Bề mặt tấn công (Attack Surface) giảm đáng kể
  - Không còn port quản trị nào mở ra Internet
  - Mọi phiên truy cập được log trong CloudTrail và Session Manager logs
  - Có thể ghi hình (record) phiên làm việc để audit

- **Hiệu quả Vận hành:**

  - Đã thực hiện cập nhật phần mềm cho cả Autoscaling Group chỉ với vài cú click
  - Không cần quản lý SSH keys cho từng user
  - Có thể chạy scripts trên hàng trăm servers cùng lúc

- **Tư duy:**

  - Chuyển từ "Quản lý từng máy chủ" sang "Quản lý đội hình máy chủ" (Fleet Management)
  - Hiểu về Zero Trust Network Access
  - Không cần bastion host hay VPN

- **Kỹ năng:**
  - Thành thạo SSM Session Manager
  - Hiểu về IAM Instance Profile
  - Biết cách tổ chức tài nguyên với Tags và Resource Groups
  - Sử dụng SSM Run Command cho automation
