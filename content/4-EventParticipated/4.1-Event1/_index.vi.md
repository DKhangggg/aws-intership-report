---
title: "Event 1"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Báo cáo "Vietnam Cloud Day 2025: Ho Chi Minh City Connect Edition for Builders (Track 1: GenAI & Data)"

## Mục đích của sự kiện

- Tìm hiểu về bảo mật trong GenAI và AI Agents để tăng cường an toàn doanh nghiệp
- Khám phá vòng đời phát triển hướng AI (AI-DLC) và cách áp dụng vào phát triển phần mềm
- Hiểu cách xây dựng nền tảng dữ liệu thống nhất được tối ưu hóa cho phân tích và AI
- Cập nhật các chiến lược và xu hướng GenAI mới nhất trên AWS

## Diễn giả

- **Jun Kai Loke** – AI/ML Specialist SA, AWS
- **Kien Nguyen** – Solutions Architect, AWS
- **Tamelly Lim** – Storage Specialist SA, AWS
- **Binh Tran** – Senior Solutions Architect, AWS
- **Taiki Dang** – Solutions Architect, AWS
- **Michael Armentano** – Principal WW GTM Specialist, AWS

## Những điểm nổi bật chính

### Nội dung chính

#### 1. Nền tảng Dữ liệu Thống nhất trên AWS cho AI & Phân tích

- Xây dựng pipeline dữ liệu end-to-end: **ingestion → storage → processing → access → governance**
- Phá vỡ rào cản trong dữ liệu, con người và quy trình; cho phép tự phục vụ & quản trị tiêu chuẩn hóa
- **Dịch vụ chính:** S3, Glue, Redshift, Lake Formation, OpenSearch, Kinesis/MSK

#### 2. Chiến lược GenAI trên AWS

- Tầm nhìn, xu hướng và lộ trình áp dụng doanh nghiệp
- **Amazon Bedrock:** lựa chọn mô hình, RAG, guardrails, tối ưu hóa chi phí/độ trễ
- **AgentCore & Amazon Nova** với hỗ trợ cho các framework (CrewAI, LangGraph, LlamaIndex…)

#### 3. Bảo mật Ứng dụng GenAI

- Rủi ro OWASP LLM; bảo mật đa lớp: **infrastructure → model → application**
- Năm trụ cột: Tuân thủ, Quyền riêng tư, Kiểm soát, Quản lý rủi ro, Khả năng phục hồi
- **Công cụ:** Bedrock Guardrails, Human-in-the-loop, Observability (OpenTelemetry)

#### 4. AI Agents – Tăng cường Năng suất

- Từ trợ lý đến hệ thống đa agent, tự động hóa với ít giám sát hơn
- **Use cases:** hỗ trợ khách hàng, BI với Amazon Q (QuickSight), tự động hóa quy trình

#### 5. Độ tin cậy & Chính xác của GenAI

- Giảm thiểu ảo giác với **Prompt Engineering, RAG, Fine-tuning**
- Quy trình RAG: **input → embedding → context → LLM → output**

#### 6. Vòng đời Phát triển Hướng AI (AI-DLC)

- **Vòng đời:** Inception → Construction → Operation
- **Tiến hóa:** AI-Assisted → AI-Driven → AI-Managed
- Triển khai với IaC, kiểm thử tự động, giám sát và quản lý rủi ro

#### 7. Amazon SageMaker – Unified Studio

- Môi trường thống nhất cho dữ liệu, phân tích và AI
- Hỗ trợ Lakehouse, governance, tích hợp Zero-ETL (S3 ↔ Redshift, Aurora, DynamoDB, RDS…)
- MLOps đầy đủ: pipelines, registry, deployment, monitoring
- Tích hợp với Bedrock & JumpStart để tăng tốc phát triển ứng dụng GenAI

## Bài học chính

### Tư duy Thiết kế

- Xây dựng hệ thống dữ liệu & AI end-to-end, loại bỏ rào cản
- Áp dụng nguyên tắc tự phục vụ và quản trị ngay từ đầu

### Kiến trúc Kỹ thuật

- Tích hợp các dịch vụ AWS (S3, Glue, Redshift, SageMaker, Bedrock…) vào nền tảng thống nhất
- Áp dụng Zero-ETL, Lakehouse, MLOps để mở rộng quy mô, quản trị và vận hành bền vững
- Tận dụng AI Agents và framework GenAI để tự động hóa quy trình và tăng năng suất

### Chiến lược

- Xác định lộ trình áp dụng GenAI cân bằng tốc độ đổi mới và chi phí
- Tập trung vào bảo mật đa lớp: infra, model, application; kết hợp guardrails & human-in-the-loop
- Ưu tiên độ tin cậy và chính xác với RAG, prompt engineering, fine-tuning

### Tư duy Phát triển Phần mềm

- Chuyển đổi từ AI-Assisted → AI-Driven → AI-Managed
- Áp dụng AI-DLC để tiêu chuẩn hóa phát triển với AI tham gia ở mọi giai đoạn

## Ứng dụng vào công việc

### Trong dự án:

- Thử nghiệm với AI Agents cho đăng ký/đăng nhập và hỗ trợ khách hàng
- Sử dụng validation/guardrails để tích hợp GenAI vào ứng dụng một cách an toàn

### Trong học tập & dự án nhóm:

- Áp dụng AI-DLC cho phân chia công việc: AI hỗ trợ tạo code/docs, nhóm review & phê duyệt
- Biết khi nào nên sử dụng Lambda (serverless) vs containers (ECS/Fargate)

### Với vai trò thực tập sinh:

- Học cách áp dụng cách tiếp cận business-first khi viết tài liệu hoặc thu thập yêu cầu
- Nhận ra tầm quan trọng của nền tảng dữ liệu vững chắc để GenAI mang lại giá trị thực

## Trải nghiệm sự kiện

Tham gia workshop "GenAI-powered App-DB Modernization" là một trải nghiệm rất có giá trị, mang đến cho em cái nhìn toàn diện về hiện đại hóa ứng dụng và cơ sở dữ liệu bằng các phương pháp và công cụ tiên tiến. Một số điểm chính:

### Học hỏi từ chuyên gia

- Các chuyên gia AWS chia sẻ xu hướng mới nhất trong GenAI, Data Foundation và Security
- Hiểu rõ hơn về cách xây dựng nền tảng dữ liệu thống nhất cho AI & Analytics
- Ấn tượng với tầm nhìn về AI Agents và tiềm năng nâng cao năng suất

### Hiểu biết Kỹ thuật thực tế

- Học cách thiết kế pipeline dữ liệu end-to-end: ingestion → storage → processing → access → governance
- Khám phá các công cụ như Amazon Bedrock, AgentCore và SageMaker Unified Studio
- Khám phá giải pháp giảm ảo giác (Prompt Engineering, RAG)
- Hiểu cách áp dụng AI-DLC để cân bằng nhiệm vụ giữa AI và con người trong phát triển phần mềm

### Công cụ & Phương pháp trong Thực tế

- Khám phá Bedrock Guardrails để đảm bảo triển khai GenAI an toàn
- Hiểu khi nào nên sử dụng serverless (AWS Lambda) vs containerization (ECS/Fargate)
- Học cách tận dụng Amazon Q cho BI (QuickSight) và hỗ trợ khách hàng

### Giao lưu & Trao đổi

- Sự kiện là cơ hội tuyệt vời để tương tác với các chuyên gia AWS và học từ các case study thực tế
- Nhận ra tầm quan trọng của cách tiếp cận business-first trong mọi quyết định công nghệ

## Kết luận chính

- **GenAI không chỉ là công cụ**, mà cần chiến lược và kiến trúc phù hợp để tạo giá trị
- **Dữ liệu và bảo mật là nền tảng**—không có chúng, AI không thể phát triển
- **AI Agents và AI-DLC** sẽ định hình lại cách chúng ta thiết kế và vận hành hệ thống
