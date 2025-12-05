---
title: "Worklog Tuần 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu Tuần 11: Kiến trúc Serverless (17/11 – 21/11)

Xây dựng hệ thống không cần quản lý server với Lambda, API Gateway và EventBridge.

### Mục tiêu tuần 11:

- Kiểm toán Kiến trúc: Đánh giá lại toàn bộ hạ tầng dựa trên AWS Well-Architected Tool.
- Quản lý Hạn mức: Kiểm tra Service Quotas và hiểu quy trình yêu cầu tăng hạn mức.
- Vệ sinh Tài nguyên: Tìm và xóa tài nguyên "mồ côi" (Orphaned resources).
- Ngân sách Nâng cao: Thiết lập AWS Budgets với cảnh báo dự báo (Forecasted breach).

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T11.1      | 2   | **EventBridge - Event-Driven:** <br> - Thiết lập EventBridge rules cho S3 events <br> - Trigger Lambda khi có object upload                                 | 17/11/2025   | 17/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.2      | 2   | **SQS - Message Queue:** <br> - Tạo SQS queue cho async processing <br> - Configure Dead Letter Queue cho failed messages                                   | 17/11/2025   | 18/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.3      | 3   | **SNS - Pub/Sub Pattern:** <br> - Thiết lập SNS topic với multiple subscribers <br> - Fan-out pattern với SQS và Lambda                                     | 18/11/2025   | 18/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.4      | 4   | **AppSync - GraphQL API:** <br> - Tạo GraphQL schema và resolvers <br> - Real-time subscriptions qua WebSocket                                              | 19/11/2025   | 19/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.5      | 5   | **X-Ray - Distributed Tracing:** <br> - Enable X-Ray cho Lambda và API Gateway <br> - Phân tích service map và performance bottlenecks                      | 20/11/2025   | 20/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.6      | 6   | **SAM - Serverless Framework:** <br> - Viết SAM template cho serverless app <br> - Deploy và test với `sam local`                                           | 21/11/2025   | 21/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Staff Dashboard (Phụ trách)**                                                                                                          |              |                 |            |                                           |
| VG11.1     | 2-3 | **Staff Layout & Auth:** <br> - Tạo staff routes riêng biệt với admin <br> - Staff login với role-based permissions <br> - Staff sidebar navigation         | 17/11/2025   | 18/11/2025      | Hoàn thành | VoltGo Web Docs                           |
| VG11.2     | 4-5 | **Staff Dashboard:** <br> - Today's tasks & assignments <br> - Station management view (limited permissions) <br> - Vehicle maintenance tracking            | 19/11/2025   | 20/11/2025      | Hoàn thành | VoltGo Web Docs                           |
| VG11.3     | 6   | **Staff Operations:** <br> - Report issue form (vehicle/station problems) <br> - Trip support (manual unlock/end trip) <br> - Customer support tickets view | 21/11/2025   | 21/11/2025      | Hoàn thành | VoltGo Web Docs                           |

### Kết quả đạt được tuần 11:

- **Báo cáo rủi ro:**

  - Well-Architected Tool chỉ ra High Risk Issue
  - Database Tuần 4 đang chạy Single-AZ
  - Nếu AZ sập, DB mất kết nối
  - Cần cân nhắc Multi-AZ cho production

- **Tối ưu:**

  - Đã xóa 2 volume EBS 10GB còn sót lại
  - Tiết kiệm khoảng $2/tháng
  - Release 1 Elastic IP không dùng
  - Tránh phí phạt $3.6/tháng

- **Nhận thức:**

  - "Kiến trúc tốt" là quá trình liên tục
  - Không phải đích đến
  - Cần review và cải thiện thường xuyên
  - Well-Architected Framework là kim chỉ nam

- **Governance:**
  - Hiểu về Service Quotas và Limits
  - Biết cách request tăng quota
  - Có thể dự báo khi cần scale
  - Proactive capacity planning
