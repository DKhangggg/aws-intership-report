---
title: "Worklog Tuần 2"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2: Điện toán và Lưu trữ Cơ bản (15/09 – 19/09)

Triển khai máy chủ ảo (EC2), hiểu về các loại hình lưu trữ (EBS, S3) và các mô hình điện toán đơn giản hóa (Lightsail).

### Các công việc triển khai trong tuần:

| Ngày    | Công việc chính                                                                                                                                                                             | Ngày thực hiện | Trạng thái | Nguồn tài liệu                            |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ---------- | ----------------------------------------- |
| Thứ Hai | **Amazon EC2 - Khởi tạo và Kết nối**<br>- Tìm hiểu Compute Essentials<br>- Phân tích Instance Types: T3, C5, R5<br>- Chọn AMI: Amazon Linux 2023<br>- Quản lý Key Pairs và SSH vào instance | 15/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Ba  | **Lưu trữ Khối (EBS) và Windows**<br>- Tạo và mount EBS volume (gp3)<br>- Triển khai Windows Server 2022<br>- Cài đặt IIS Web Server<br>- Tạo Snapshot (incremental backup)                 | 16/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Tư  | **AWS Cloud9 và S3 Cơ bản**<br>- Thiết lập Cloud9 IDE<br>- Tìm hiểu Object Storage model<br>- Cấu hình Static Website Hosting<br>- Viết Bucket Policy                                       | 17/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Năm | **S3 Nâng cao và Lightsail**<br>- Thiết lập Lifecycle Policy<br>- Bật Versioning và Encryption<br>- Triển khai WordPress trên Lightsail                                                     | 18/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| Thứ Sáu | **Container trên Lightsail**<br>- Đóng gói Node.js app thành Docker Image<br>- Push lên Lightsail Container Service<br>- Làm quen container workflow                                        | 19/09/2025     | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được Tuần 2:

**Điện toán Đám mây:**

- Nắm vững các loại EC2 Instance Types và use-cases
- Thành thạo quản lý Key Pairs và kết nối SSH/RDP
- Triển khai thành công cả Linux và Windows workloads
- Hiểu AMI và cách tùy chỉnh instances

**Lưu trữ Khối (EBS):**

- Hiểu tính bền vững của EBS tách biệt với EC2 lifecycle
- Thành thạo mount và quản lý volumes
- Nắm vững cơ chế Snapshot (incremental backup)
- Phân biệt các loại volume (gp3, io2, st1, sc1)

**Lưu trữ Đối tượng (S3):**

- Hiểu mô hình Object Storage
- Cấu hình Static Website Hosting thành công
- Viết Bucket Policies với granular permissions
- Triển khai Lifecycle Policies để tối ưu chi phí
- Áp dụng các Security Best Practices (Versioning, Encryption, Block Public Access)

**Môi trường Phát triển:**

- Sử dụng Cloud9 cho development workflow
- Loại bỏ "works on my machine" syndrome
- Truy cập an toàn mà không cần mở SSH port

**Container Cơ bản:**

- Làm quen với Docker và containerization
- Triển khai thành công ứng dụng trên Lightsail Containers
- Hiểu sự khác biệt giữa Lightsail và EC2
- Nền tảng sẵn sàng cho ECS/EKS sau này

**Kiến trúc Ứng dụng:**

- Chia tách rõ compute và storage
- Hiểu khái niệm stateless vs stateful applications
- Sẵn sàng xây dựng kiến trúc 3-tier trong tuần tiếp theo
