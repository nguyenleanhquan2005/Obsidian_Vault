Một hệ thống Speech-to-Text (ASR) chuẩn hoạt động như thế nào?

**1. Mô hình HMM (Câu 50)**

- Tiếng nói là chuỗi tín hiệu thời gian với độ dài ngắn ngẫu nhiên. Để xác định các vùng Hữu thanh/Vô thanh hoặc nhận diện một âm vị, người ta không dùng các luật logic (if/else) cứng nhắc.
- Thay vào đó, thuật toán **Hidden Markov Model (HMM)** (thuộc trường phái Bayesian/Xác suất thống kê) được sử dụng rộng rãi nhất. HMM cho phép tính toán xác suất chuyển trạng thái từ vùng Âm lặng (Silence) $\rightarrow$ Vô thanh (Unvoiced) $\rightarrow$ Hữu thanh (Voiced) một cách trơn tru, dẻo dai với nhiễu môi trường.

**2. Giai đoạn Decoding (Giải mã - Câu 45)**

- Sau khi chuyển sóng âm thành các Vector đặc trưng (MFCC), máy tính vẫn chưa biết bạn nói gì. Giai đoạn khó nhất là đưa các Vector này đối chiếu với một từ điển (Lexicon) và mô hình ngôn ngữ (Language Model).
- Quá trình **khớp các từ được nói với một từ điển định sẵn** (matching spoken words to a pre-defined vocabulary) để tìm ra chuỗi từ (sentence) có xác suất cao nhất chính là **Decoding (Giải mã)**.


Chúng ta kết thúc bằng việc nhìn vào bức tranh toàn cảnh của hệ thống ASR.

**1. Ứng dụng tiêu biểu của DSP (Câu 109)**

- **Đáp án A:** Tất cả các kỹ thuật STFT, LPC, Cepstrum cuối cùng đều phục vụ cho một ứng dụng khổng lồ: **Hệ thống nhận dạng giọng nói (Voice recognition systems)**. Nó là tinh hoa của ngành Xử lý tín hiệu số (DSP).

**2. Mô hình Ngôn ngữ (Language Model) trong ASR (Câu 108)**

- **Bản chất Toán học:** Thuật toán giải mã ASR dựa trên Định lý Bayes: $$\hat{W} = \arg\max_{W} P(X|W) P(W)$$
    - $P(X|W)$: Mô hình âm học (Acoustic Model - HMM) đánh giá xác suất sóng âm $X$ khớp với từ $W$.
    - $P(W)$: **Mô hình Ngôn ngữ (Language Model)** đánh giá xác suất chuỗi từ $W$ có hợp lý trong ngữ pháp hay không.
- **Vai trò (Đáp án C):** Language model cải thiện độ chính xác bằng cách **Dự đoán xác suất của các chuỗi từ (predicting the probability of word sequences)**.
- **Liên hệ thực tế:** Nếu bạn nói "I write with a pen". Sóng âm của "write" và "right" giống hệt nhau. Acoustic model sẽ bối rối. Nhưng Language Model (N-gram) sẽ biết xác suất xuất hiện chuỗi "I write" cao gấp hàng nghìn lần "I right". Nhờ đó, ASR chọn đúng kết quả!

**3. Giao diện Đa phương thức (Multimodal UIs) (Câu 113)**

- **Bản chất:** Multimodal UI kết hợp nhận dạng giọng nói với các luồng dữ liệu khác (như ánh mắt, nét mặt, hay cử chỉ chạm trên màn hình cảm ứng).
- **Thách thức lớn nhất (Đáp án A):** Đó là việc **Đồng bộ hóa tín hiệu đầu vào từ nhiều phương thức khác nhau (Synchronizing input from multiple modalities)**.
- **Liên hệ thực tiễn:** Tưởng tượng bạn đang dùng bản đồ trên xe ô tô, bạn vừa lấy tay chỉ vào màn hình vừa nói "Dẫn đường cho tôi tới _đây_". Từ "đây" và khoảnh khắc ngón tay bạn chạm vào màn hình xảy ra trên hai phần cứng khác nhau với độ trễ (latency) khác nhau. Việc đồng bộ mốc thời gian (timestamp) để hệ thống AI hiểu rằng từ "đây" ứng với "tọa độ ngón tay" là một cơn ác mộng về mặt lập trình hệ thống.