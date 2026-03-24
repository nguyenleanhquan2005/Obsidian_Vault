**1. Mục tiêu và Kiến trúc ASR (Câu 8, 15, 21, 23)**

- **Mục tiêu (Câu 8, 23):** DSP sinh ra để phân tích, thao tác và tổng hợp tiếng nói. Đối với ASR, mục tiêu tối thượng là dịch tiếng nói thành văn bản (Speech to Text). Các hệ thống này giao tiếp với người dùng thông qua **VUI (Voice User Interface)** (ví dụ: nói "Hey Siri").
- **Front-End Processing (Câu 9, 15):** Máy tính không "nghe" được file WAV. Khối Front-End làm nhiệm vụ tiền xử lý, trích xuất đặc trưng (Feature Extraction - như MFCC) để **tìm ra các mẫu hình có ý nghĩa (meaningful patterns)** và **chuyển đổi tín hiệu thành biểu diễn số hóa** dưới dạng vector. Đặc trưng khu biệt này (Acoustic-phonetic feature) giúp máy tính phân biệt được các âm vị khác nhau (như /b/ khác /p/).

**2. Khối Giải mã (Decoder) và Mô hình Ngôn ngữ (Câu 6)**

- Dữ liệu từ Front-End chỉ là các phổ âm thanh. Khối **Decoder (Bộ giải mã)** sẽ dùng thuật toán Viterbi kết hợp với Mô hình Ngôn ngữ (Language Model) để **áp dụng các quy tắc ngôn ngữ nhằm tạo ra văn bản mạch lạc (coherent text)**.
    - _Ví dụ:_ Front-end nghe được âm thanh giống "ai lóp diu". Decoder dùng xác suất ngôn ngữ để biết đó là "I love you" chứ không phải "Eye lob yew".


**2. Phương pháp Overlap-Add (OLA) (Câu 39)**

- **Bản chất:** Sau khi đã cắt âm thanh thành từng khung (frames), nhân với cửa sổ $w[n]$, và dùng STFT để chỉnh sửa (ví dụ: khử nhiễu, tăng giảm pitch), làm sao để ghép chúng lại thành file Audio ban đầu?
- **Cách làm đúng:** Bạn không thể cứ thế xếp chúng nối đuôi nhau. Do hiệu ứng của hàm cửa sổ (tín hiệu bị bóp nhỏ ở 2 đầu), bạn bắt buộc phải xếp chúng chồng lấp lên nhau (Overlap) rồi **Cộng các phần chồng lấp lại (Summing the overlapped segments)**. $$y[n] = \sum_{r=-\infty}^{\infty} y_r[n]$$
- **Ứng dụng:** Các phần mềm chỉnh phô giọng hát (Auto-Tune) hoạt động chính xác dựa trên thuật toán TD-PSOLA (Pitch Synchronous Overlap-Add) này!

**1. Giao diện Người dùng Giọng nói - VUI (Câu 29)**

- Trong chu trình giao tiếp tự nhiên với máy (Speech Dialog Circle), hệ thống được thiết kế đặc biệt để xử lý các lệnh bằng ngôn ngữ tự nhiên được gọi là **Voice User Interface (VUI)**. Khác với GUI (Graphic User Interface) dùng chuột và màn hình, VUI cho phép bạn nói "Siri, đặt báo thức 7h sáng mai" và máy tự hiểu.