---
title: "Bản đề xuất"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Hệ thống cho thuê xe điện tại điểm cố định

## Phần mềm cho thuê và trả xe điện tại các điểm cố định – Giải pháp di chuyển xanh cho đô thị thông minh

### 1. Tóm tắt điều hành

Hệ thống EV Station-based Rental System được phát triển nhằm cung cấp một nền tảng tất cả trong một cho việc thuê và quản lý xe điện. Hệ thống tích hợp việc đặt xe theo thời gian thực, thanh toán và quản lý điểm thuê thông qua giải pháp đám mây thống nhất. Ứng dụng bao gồm app di động React Native và backend Spring Boot triển khai trên AWS ECS Fargate, với PostgreSQL (RDS) và Redis (ElastiCache) để lưu trữ dữ liệu và tăng tốc độ truy xuất. Xác thực người dùng được quản lý qua Amazon Cognito, trong khi phân phối nội dung toàn cầu được tối ưu bằng CloudFront. Thiết kế theo AWS Well-Architected Framework giúp nền tảng đảm bảo khả năng mở rộng, độ sẵn sàng cao, bảo mật, đồng thời tối ưu chi phí vận hành.

### 2. Tuyên bố vấn đề

### Vấn đề hiện tại là gì?

Các dịch vụ thuê xe điện hiện nay còn phân mảnh, buộc người dùng phải sử dụng nhiều ứng dụng khác nhau để tìm, đặt và quản lý xe tại các điểm cố định. Điều này gây ra sự bất tiện, hiệu suất chậm và trải nghiệm thiếu tin cậy — người dùng thường đến các điểm thuê "không khả dụng" hoặc "ngoại tuyến", dẫn đến bức xúc và mất niềm tin.

Đối với chủ xe và nhà vận hành, việc quản lý đội xe, điều phối đơn thuê và theo dõi bảo trì thủ công gây ra nhiều bất cập, giảm hiệu quả vận hành và mất doanh thu. Hiện chưa có nền tảng thống nhất và thời gian thực kết nối người thuê, chủ xe và nhà vận hành điểm thuê.

### Giải pháp

Hệ thống cho thuê và trả xe điện tại điểm cố định hợp nhất việc thuê và trả xe vào một nền tảng đám mây duy nhất. Hệ thống được xây dựng với React Native cho di động và Spring Boot cho backend, cung cấp tính năng đặt xe theo thời gian thực, theo dõi phương tiện và tích hợp thanh toán.

Các dịch vụ AWS cốt lõi bao gồm ECS Fargate cho xử lý tính toán, RDS PostgreSQL cho lưu trữ dữ liệu, ElastiCache cho hiệu năng truy xuất nhanh, API Gateway và Cognito cho truy cập bảo mật, và CloudFront cho phân phối nội dung toàn cầu. Nền tảng hỗ trợ cả hình thức quản lý đội xe và chia sẻ xe P2P, cung cấp giao diện tập trung cho người dùng và nhà vận hành để quản lý việc thuê xe hiệu quả, an toàn và dễ mở rộng.

### Lợi ích và hoàn vốn đầu tư (ROI)

Nền tảng loại bỏ sự phân mảnh ứng dụng và thao tác thủ công, mang lại trải nghiệm thống nhất, tự động cho cả người thuê và chủ xe. Dữ liệu thời gian thực đảm bảo độ tin cậy và minh bạch về tình trạng xe và điểm thuê.

Thiết kế theo AWS Well-Architected Framework giúp tối ưu chi phí vận hành thông qua mô hình serverless, trả theo mức sử dụng, đồng thời duy trì khả năng mở rộng và độ sẵn sàng 99,99%. Trong vòng 1 tháng, nền tảng dự kiến đạt 1.000+ người dùng hoạt động hàng tháng, hợp tác với 200+ điểm thuê, và mang lại hiệu quả đáng kể về thời gian, chi phí và vận hành cho cả người dùng và nhà vận hành.

### 3. Kiến trúc giải pháp

![Kiến trúc giải pháp Volgo](/images/2-Proposal/voltgo_architecture.png)

### Dịch vụ AWS sử dụng

- **Amazon ECS Fargate**: Điều phối container serverless cho các microservices backend.
- **Amazon PostgreSQL**: Cơ sở dữ liệu quan hệ.
- **Amazon ElastiCache Serverless (Valkey)**: Lưu cache trong bộ nhớ để truy cập dữ liệu với độ trễ thấp.
- **Amazon API Gateway**: Điểm vào API REST an toàn được tích hợp qua PrivateLink.
- **Amazon Cognito**: Xác thực và phân quyền người dùng với JWT và MFA.
- **Amazon CloudFront + S3**: Phân phối nội dung toàn cầu và lưu trữ tĩnh với bảo vệ WAF.
- **Amazon CloudWatch**: Giám sát, ghi log và cảnh báo thống nhất cho tất cả các dịch vụ.
- **Amazon ACM**: Quản lý bảo mật cấp edge và chứng chỉ SSL/TLS.
- **Amazon Application Load Balancer**: Định tuyến lưu lượng chuyển tiếp đến target group
- **Amazon Location Service**: Cung cấp bản đồ và địa điểm (index) cho frontend cho phép người dùng tìm kiếm và kiểm tra trạm gần đó.
- **Amazon Bedrock**: Xử lý hỗ trợ trò chuyện người dùng cho QA và tìm trạm gần đó dựa trên vị trí của người dùng
- **Amazon EC2**: Bastion Server kết nối RDS để cấu hình extension và chạy script
- **Amazon Lambda**: Cầu nối kết nối với Bedrock để xử lý api trong QA từ người dùng
- **Amazon ECR**: Kho lưu trữ image cho ecs task

### Thiết kế thành phần

- **Frontend**: Ứng dụng web React được lưu trữ trên Amazon S3 và phân phối qua CloudFront, được bảo mật bằng chứng chỉ ACM SSL/TLS.
- **API Layer**: Amazon API Gateway cung cấp điểm cuối API công khai.
- **Compute Layer**: Amazon ECS Fargate chạy container hóa trên nhiều Availability Zones, tự động mở rộng dựa trên sử dụng CPU và bộ nhớ.
- **Database Layer**: Amazon PostgreSQL lưu trữ dữ liệu quan hệ để có tính khả dụng cao và tự động mở rộng.
- **Caching Layer**: Amazon ElastiCache Serverless (Redis) lưu cache phiên và dữ liệu đặt chỗ để giảm tải cơ sở dữ liệu và cải thiện thời gian phản hồi.
- **Authentication**: Amazon Cognito xử lý đăng ký người dùng, đăng nhập và phân quyền dựa trên JWT với hỗ trợ MFA tùy chọn.
- **Storage**: Amazon S3 quản lý tài sản tĩnh và tải lên của người dùng, chỉ có thể truy cập thông qua CloudFront qua Origin Access Control (OAC).
- **Monitoring & Security**: Amazon CloudWatch theo dõi log và chỉ số hiệu suất, trong khi AWS Secrets Manager lưu trữ thông tin xác thực an toàn với tự động xoay vòng.

### 4. Triển khai kỹ thuật

**Các giai đoạn triển khai**
Dự án này có hai phần chính—phát triển backend cục bộ và triển khai lên đám mây AWS—mỗi phần theo bốn giai đoạn chính:

- 1. Xây dựng và thiết kế kiến trúc:
     Phát triển và kiểm tra các dịch vụ backend cục bộ bằng Docker Compose, PostgreSQL và Redis. Thiết kế kiến trúc AWS serverless bao gồm ECS Fargate, Aurora Serverless, ElastiCache và API Gateway với kết nối PrivateLink. (Giai đoạn trước triển khai)
- 2. Ước tính chi phí và xác thực tính khả thi:
     Sử dụng AWS Pricing Calculator để ước tính chi phí hàng tháng của các tác vụ ECS, đơn vị dung lượng Aurora và băng thông CloudFront. Điều chỉnh quyết định thiết kế để đảm bảo hiệu quả chi phí và di chuyển suôn sẻ.
- 3. Cấu hình và triển khai hạ tầng:
     Xây dựng và triển khai hạ tầng đám mây bằng Terraform cho IaC. Cấu hình VPC, ECS, Aurora, ElastiCache, Cognito và CloudFront. Xác thực vai trò IAM, mạng và truy cập chỉ riêng tư qua VPC Endpoints.
- 4. Kiểm tra, tối ưu hóa và phát hành:
     Triển khai các dịch vụ Docker hóa lên ECS Fargate, kiểm tra luồng API Gateway → PrivateLink → NLB → ECS và xác minh kết nối cơ sở dữ liệu. Kích hoạt giám sát CloudWatch, tự động mở rộng và bảo vệ WAF. Tối ưu hóa ngưỡng mở rộng và tài liệu kiến trúc cuối cùng.

**Yêu cầu kỹ thuật**

- Backend Services:
  Các microservices Node.js hoặc Spring Boot cho Auth, Booking và Payment, được container hóa với Docker và triển khai lên ECS Fargate (2–10 tasks, tự động mở rộng).
- Database Layer:
  Amazon Aurora PostgreSQL Serverless v2 với writer và reader instances, hỗ trợ tự động mở rộng và tính khả dụng cao multi-AZ.
- Caching Layer:
  Amazon ElastiCache Serverless (Redis 7.1) để lưu cache phiên và dữ liệu được truy cập thường xuyên.
- Authentication:
  Amazon Cognito quản lý đăng ký người dùng, xác thực dựa trên JWT và MFA tùy chọn, tích hợp với API Gateway.
- Storage & Content Delivery:
  Frontend được lưu trữ trên Amazon S3 và phân phối qua CloudFront, được bảo vệ bởi AWS WAF và chứng chỉ ACM SSL/TLS.
- Secrets & Monitoring:
  AWS Secrets Manager để lưu trữ thông tin xác thực (DB, Redis, JWT keys) với xoay vòng 30 ngày. Amazon CloudWatch để ghi log, chỉ số và cảnh báo mở rộng.

### 5. Lộ trình & Mốc triển khai

**Lộ trình dự án**

- Giai đoạn 1: Nền tảng & Thiết kế (Tuần 1-2)
  - Tuần 1: Hoàn thiện phạm vi MVP (P0 User Stories), xác định user flows và phê duyệt kiến trúc AWS.
  - Tuần 2: FE Lead hoàn thiện mockups UI/UX. Backend cung cấp AWS cốt lõi (VPC, S3, ECR, Aurora).
- Giai đoạn 2: Phát triển MVP cốt lõi (Tuần 3-8)
- Tuần 3-4: Backend xây dựng User Auth (Cognito) & core APIs (API Gateway, ECS).
  - Tuần 5-6: Tất cả các nhóm (FE/BE/Mobile) xây dựng các màn hình cốt lõi (Login, Search, Details) và Booking Engine APIs.
  - Tuần 7-8: Tích hợp luồng KYC (Lambda, Textract, Rekognition) và tích hợp Payment Gateway.
- Giai đoạn 3: Kiểm tra & UAT (Tuần 9-10)
  - Tuần 9: Kiểm tra End-to-End (E2E) đầy đủ. QA được thực hiện bởi nhóm phát triển 5 người, vì không có QA chuyên dụng được phân bổ.
  - Tuần 10: Kiểm tra chấp nhận người dùng bên liên quan (UAT) và sửa lỗi quan trọng cuối cùng.
- Giai đoạn 4: Ra mắt (Tuần 11)
  - Tuần 11: Triển khai sản xuất, Go-live và giám sát Hypercare chuyên sâu qua CloudWatch.

### 6. Ước tính ngân sách

Ước tính ngân sách này dựa trên sơ đồ kiến trúc AWS được cung cấp và chiến lược khởi chạy MVP "rẻ nhất có thể", tối đa hóa việc sử dụng Free Tier.

### Chi phí hạ tầng

- Dịch vụ AWS (Ước tính hàng tháng):
  - Amazon Route 53: $0.50/tháng (1 hosted zone).
  - AWS WAF: $6.00/tháng (1 WebACL + 1 Rule + yêu cầu tối thiểu).
  - AWS S3 Standard: $0.00/tháng (Nằm trong 5GB Always Free tier).
  - Amazon CloudFront: $0.00/tháng (Nằm trong 1TB/10M request Always Free tier).
  - AWS Cognito: $0.00/tháng (Nằm trong 10,000 MAU free tier).
  - Amazon API Gateway: $0.00/tháng (Nằm trong 1M request 12-month free tier).
  - AWS Lambda: $0.00/tháng (Nằm trong 1M request Always Free tier).
  - Amazon Textract/Rekognition: $0.00/tháng (Nằm trong 12-month free tier cho KYC).
  - Application Load Balancer: $17.52/tháng (1 ALB, xử lý tối thiểu).
  - VPC Endpoint (PrivateLink): $7.30/tháng (1 Endpoint, 1 AZ, 1GB data).
  - Amazon ECS trên Fargate: ~$20.00/tháng (Giả sử 2 container tối thiểu 24/7, ví dụ: 0.25 vCPU/0.5GB RAM).
  - Amazon Aurora Serverless v2: ~$25.00/tháng (ACUs tối thiểu, được cấu hình để mở rộng gần bằng không).
  - Amazon ElastiCache Serverless: ~$10.00/tháng (Sử dụng tối thiểu).
  - Amazon CloudWatch: $0.00/tháng (Nằm trong 5GB log Always Free tier).
  - Amazon ECR: ~$0.10/tháng (Lưu trữ tối thiểu trên 500MB free tier).

Tổng: ~$86.42/tháng, ~$1,037.04/12 tháng

### 7. Đánh giá rủi ro

#### Ma trận rủi ro

- Thời gian ngừng hoạt động hệ thống: Tác động cao, xác suất trung bình.
- Lỗi đồng bộ dữ liệu (Giữa trạm & máy chủ): Tác động trung bình, xác suất cao.
- Lỗi xác minh OCR: Tác động trung bình, xác suất trung bình.
- Thiếu hụt phương tiện hoặc Pin yếu tại các trạm: Tác động cao, xác suất cao.
- Sai sót vận hành của nhân viên: Tác động trung bình, xác suất trung bình.
- Vượt chi phí: Tác động trung bình, xác suất thấp.

#### Chiến lược giảm thiểu

- Hệ thống: Sử dụng máy chủ đám mây cân bằng tải với tự động mở rộng và sao lưu dự phòng.
- Đồng bộ dữ liệu: Triển khai lưu cache ngoại tuyến và đồng bộ nền định kỳ.
- Xác minh OCR: Kết hợp nhận dạng ID dựa trên AI với tùy chọn phê duyệt thủ công.
- Quản lý phương tiện: Theo dõi theo thời gian thực trạng thái pin và phương tiện; dự đoán tái cung cấp qua phân tích.
- Vận hành nhân viên: Cung cấp đào tạo và danh sách kiểm tra kỹ thuật số để giảm lỗi con người.
- Chi phí: Thiết lập giám sát chi phí đám mây và cảnh báo tối ưu hóa.

#### Kế hoạch dự phòng

- Kích hoạt chế độ ngoại tuyến cho nhân viên trạm khi Internet không khả dụng.
- Kích hoạt máy chủ dự phòng trong trường hợp ngừng hoạt động lớn.
- Cung cấp quy trình làm việc check-in/out thủ công cho thuê xe trong thời gian ngừng hoạt động hệ thống.
- Triển khai nhóm bảo trì di động để xử lý các vấn đề về phương tiện hoặc pin tại các trạm.
- Tạm dừng hoặc giới hạn đặt chỗ một cách linh hoạt nếu nguồn cung cấp phương tiện giảm xuống dưới ngưỡng an toàn.

### 8. Kết quả kỳ vọng

#### Cải tiến kỹ thuật:

- Giám sát theo thời gian thực tất cả các trạm EV và trạng thái thuê.
- Xác minh tự động và ký hợp đồng điện tử thay thế giấy tờ thủ công.
- Bảng điều khiển tập trung cho quản trị viên để quản lý đội xe, khách hàng và nhân viên.
- Hệ thống có thể mở rộng lên 20+ trạm thuê trong giai đoạn triển khai tiếp theo.

#### Giá trị dài hạn

- Thiết lập cơ sở hạ tầng di chuyển EV đáng tin cậy cho các khu vực đô thị.
- Xây dựng nền tảng dữ liệu cho dự báo nhu cầu dựa trên AI trong tương lai.
- Cho phép tích hợp với mạng lưới đô thị thông minh và giao thông xanh.
- Phục vụ như một nền tảng có thể tái sử dụng để mở rộng sang các dự án chia sẻ EV toàn quốc.

#### Lợi ích ngắn đến trung hạn

- Tăng tốc độ giới thiệu khách hàng nhanh hơn (từ 15 phút → <5 phút).
- Tăng tỷ lệ sử dụng đội xe 30% thông qua lập lịch dựa trên dữ liệu.
- Cải thiện độ chính xác của hồ sơ thuê và đối chiếu thanh toán.
- Nâng cao sự hài lòng của người dùng thông qua đặt chỗ liền mạch và thanh toán minh bạch.
