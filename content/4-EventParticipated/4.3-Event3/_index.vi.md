---
title: "Event 3"
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Báo cáo "AWS Cloud Mastery Series #2: Từ DevOps, IaC đến Containers & Observability"

## Mục tiêu sự kiện

- **Chuẩn hóa Tư duy:** Hiểu sâu về Chu trình Giá trị và vai trò cốt lõi của DevOps trong việc phân phối phần mềm liên tục, đáng tin cậy
- **Hiện đại hóa Hạ tầng (IaC):** Chuyển đổi từ vận hành thủ công (ClickOps) sang quản lý hạ tầng dưới dạng mã sử dụng CloudFormation, Terraform và CDK
- **Tối ưu Ứng dụng (Containerization):** Nắm vững kiến trúc và chiến lược lựa chọn nền tảng container phù hợp: App Runner, ECS hoặc EKS
- **Giám sát Toàn diện (Observability):** Xây dựng hệ thống giám sát chủ động để phát hiện lỗi và tối ưu hiệu năng sử dụng CloudWatch và X-Ray

## Diễn giả

**Chuyên gia AWS & Cloud Engineers:** Chia sẻ insights về kiến trúc hệ thống, chiến lược Platform Engineering và demo kỹ thuật chuyên sâu.

## Chi tiết Nội dung Chính

### 1. Tư duy DevOps & CI/CD Pipeline (Nền tảng)

Sự kiện bắt đầu bằng việc định nghĩa lại DevOps không chỉ là một tập hợp công cụ, mà là văn hóa tối ưu hóa chuỗi giá trị.

**Chu trình Giá trị:**

Quy trình khép kín 5 bước: **Insights & Analysis → Portfolio & Backlog → Continuous Integration → Continuous Testing → Continuous Delivery**.

**Mục tiêu Cốt lõi:** Tăng tốc độ phân phối (Speed) để đáp ứng nhu cầu thị trường nhanh hơn, đồng thời đảm bảo tính ổn định (Stability) và chất lượng của hệ thống.

**Định nghĩa lại Khái niệm CI/CD:**

- **Continuous Integration (CI):** Các nhà phát triển merge code thường xuyên (hàng ngày). Hệ thống tự động build và chạy Unit Tests. Mục tiêu là phát hiện lỗi sớm (Fail fast)
- **Continuous Delivery:** Tự động hóa quy trình triển khai đến môi trường Staging/Pre-prod. Triển khai lên Production yêu cầu phê duyệt của con người (Manual Trigger)
- **Continuous Deployment:** Tự động hóa hoàn toàn 100% từ Code Commit đến chạy trên Production (không có can thiệp thủ công)

**Chiến lược Pipeline Hiệu quả:**

- **Centralized CI:** Xây dựng hệ thống CI tập trung cho bảo mật và quản lý tài nguyên, nhưng đảm bảo khả năng Self-service cho Developers để tránh nút thắt cổ chai
- **Artifact Management:** Áp dụng nguyên tắc "Build Once, Deploy Anywhere". Source code chỉ được build một lần thành gói Binary (Artifact). Các môi trường tiếp theo (Staging, Prod) sử dụng chính xác Artifact này để triển khai, đảm bảo tính nhất quán tuyệt đối
- **Fail Fast Conditions:** Pipeline phải được cấu hình để fail ngay lập tức nếu vi phạm: Lỗi biên dịch, Vi phạm Code Style, Quét bảo mật phát hiện lỗ hổng, hoặc Tests chạy quá chậm

**Đo lường Hiệu quả (Metrics):**

- Sử dụng Heatmaps để giám sát tình trạng Pipeline của toàn tổ chức
- **Golden Metrics:** Deployment Frequency, Change Failure Rate và MTTR (Mean Time To Recovery)

### 2. Infrastructure as Code (IaC) - Từ ClickOps sang Code

Phần này đi sâu vào việc loại bỏ thói quen thủ công (ClickOps) và chuyển sang tự động hóa hạ tầng hoàn toàn.

**Vấn đề với "ClickOps":** Vận hành thủ công trên AWS Console dễ gây lỗi con người (Human Error), chậm, khó mở rộng và gây mất nhất quán giữa môi trường Dev/Prod.

**Giải pháp IaC:** Cung cấp Tự động hóa, Khả năng mở rộng, Tái tạo và Cộng tác.

**Đi sâu vào 3 Công cụ IaC Hàng đầu:**

#### 1. AWS CloudFormation (Công cụ Native):

- Sử dụng file văn bản (YAML hoặc JSON) để mô tả trạng thái mong muốn
- **Template Anatomy:** Cấu trúc bao gồm Parameters (Đầu vào động), Mappings (Xử lý sự khác biệt theo vùng - ví dụ: AMI IDs khác nhau mỗi Region), và Resources (Tài sản thực tế cần tạo)
- **Stack:** Đơn vị quản lý vòng đời tài nguyên. Xóa Stack sẽ xóa tất cả tài nguyên liên quan

#### 2. Terraform (Multi-Cloud Powerhouse):

- Công cụ mã nguồn mở, sử dụng HCL (HashiCorp Configuration Language)
- **Điểm mạnh:** Hỗ trợ đa nền tảng (Multi-cloud: AWS, Azure, GCP…)
- **Workflow:** Write (Code) → Plan (Preview changes) → Apply (Execute). Bước Plan rất quan trọng cho kiểm tra an toàn
- **State File:** Lưu trữ trạng thái thực tế của hạ tầng để đồng bộ hóa

#### 3. AWS CDK (Cloud Development Kit):

- Cho phép định nghĩa hạ tầng sử dụng ngôn ngữ lập trình (Python, TypeScript, Java…)
- **Constructs:**
  - **L1 (Cfn Resources):** Cấu hình chi tiết từng dòng (như CloudFormation)
  - **L2 (Curated):** Tự động áp dụng Best Practices và cấu hình mặc định an toàn
  - **L3 (Patterns):** Xây dựng kiến trúc phức tạp (ví dụ: VPC + ALB + ECS) chỉ trong vài dòng code

**Drift Detection:** Tính năng quan trọng để phát hiện sự không nhất quán giữa Code và Thực tế (do thay đổi thủ công "ClickOps"), giúp duy trì kỷ luật vận hành.

### 3. Containerization - Chiến lược Ứng dụng

Phân tích chuyên sâu các nền tảng điều phối container:

**Kubernetes (K8s):**

- Kiến trúc bao gồm Control Plane (API Server, etcd, Scheduler) và Worker Nodes (Kubelet, Pods)
- Mạnh mẽ và linh hoạt nhưng phức tạp để vận hành

**So sánh: Amazon ECS vs. Amazon EKS:**

- **Amazon ECS:** Đơn giản, tích hợp sâu với AWS (ALB, IAM). Phù hợp cho các team muốn giảm chi phí vận hành và triển khai nhanh
- **Amazon EKS:** Dựa trên Kubernetes chuẩn. Mạnh mẽ, hệ sinh thái khổng lồ. Phù hợp cho Doanh nghiệp, hệ thống phức tạp hoặc Hybrid-cloud

**Lựa chọn Compute:**

- **EC2 Launch Type:** Bạn quản lý servers (Patching, Scaling). Kiểm soát cao nhất nhưng nỗ lực vận hành lớn
- **AWS Fargate (Serverless):** Không cần quản lý server. AWS xử lý hạ tầng; người dùng chỉ định nghĩa CPU/RAM cho Tasks. An toàn và tiện lợi

**AWS App Runner:**

- Giải pháp "Zero-ops" cho Web Apps/APIs
- Hoàn toàn tự động từ Source Code/Image → Public URL (HTTPS) mà không cần cấu hình mạng hoặc servers

### 4. Observability - Giám sát & Tối ưu

Khép kín vòng đời phát triển với observability sâu để đảm bảo hệ thống vận hành ổn định.

**Amazon CloudWatch (Mắt & Tai của Hệ thống):**

- **Metrics:** Thu thập dữ liệu hiệu năng (CPU, Memory, Disk)
- **Logs:** Thu thập log ứng dụng tập trung. Sử dụng Logs Insights để truy vấn lỗi
- **Alarms:** Tự động kích hoạt hành động (Auto Scaling, Restart Server, Gửi Thông báo) khi ngưỡng bị vi phạm

**AWS X-Ray (Distributed Tracing):**

- Giải quyết vấn đề "tìm kim đáy bể" trong Microservices
- **Distributed Tracing:** Theo dõi hành trình của một request qua nhiều dịch vụ để xác định nút thắt cổ chai và nguyên nhân gốc rễ

**AWS Observability Best Practices:**

- Sử dụng tài nguyên AWS để tham khảo các Patterns và Recipes chuẩn
- Phân biệt rõ: **Logs** (Sự kiện rời rạc) vs. **Traces** (Hành trình kết nối)

## Trải nghiệm Sự kiện & Suy ngẫm

Tham gia chuỗi sự kiện này mang đến những thay đổi đáng kể trong nhận thức và kỹ năng kỹ thuật của tôi:

### 1. Sự chuyển dịch từ "Ops" sang "Platform Engineering"

Tôi nhận ra vai trò của DevOps hiện đại không phải là chạy theo Developers để triển khai code thủ công. DevOps là về việc kiến trúc một "Đường cao tốc" (Pipeline & Platform). Một nền tảng tốt cho phép Developers tự phục vụ tạo môi trường và triển khai code nhanh chóng, trong khi vẫn ở trong ranh giới an toàn (Governance) do đội ngũ DevOps thiết lập.

### 2. Kỷ luật Vận hành

Bài học về Artifact Management và Drift Detection là những quy tắc vàng. Trong môi trường Doanh nghiệp, tính nhất quán là quan trọng. Sự khác biệt trong quy trình build giữa các môi trường (Dev/Test/Prod) bị cấm nghiêm ngặt, và các thay đổi thủ công đối với hệ thống được quản lý bằng code phải bị cấm.

### 3. Chiến lược Lựa chọn Công cụ Thông minh

Không có công cụ "tốt nhất", chỉ có công cụ "phù hợp nhất":

- Cần sự ổn định tuyệt đối và hỗ trợ sâu nhất cho các dịch vụ AWS mới: Chọn **CloudFormation**
- Doanh nghiệp sử dụng Multi-cloud hoặc Hybrid-cloud: **Terraform** là lựa chọn tối ưu
- Đội ngũ Phát triển Lập trình mạnh cần xây dựng kiến trúc phức tạp nhanh với tái sử dụng code cao: **AWS CDK** là vũ khí mạnh nhất
- Ứng dụng Web đơn giản: Sử dụng **App Runner** thay vì lãng phí tài nguyên vận hành cụm Kubernetes

## Kết luận

Chuỗi "DevOps & IaC Mastery" cung cấp lộ trình hoàn chỉnh cho hành trình Cloud:

- **Tư duy:** Chuyển đổi từ công việc thủ công sang tự động hóa và đo lường dựa trên dữ liệu
- **Hạ tầng:** Nắm vững IaC cho hệ thống có khả năng mở rộng, tái tạo với kiểm soát drift
- **Vận hành:** Kết hợp Containerization linh hoạt và Observability sâu để đảm bảo tính ổn định hệ thống, hiệu năng cao và khả năng tự phục hồi

Đây là nền tảng kiến thức vững chắc để xây dựng hệ thống phần mềm hiện đại quy mô lớn trên AWS.
