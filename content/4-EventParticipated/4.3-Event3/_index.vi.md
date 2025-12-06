---
title: "Event 3"
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# BÁO CÁO CHUYÊN SÂU: AWS FIRST CLOUD AI JOURNEY DAY
## CHỦ ĐỀ: CLOUD MASTERY - LÀM CHỦ GENAI TỪ NỀN TẢNG ĐẾN ỨNG DỤNG

**Thông tin sự kiện:**
- **Tên sự kiện:** AWS First Cloud AI Journey Day - Cloud Mastery
- **Ngày:** Thứ Sáu, 22/11/2025
- **Thời gian:** Cả ngày
- **Địa điểm:** Văn phòng AWS Việt Nam (Bitexco Financial Tower)
- **Ban tổ chức:** Nguyễn Gia Hưng (Mentor), Nghi Danh, Aiden Dinh, Kha Van

### 1. Tổng Quan Điều Hành

Sự kiện AWS First Cloud AI Journey Day - Cloud Mastery vừa qua đã mang đến một góc nhìn thực tiễn và dễ tiếp cận hơn về thế giới Generative AI (GenAI). Không còn là những lý thuyết xa vời, buổi chia sẻ tập trung vào cách tận dụng các dịch vụ AI mạnh mẽ hiện có của AWS để phục vụ trực tiếp cho công việc và đổi mới sáng tạo.

Không khí sự kiện diễn ra vô cùng sôi nổi với sự tham gia tích cực từ cộng đồng, từ những câu hỏi nền tảng đến các thảo luận chuyên sâu về triển khai thực tế. Sự kiện được dẫn dắt và hỗ trợ bởi đội ngũ chuyên gia tâm huyết: anh Nguyễn Gia Hưng (Mentor), cùng sự phối hợp của Nghi Danh, Aiden Dinh và Kha Van.

### 2. Phân Tích Chuyên Sâu: 4 Trụ Cột Của Ứng Dụng GenAI Hiện Đại

Dựa trên khung chương trình, nội dung chuyên môn được chia thành 4 phiên trọng điểm, đi từ tầng hạ tầng mô hình (Foundation) đến tầng ứng dụng phức tạp (Agent).

#### 2.1. Khai Phá Sức Mạnh Foundation Models trên AWS Bedrock

Đây là nền tảng cốt lõi để xây dựng bất kỳ ứng dụng GenAI nào trên AWS.

**Tiếp cận Serverless:** Phiên này làm rõ cách AWS Bedrock giúp doanh nghiệp tiếp cận các mô hình ngôn ngữ lớn (LLMs) hàng đầu (như Claude, Titan, Stable Diffusion) thông qua một API duy nhất mà không cần quản lý hạ tầng máy chủ phức tạp.

**Lựa chọn Model phù hợp:** Phân tích sự đánh đổi (trade-off) giữa tốc độ, chi phí và độ chính xác khi chọn model cho từng use-case cụ thể.

**Bảo mật dữ liệu:** Nhấn mạnh cơ chế dữ liệu của khách hàng không được dùng để train lại model public – một yếu tố then chốt cho khối doanh nghiệp.

#### 2.2. Nguyên Lý & Triển Khai RAG (Retrieval-Augmented Generation)

Để giải quyết vấn đề "ảo giác" (hallucination) của AI và cập nhật dữ liệu thời gian thực, RAG là kỹ thuật bắt buộc phải nắm vững.

**Kiến trúc RAG chuẩn:** Đi sâu vào quy trình: Ingestion (Nạp dữ liệu) -> Embedding (Mã hóa vector) -> Retrieval (Truy xuất) -> Generation (Sinh câu trả lời).

**Vector Database:** Cách tích hợp Knowledge Base để cung cấp ngữ cảnh (context) chính xác cho LLM từ dữ liệu nội bộ của tổ chức.

**Tối ưu hóa:** Các chiến lược chunking (cắt nhỏ dữ liệu) và re-ranking (xếp hạng lại kết quả tìm kiếm) để nâng cao chất lượng câu trả lời.

#### 2.3. Deep Dive: Hệ Sinh Thái Dịch Vụ AI Của AWS

Bên cạnh GenAI, việc kết hợp các dịch vụ AI truyền thống (Predictive AI) tạo nên sức mạnh tổng thể.

**Đa dạng hóa công cụ:** Khám phá các dịch vụ như Amazon Rekognition (xử lý ảnh), Amazon Transcribe (chuyển đổi giọng nói), và Amazon Polly.

**Tích hợp:** Cách kết hợp các dịch vụ này làm "giác quan" (nghe, nhìn) cho ứng dụng GenAI, giúp ứng dụng không chỉ biết "chat" mà còn biết phân tích hình ảnh và xử lý âm thanh đa phương thức.

#### 2.4. Xây Dựng Ứng Dụng AI Với AgentCore

Đây là bước tiến hóa từ Chatbot thụ động sang Agent chủ động.

**Agentic Workflow:** Hướng dẫn cách thiết kế các AI Agent có khả năng tự suy luận (reasoning), lên kế hoạch (planning) và thực thi hành động (tool use) thay vì chỉ trả lời câu hỏi.

**Orchestration:** Sử dụng AgentCore để điều phối các tác vụ phức tạp, kết nối với API bên ngoài để thực hiện công việc thực tế (ví dụ: tự động tra cứu tồn kho, đặt lịch họp, gửi email).

### 3. Tổng Hợp Chiến Lược: Bài Học Cốt Lõi

Từ nội dung sự kiện, ba định hướng chính được rút ra cho lộ trình phát triển AI:

**Thực tiễn hóa GenAI:** Chuyển dịch từ việc "chơi đùa" với prompt sang việc xây dựng hệ thống bài bản có kiểm soát (thông qua Bedrock và RAG).

**Dữ liệu là tài sản:** Sức mạnh của RAG phụ thuộc hoàn toàn vào chất lượng dữ liệu của doanh nghiệp. Việc chuẩn hóa dữ liệu (Data Cleanliness) là bước đầu tiên của hành trình AI.

**Tư duy Agent:** Tương lai của ứng dụng AI nằm ở các Agent có khả năng hành động tự chủ. Nắm vững AgentCore là nắm giữ lợi thế cạnh tranh trong làn sóng công nghệ tiếp theo.

### 4. Tóm Tắt Chính (Key Takeaways)

**Foundation Models:** Tiếp cận serverless các LLM hàng đầu thông qua AWS Bedrock với bảo mật cấp doanh nghiệp.

**Kiến trúc RAG:** Kỹ thuật thiết yếu để neo câu trả lời AI vào kiến thức tổ chức và loại bỏ ảo giác.

**Tích hợp Dịch vụ AI:** Kết hợp GenAI với các dịch vụ AI truyền thống (Rekognition, Transcribe, Polly) cho khả năng đa phương thức.

**Agentic AI:** Xây dựng các agent tự chủ với khả năng suy luận, lập kế hoạch và thực thi hành động sử dụng AgentCore.
