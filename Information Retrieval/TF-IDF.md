**Term Frequency – Inverse Document Frequency**


Là trọng số thống kê dùng để đánh giá mức độ quan trọng của một từ đối với một văn bản nằm trong kho ngữ liệu. giúp khắc phục nhược điểm của phương pháp đếm từ thông thường bằng cách không chỉ xem xét số lần từ xuất hiện, mà còn xem xét sự phổ biến của từ đó trên toàn bộ tập dữ liệu. 

- **TF (Term Frequency - Tần suất từ):** Dùng để ước lượng tần suất xuất hiện của một từ trong một văn bản cụ thể. Từ nào xuất hiện càng nhiều trong một văn bản thì giá trị TF của nó càng cao.
Được biểu diễn dưới công thức:
$$  
TF(t, d) = \frac{f(t, d)}{\max \{ f(w, d) : w \in d \}}  
$$
- **IDF (Inverse Document Frequency - Nghịch đảo tần suất văn bản):** Dùng để ước lượng mức độ quan trọng của một từ trong toàn bộ tập văn bản. Những từ quá phổ biến và xuất hiện ở hầu hết mọi văn bản (như "và", "nhưng", "thì", "ở"...) sẽ bị giảm mức độ quan trọng. Ngược lại, những từ hiếm gặp và chỉ xuất hiện ở một vài văn bản nhất định sẽ có giá trị IDF cao, giúp phân biệt các văn bản với nhau
$$  
IDF(t, D) = \log \left( \frac{|D|}{|\{d \in D : t \in d\}|} \right)  
$$

có 7 ứng dụng chính của TF-IDF lần lượt là: 
1. **Công cụ tìm kiếm và Truy xuất thông tin (Search Engines & Information Retrieval)** TF-IDF được sinh ra như một chuẩn mực để xếp hạng kết quả tìm kiếm

2. **Phân loại văn bản (Text Classification)** TF-IDF được sử dụng làm bước trích xuất đặc trưng (feature extraction) để biến văn bản thô thành các vector số học

3. **Đo lường độ tương đồng và Hệ thống gợi ý (Document Similarity & Recommender Systems)** Bằng cách so sánh khoảng cách giữa các vector TF-IDF của các văn bản (thường dùng độ đo khoảng cách Cosine), hệ thống có thể nhận biết mức độ giống nhau giữa chúng

4. **Mô hình hóa chủ đề và Phân tích ngữ nghĩa (Topic Modeling & Semantic Analysis)** TF-IDF là bước đầu để khám phá ngữ nghĩa tiềm ẩn (latent semantics) trong văn bản

5. **Xây dựng Chatbot và Hệ thống đối thoại (Dialog Systems)** Nhiều hệ thống chatbot sử dụng TF-IDF như một công cụ tìm kiếm nội bộ để so sánh độ tương đồng giữa câu hỏi của người dùng và các tập lệnh/câu hỏi đã được đào tạo trong cơ sở dữ liệu

6. **Tóm tắt văn bản và Trích xuất từ khóa (Text Summarization & Keyword Extraction)** Bằng cách đánh giá trọng số TF-IDF, hệ thống có thể tìm ra những từ, cụm từ khóa (keyphrases) hoặc câu mang hàm lượng thông tin cốt lõi nhất của một bài viết

7. **Đo lường sự tương đồng của từ (Word Similarity)** TF-IDF cũng được sử dụng trên các ma trận thuật ngữ (term-term matrix) để tính toán sự giống nhau giữa các từ với nhau
