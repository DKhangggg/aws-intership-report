---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9: Công nghệ Container (03/11 – 07/11)

Triển khai ứng dụng Docker lên ECS với Fargate để tối ưu hóa và quản lý mạnh mẽ.

### Mục tiêu tuần 9:

- Minh bạch Mạng: Thu thập và phân tích lưu lượng mạng để phát hiện các kết nối bất thường.
- Truy vấn Log: Sử dụng CloudWatch Logs Insights để chạy query trên dữ liệu log khổng lồ.
- Tối ưu Chi phí: Xác định các tài nguyên đang lãng phí và thực hiện "Right Sizing".
- Phân quyền Billing: Cấu hình quyền truy cập Billing cho tài khoản IAM.

### Các công việc cần triển khai trong tuần này:

| Task ID    | Thứ | Công việc                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu                            |
| ---------- | --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------- | ----------------------------------------- |
| T9.1       | 2   | **Docker - Containerization:** <br> - Viết Dockerfile tối ưu với Multi-stage build <br> - Build image và test locally                                       | 03/11/2025   | 03/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.2       | 2   | **ECR - Image Registry:** <br> - Tạo ECR Repository <br> - Push Docker image lên ECR với tag versioning                                                     | 03/11/2025   | 04/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.3       | 3   | **ECS Fargate - Task Definition:** <br> - Định nghĩa Task với CPU/RAM requirements <br> - Cấu hình container port mappings                                  | 04/11/2025   | 04/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.4       | 4   | **ECS - Service Deployment:** <br> - Tạo ECS Cluster và Service <br> - Launch Type: Fargate (serverless containers)                                         | 05/11/2025   | 05/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.5       | 5   | **Load Balancing - ALB Integration:** <br> - Tích hợp ECS Service với Application Load Balancer <br> - Cấu hình Health Check và Target Group                | 06/11/2025   | 06/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.6       | 6   | **Auto Scaling - Container Level:** <br> - Thiết lập Service Auto Scaling dựa trên CPU <br> - Test scaling behavior khi tăng load                           | 07/11/2025   | 07/11/2025      | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Trips & Messages Tabs**                                                                                                                |              |                 |            |                                           |
| VG9.1      | 2-3 | **Trips Tab - History:** <br> - Fetch trip history từ API <br> - FlatList hiển thị past trips <br> - Trip card component với details (date, duration, cost) | 03/11/2025   | 04/11/2025      | Hoàn thành | VoltGo API Docs                           |
| VG9.2      | 4-5 | **Trip Detail Screen:** <br> - Show full trip information <br> - Map route visualization <br> - Invoice/Receipt generation                                  | 05/11/2025   | 06/11/2025      | Hoàn thành | VoltGo Figma Design                       |
| VG9.3      | 6   | **Messages Tab:** <br> - System notifications list <br> - Support chat UI skeleton <br> - Unread badge indicator                                            | 07/11/2025   | 07/11/2025      | Hoàn thành | VoltGo Figma Design                       |

### Kết quả đạt được tuần 9:

- **Điều tra số:**

  - Đã xác định địa chỉ IP nào đang cố quét port SSH
  - Phát hiện các pattern tấn công
  - Có thể trace được network path

- **Tiết kiệm:**

  - Compute Optimizer chỉ ra instances đang chạy dưới 5% CPU
  - Xác nhận t3.micro phù hợp hoặc có thể gom lại
  - Phát hiện tài nguyên không sử dụng

- **Kỹ năng:**

  - Thành thạo cú pháp query của Logs Insights
  - Kỹ năng quan trọng để xử lý sự cố nhanh
  - Hiểu về VPC Flow Logs format

- **FinOps:**
  - Biết cách phân tích chi phí theo nhiều chiều
  - Hiểu về Cost Allocation Tags
  - Có thể dự báo chi phí hàng tháng
