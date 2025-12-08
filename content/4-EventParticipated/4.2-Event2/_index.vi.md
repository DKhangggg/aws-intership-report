---
title: "Event 2"
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo Workshop: "AWS Cloud Mastery Series #1: GENERATIVE AI, RAG & AWS AGENTIC AI"

## Mục tiêu sự kiện

- Nắm vững nghệ thuật Prompt Engineering để điều khiển hiệu quả các mô hình AI
- Khám phá hệ sinh thái Pretrained AI Services có sẵn trên AWS
- Hiểu sâu về việc xây dựng ứng dụng AI sử dụng RAG (Retrieval-Augmented Generation)
- Cập nhật các xu hướng mới nhất về Agentic AI và cách đưa AI Agents từ nguyên mẫu (POC) lên môi trường sản xuất sử dụng Amazon Bedrock AgentCore
- Khám phá Pipecat Framework để xây dựng trợ lý ảo dựa trên giọng nói thời gian thực

## Diễn giả

- **Lâm Tuấn Kiệt** - Sr. DevOps Engineer (FPT Software)
- **Danh Hoàng Hiếu Nghi** - AI Engineer (Renova Cloud)
- **Đinh Lê Hoàng Anh** - Cloud Engineer Trainee (First Cloud AI Journey)

## Những điểm nổi bật chính

### 1. Prompt Engineering & Foundation Models (Nền tảng cốt lõi)

Trước khi đi sâu vào các dịch vụ phức tạp, sự kiện nhấn mạnh tầm quan trọng của việc hiểu và giao tiếp với Foundation Models thông qua Amazon Bedrock.

- **Zero-shot / Few-shot Prompting:** Kỹ thuật bao gồm hướng dẫn trực tiếp hoặc cung cấp ví dụ để hướng dẫn định dạng đầu ra của mô hình
- **Chain of Thought (CoT):** Kỹ thuật quan trọng yêu cầu mô hình "suy nghĩ từng bước," cải thiện đáng kể độ chính xác cho các vấn đề logic phức tạp

### 2. Pretrained AWS AI Services (API sẵn sàng sử dụng)

Giới thiệu các API "sẵn sàng sử dụng" tích hợp các tính năng thông minh mà không cần huấn luyện mô hình:

- **Hình ảnh/Video:** Amazon Rekognition
- **Ngôn ngữ:** Amazon Translate, Comprehend, Textract (OCR)
- **Âm thanh:** Amazon Polly (Text-to-Speech), Transcribe (Speech-to-Text)

### 3. RAG - Retrieval Augmented Generation

Một quy trình giúp AI trả lời dựa trên dữ liệu doanh nghiệp, giảm thiểu ảo giác:

- **Embeddings:** Sử dụng Amazon Titan Text Embeddings V2 để vector hóa văn bản cho tìm kiếm ngữ nghĩa
- **Knowledge Bases for Amazon Bedrock:** Quy trình được quản lý hoàn toàn xử lý Chunking → Vector Store → Retrieval → Generation

### 4. Sự tiến hóa sang Agentic AI

Sự kiện giới thiệu bước tiến hóa tiếp theo của GenAI:

- **GenAI Assistants:** Tuân theo quy tắc, tự động hóa các tác vụ lặp đi lặp lại
- **GenAI Agents:** Hướng mục tiêu, xử lý phạm vi rộng hơn các tác vụ
- **Agentic AI Systems:** Hệ thống đa agent hoạt động hoàn toàn tự chủ với sự giám sát tối thiểu của con người

**"Khoảng cách từ Nguyên mẫu đến Sản xuất":** Chuyển Agents từ POC sang Production gặp nhiều trở ngại lớn liên quan đến:

- Hiệu suất & Khả năng mở rộng
- Bảo mật & Quản trị
- Độ phức tạp: Khó khăn trong quản lý Bộ nhớ, kiểm soát truy cập và kiểm toán tương tác của Agent

### 5. Amazon Bedrock AgentCore: Bắc cầu khoảng cách

Để giải quyết những thách thức này, AWS giới thiệu AgentCore - một nền tảng toàn diện để xây dựng và vận hành Agents:

**Các thành phần chính:**

- **Runtime & Memory:** Môi trường thực thi và khả năng "ghi nhớ" lịch sử tương tác/học tập
- **Identity & Gateway:** Quản lý danh tính và cổng kết nối an toàn
- **Code Interpreter:** Cho phép Agents viết và thực thi mã để xử lý dữ liệu phức tạp
- **Observability:** Công cụ giám sát và kiểm toán các hoạt động của agent

**Lợi ích:** Cho phép nhà phát triển tập trung vào logic nghiệp vụ thay vì bảo mật hạ tầng hoặc quản lý ngữ cảnh.

### 6. Pipecat: Framework cho Voice AI thời gian thực

Một framework Open Source thú vị được giới thiệu để xây dựng Trợ lý Ảo đa phương thức:

- **Tập trung:** Tối ưu hóa cho tương tác thời gian thực và streaming hội thoại

**Cơ chế Pipeline:**

1. **WebRTC Input:** Nhận tín hiệu âm thanh từ người dùng
2. **STT (Speech-to-Text):** Chuyển đổi giọng nói thành văn bản
3. **LLM Processing:** Xử lý ngôn ngữ tự nhiên để tạo phản hồi
4. **TTS (Text-to-Speech):** Chuyển đổi văn bản trở lại giọng nói
5. **Output:** Phát âm thanh trở lại người dùng với độ trễ cực thấp

## Trải nghiệm sự kiện & Suy ngẫm

Tham gia workshop này mở rộng góc nhìn của tôi từ các khái niệm cơ bản đến các công nghệ tiên tiến đang định hình tương lai của AI.

### 1. Sự chuyển dịch từ "Hỏi đáp" sang "Hành động" (Agentic AI)

Khái niệm ấn tượng nhất với tôi là Agentic AI. Trước đây, tôi chủ yếu xem AI để trò chuyện hoặc tóm tắt. Tuy nhiên, qua bài thuyết trình về AgentCore, tôi thấy một tương lai của "nhân viên ảo" có khả năng lập kế hoạch, sử dụng công cụ (như trình duyệt web hoặc trình thông dịch mã) và giải quyết quy trình công việc phức tạp mà không cần sự hỗ trợ liên tục từ con người.

### 2. Giải quyết bài toán "Production"

Tôi đồng cảm sâu sắc với cuộc thảo luận về "Khoảng cách" giữa POC và Production. Các công cụ như Amazon Bedrock AgentCore về cơ bản là chìa khóa để xây dựng niềm tin doanh nghiệp. Chúng cung cấp các lớp bảo mật cần thiết (Identity) và cơ chế kiểm soát (Observability) cho phép doanh nghiệp tự tin giao nhiệm vụ cho AI.

### 3. Tiềm năng của Voice AI với Pipecat

Demo Pipecat rất hấp dẫn. Kết hợp WebRTC với các mô hình AI để tạo ra các cuộc hội thoại mượt mà, độ trễ thấp mở ra vô số ứng dụng thực tế, chẳng hạn như tổng đài ảo thông minh, trợ lý phỏng vấn AI, hoặc gia sư ngôn ngữ thời gian thực.

## Kết luận

Workshop "Generative AI & Agentic AI on AWS" cung cấp một cái nhìn toàn cảnh có giá trị:

- **Hiện tại:** Chúng ta dựa vào RAG và Prompt Engineering để làm việc hiệu quả với dữ liệu
- **Tương lai:** Chúng ta đang bước vào kỷ nguyên của Agentic AI, nơi các Agent tự chủ sẽ chuyển đổi hoạt động kinh doanh
- **Công cụ:** Với hệ sinh thái AWS (Bedrock, AgentCore) và Frameworks (Pipecat, LangChain), các rào cản kỹ thuật đang được loại bỏ, trao quyền cho các kỹ sư biến ý tưởng đột phá thành hiện thực
