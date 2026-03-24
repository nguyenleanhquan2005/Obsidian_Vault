**1. Tại sao phải phân tích khung ngắn (Short-time analysis)? (Câu 1, 10)**

- **Bản chất:** Tiếng nói là tín hiệu **không dừng (Non-stationary)**. Lưỡi và môi bạn di chuyển liên tục, nên phổ âm thanh thay đổi từng mili-giây. Nếu bạn lấy Fourier của cả 1 câu nói 5 giây, kết quả là một mớ hỗn độn.
- **Giải pháp:** Ta cắt tín hiệu thành các đoạn rất ngắn (thường là 20-30ms). Trong chớp mắt này, bộ máy phát âm chưa kịp cử động nhiều, ta coi tín hiệu là "tạm thời dừng" để trích xuất đặc trưng (extract temporal features over short segments). Khái niệm này gọi là **STFT (Short-Time Fourier Transform)**.

**2. Hàm Cửa sổ (Windowing) và Sự đánh đổi (Câu 5)**

- **Công thức STFT Bắt buộc:** $$X_{\hat{n}}(e^{j\hat{\omega}}) = \sum_{m=-\infty}^{\infty} x[m]w[\hat{n}-m]e^{-j\hat{\omega}m}$$ _(Trong đó: $w[\hat{n}-m]$ chính là hàm cửa sổ trượt đi trên tín hiệu)._
- **Liên hệ thực tế:** Hàm cửa sổ (như Hamming window) quyết định sự đánh đổi (trade-off) giữa độ phân giải thời gian (time resolution) và tần số (frequency resolution).
    - _Cửa sổ dài:_ Bạn thấy rõ các sóng hài (pitch) nhưng lại làm mờ mất các âm bật nhanh như chữ /t/ hay /p/.
    - _Cửa sổ ngắn:_ Bắt chính xác thời điểm phát âm /t/, nhưng phổ tần số bị nhòe. Đây chính là "Nguyên lý bất định Heisenberg" trong xử lý âm thanh!




**1. Filter Banks và Decimation (Câu 2, 24)**

- **Bản chất:** Ta không phân tích toàn bộ dải tần 0-8000Hz cùng lúc, mà dùng một băng lọc (Filter bank) để phân rã tín hiệu thành các dải băng con nhỏ hơn (subbands) (Ví dụ: 0-1000Hz, 1000-2000Hz...).
- **Maximally Decimated (Câu 2):** Khi tín hiệu bị chia thành các băng tần nhỏ hơn, theo định lý Nyquist, ta không cần giữ mức tần số lấy mẫu cũ mà có thể giảm mẫu (Downsampling/Decimation). Một Filter bank được gọi là "Maximally decimated" (Giảm mẫu tối đa) khi **Số lượng kênh lọc bằng đúng với hệ số giảm mẫu (number of channels equals the downsampling factor)**. (Kỹ thuật này là cốt lõi của chuẩn nén MP3).



**2. Bộ Lọc Số & Biên độ ngắn hạn (Câu 32, 36)**

- **Bộ lọc số - Digital Filters (Câu 36):** Mục đích chính của bộ lọc số trong hệ thống là **loại bỏ nhiễu và cải thiện độ rõ nét của tiếng nói (remove noise and improve speech clarity)**. Ví dụ, bộ lọc Anti-aliasing (Low-pass filter) luôn được đặt trước bộ A/D converter để cắt bỏ mọi dải tần vượt quá $F_{max}$.
- **Biên độ ngắn hạn - Short-time Magnitude (Câu 32):** Thay vì dùng Năng lượng (Bình phương biên độ), ta có thể dùng Trị tuyệt đối để đo cường độ âm thanh trong 1 khung: $$M_{\hat{n}} = \sum_{m=0}^{L-1} |x[\hat{n}+m] \cdot w[m]|$$ _Tại sao cái này đúng?_ Việc tính tổng các "trị tuyệt đối" (absolute values) thay vì bình phương giúp hệ thống ít bị nhạy cảm (ít bị nhiễu) hơn bởi các điểm dữ liệu dị biệt có biên độ quá lớn.


_(Bao trùm các câu: 37, 39)_

Máy tính không thể phân tích âm thanh nếu chỉ nhìn vào đồ thị sóng (waveform). Chúng ta cần đưa nó sang miền tần số, nhưng vẫn phải giữ được mốc thời gian.

**1. Sự kỳ diệu của STFT (Câu 37)**

- **Công thức BẮT BUỘC của STFT:** $$X_{\hat{n}}(e^{j\hat{\omega}}) = \sum_{m=-\infty}^{\infty} x[m]w[\hat{n}-m]e^{-j\hat{\omega}m}$$
- **Lợi ích lớn nhất:** STFT cung cấp **Biểu diễn thời gian - tần số (Time-frequency representation)**. Biến đổi Fourier thông thường (FFT) cho bạn biết _âm thanh có những tần số nào_, nhưng STFT cho bạn biết _tần số đó xuất hiện vào lúc nào_.
- **Ứng dụng:** Đây là công nghệ cốt lõi tạo ra **Spectrogram (Ảnh phổ)**. Các kỹ sư AI dùng Spectrogram làm đầu vào cho mạng Nơ-ron tích chập (CNN) để nhận diện giọng nói.



**1. Băng lọc giảm mẫu - Time-decimated filter bank (Câu 27)**

- **Vấn đề:** Phân tích tần số độ phân giải cao trên toàn dải âm thanh tốn quá nhiều tài nguyên CPU.
- **Giải pháp:** Ta chia âm thanh thành các băng tần nhỏ (ví dụ 0-1kHz, 1-2kHz). Vì dải tần đã bị thu hẹp, theo định lý Nyquist, ta có quyền **Downsampling (Giảm mẫu/Decimation)** các dải tần con này.
- **Lợi ích (Đáp án C):** Việc này giúp **giảm thiểu đáng kể khối lượng tính toán tổng thể (reduces overall computational load)**. Đây là kỹ thuật cốt lõi làm nên sự thành công của chuẩn nén MP3!
Các hệ thống AI thường trích xuất các tính năng (features) trực tiếp từ đồ thị sóng (waveform) để đưa ra quyết định nhanh.

**1. Năng lượng ngắn hạn (STE - Câu 47, 54)**

- **Công thức:** $E_{\hat{n}} = \sum_{m} (x[m] \cdot w[\hat{n}-m])^2$
- _Ý nghĩa vật lý (Câu 47):_ Nó chính là **Độ lớn/Âm lượng (Loudness)** của tiếng nói trong một khung thời gian ngắn.
- _Yếu tố quyết định (Câu 54):_ Để dùng STE phân biệt vùng Hữu thanh (Voiced - năng lượng cao) và Vô thanh (Unvoiced - năng lượng thấp), bạn **bắt buộc phải có một Giá trị Ngưỡng (Threshold value)**. Nếu năng lượng vượt qua Threshold, đó là âm Hữu thanh.

**2. Tỷ lệ qua điểm không (ZCR - Câu 49)**

- **Bản chất:** Là số lần sóng âm cắt qua trục hoành (0 Volt).
- _Tại sao ZCR cao lại là âm Vô thanh?_ Âm vô thanh (như /s/, /sh/, /f/) là âm xát, thực chất là nhiễu trắng tần số rất cao. Sóng dao động cực nhanh nên nó cắt trục hoành liên tục. Ngược lại, nguyên âm (/a/, /o/) trầm và chậm nên ZCR thấp.
