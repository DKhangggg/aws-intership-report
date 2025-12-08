---
title: "Event 4"
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Báo cáo: "AWS Cloud Mastery Series #3"

## Mục đích Sự kiện

Chuỗi sự kiện này không chỉ về các dịch vụ riêng lẻ mà là một hành trình trong System Thinking, giúp chuyển đổi từ quản lý hạ tầng truyền thống sang mô hình Bảo mật Cloud-Native. Các mục tiêu cốt lõi bao gồm:

- **Kết nối Cộng đồng:** Lan tỏa tinh thần học hỏi và phát triển kỹ năng thông qua AWS Cloud Clubs
- **Nền tảng Quản trị:** Quản lý quy mô với hàng trăm tài khoản AWS trong khi đảm bảo tuân thủ
- **Phòng thủ Chiều sâu:** Kết hợp bảo vệ Identity, Network và Data để loại bỏ Single Points of Failure
- **Phản ứng Tự động:** Loại bỏ độ trễ con người khỏi quy trình phản ứng sự cố

## Danh sách Diễn giả

Sự kiện tập hợp các chuyên gia hàng đầu từ cộng đồng AWS, bao gồm AWS Community Builders, Cloud Engineers và các thành viên cốt lõi của chương trình First Cloud Journey:

- **Đại diện AWS Cloud Clubs:** Captains từ HCMUTE, SGU, PTIT, HUFLIT (Lê Vũ Xuân An, Trần Đức Anh, Trần Doãn Công Lý, Danh Hoàng Hiếu Nghi)
- **Identity & Governance:** Huỳnh Hoàng Long, Đinh Lê Hoàng Anh (AWS Community Builders)
- **Detection & Monitoring:** Trần Đức Anh, Nguyễn Tuấn Thịnh, Nguyễn Đỗ Thành Đạt
- **Network Security:** Kha Văn (Cloud Security Engineer | AWS Community Builder)
- **Data Protection:** Thịnh Lâm, Việt Nguyễn
- **Incident Response:** Mendel Grabski (Long) - ex Head of Security & DevOps, Tĩnh Trương - Platform Engineer

## Nội dung Chi tiết

### PHẦN 1: KICK-OFF - AWS CLOUD CLUBS & CƠ HỘI

Hành trình bắt đầu với việc giới thiệu AWS Cloud Clubs, nơi nuôi dưỡng tài năng Cloud tương lai.

#### 1. Tầm nhìn:

- Trao quyền cho sinh viên khám phá và phát triển kỹ năng điện toán đám mây
- Phát triển lãnh đạo kỹ thuật và xây dựng kết nối toàn cầu

#### 2. Lợi ích Cốt lõi:

- **Xây dựng Kỹ năng:** Học thông qua các dự án thực hành, truy cập voucher thi AWS và tài khoản Udemy
- **Xây dựng Cộng đồng:** Kết nối với các chuyên gia AWS và diễn giả trong ngành
- **Xây dựng Cơ hội:** Nâng cao portfolio cá nhân, nhận AWS credits và hỗ trợ nghề nghiệp

#### 3. Hành trình Badging:

- Lộ trình phát triển được gamify hóa cho các thành viên Core Team và Captains
- Các cấp độ từ Bronze, Silver, Gold, Platinum đến Diamond
- **Phần thưởng:** AWS Credits ($200+), Certification Vouchers, Swag kits độc quyền và pre-approval cho Student Community Day

### PHẦN 2: NỀN TẢNG IDENTITY & GOVERNANCE

Bảo mật trong Cloud bắt đầu với việc kiểm soát "Ai có thể làm gì".

#### 1. Tư duy IAM Hiện đại:

- **Identity First:** Trong môi trường Cloud, Identity là tường lửa mới
- **Credential Spectrum:** Chuyển đổi tuyệt đối từ Long-term Credentials (Permanent Access Keys - rủi ro cao) sang Short-term Credentials (STS tokens - an toàn, tự động hết hạn)
- **Least Privilege:** Áp dụng quyền tối thiểu cần thiết. Tránh sử dụng \* trong Policies trừ khi thực sự cần thiết

#### 2. Governance ở Quy mô với AWS Organizations:

- **Cấu trúc Phân cấp:** Chia tổ chức thành các Organizational Units (OUs) như Security, Shared Services, Workloads (Prod/Dev) để cô lập rủi ro
- **Service Control Policies (SCPs):** Đây là "Hiến pháp" của tổ chức. SCPs thiết lập Guardrails chặn các hành động nguy hiểm (ví dụ: cấm tắt CloudTrail, hạn chế Regions) mà ngay cả tài khoản Admin cũng không thể vượt qua

### PHẦN 3: VISIBILITY & DETECTION

Bạn không thể bảo vệ những gì bạn không thể nhìn thấy.

#### 1. Amazon GuardDuty - Trinh sát Thông minh:

- Sử dụng Machine Learning để phát hiện bất thường từ 3 nguồn dữ liệu nền tảng: CloudTrail (management events), VPC Flow Logs (network traffic) và DNS Logs (domain queries)
- **Runtime Monitoring:** Tính năng nâng cao nhìn "sâu" vào bên trong hệ điều hành (qua Agent nhẹ) để phát hiện các process lạ, sửa đổi file hoặc hành vi leo thang đặc quyền

#### 2. AWS Security Hub - Trung tâm Chỉ huy:

- Giải quyết vấn đề "mệt mỏi cảnh báo" sử dụng ASFF (AWS Security Finding Format). Nó chuẩn hóa cảnh báo từ GuardDuty, Inspector và Macie thành một ngôn ngữ JSON duy nhất
- Đóng vai trò như công cụ Cloud Security Posture Management (CSPM), tự động kiểm tra xem hệ thống có tuân thủ các tiêu chuẩn CIS, PCI-DSS không

### PHẦN 4: NETWORK SECURITY

Xây dựng một "Pháo đài Kỹ thuật số" với chiến lược phòng thủ chiều sâu từ rìa đến lõi.

#### 1. Kiểm soát Cơ bản (VPC Fundamentals):

- **Security Groups (Stateful):** Áp dụng Micro-segmentation. Thay vì whitelist địa chỉ IP (dễ thay đổi), sử dụng Security Group Referencing (ví dụ: SG-DB chỉ cho phép traffic từ SG-App)
- **NACLs (Stateless):** Hoạt động như lớp lọc thô ở biên Subnet, dùng để chặn IP blacklist hoặc subnet không tin cậy

#### 2. Phòng thủ Nâng cao (Advanced Filtering):

- **DNS Firewall (Route 53 Resolver):** Chặn kết nối đến máy chủ Command & Control (C2) ngay tại bước phân giải tên miền. Đây là điểm nghẽn quan trọng chống lại malware (như case study Mélofée)
- **AWS Network Firewall:** Tường lửa thế hệ mới với khả năng Deep Packet Inspection (DPI)
  - **Stateless Engine:** Lọc nhanh dựa trên 5-tuple (IP/Port)
  - **Stateful Engine:** Sử dụng quy tắc tương thích Suricata cho Intrusion Prevention (IPS) và Domain filtering (FQDN) cho Egress traffic

#### 3. Kiến trúc Network Hiện đại:

- Sử dụng AWS Transit Gateway với tích hợp Native Network Firewall để đơn giản hóa mô hình mạng, loại bỏ độ phức tạp của việc định tuyến qua "Inspection VPC"
- Áp dụng Active Threat Defense: Tự động đồng bộ danh sách IP độc hại từ GuardDuty sang Network Firewall để chặn ngay lập tức mà không cần can thiệp thủ công

### PHẦN 5: DATA PROTECTION

Dữ liệu là tài sản tối thượng phải được bảo vệ bằng mã hóa.

#### 1. Envelope Encryption:

Hiểu cơ chế AWS KMS: Master Key (nằm trong HSM) mã hóa Data Key, và Data Key là thứ mã hóa dữ liệu thực tế. Cơ chế này đảm bảo hiệu năng cao và bảo mật tuyệt đối.

#### 2. Secrets Management:

- **Vấn đề:** Hardcode mật khẩu trong source code là lỗi cơ bản nhưng phổ biến
- **Giải pháp:** Sử dụng AWS Secrets Manager để lưu trữ và quan trọng hơn, Automatic Rotation của Database passwords sử dụng Lambda. Ứng dụng luôn lấy mật khẩu mới nhất qua API

#### 3. Infrastructure Encryption:

Sử dụng AWS Nitro System: Các tác vụ mã hóa được offload sang phần cứng chuyên dụng (Nitro Cards), cho phép mã hóa dữ liệu mà không ảnh hưởng đến hiệu năng CPU của máy chủ host (Zero Performance Impact).

### PHẦN 6: INCIDENT RESPONSE

Khi các lớp phòng thủ bị xuyên thủng, quy trình phản ứng quyết định mức độ thiệt hại.

#### 1. Chiến lược Phòng ngừa (Sleep Better):

- **Golden Rules:** Loại bỏ SSH/Keys sống lâu, Chặn Public S3 access, Mặc định Private Subnets
- **Infrastructure as Code (IaC):** Bắt buộc mọi thay đổi hạ tầng qua Code (Terraform/CDK) và quy trình phê duyệt (PR Review), hoàn toàn loại bỏ thay đổi thủ công (ClickOps) gây configuration drift

#### 2. Quy trình 5 Bước Chuẩn:

1. **Preparation:** Chuẩn bị sẵn công cụ và Playbooks
2. **Detection:** Dựa vào CloudTrail và GuardDuty
3. **Containment:** "Nhốt" tài nguyên bị nhiễm bằng cách thay đổi Security Groups hoặc thu hồi quyền IAM
4. **Eradication & Recovery:** Loại bỏ malware, khôi phục từ backup sạch
5. **Post-Incident:** Rút kinh nghiệm

#### 3. Automation là Vua:

Con người không thể chạy đua với tốc độ máy móc. Các bài lab thực hành chứng minh sự cần thiết của việc sử dụng EventBridge + Lambda để tự động cô lập EC2 instance bị xâm nhập hoặc tự động khắc phục S3 bucket public trong vài giây.

## Kết luận

Chuỗi "Cloud Security & Operations Mastery" đã cung cấp cái nhìn toàn diện về xây dựng hệ thống an toàn trên AWS thông qua các trụ cột chính:

- **Governance & Identity:** Nền tảng của mọi hệ thống bảo mật bắt đầu với quản lý người dùng chặt chẽ và chính sách tổ chức
- **Network & Monitoring:** Thiết lập các lớp phòng thủ chiều sâu và khả năng hiển thị toàn diện để phát hiện các mối đe dọa tiềm ẩn
- **Data & Response:** Bảo vệ tài sản kỹ thuật số bằng mã hóa và sẵn sàng quy trình phản ứng sự cố tự động để đảm bảo tính liên tục của dịch vụ
