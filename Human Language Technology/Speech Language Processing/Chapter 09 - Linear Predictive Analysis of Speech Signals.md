**2. Cốt lõi của mô hình LPC** LPC coi cổ họng con người như một ống lọc bằng nhựa (IIR filter), còn thanh quản là nguồn phát âm.

- **Công thức Tổng quát LPC Bắt buộc:** $$s[n] = \sum_{k=1}^{p} \alpha_k s[n-k] + G u[n]$$ _(Ý nghĩa: Mẫu âm thanh hiện tại $s[n]$ có thể được **dự đoán tuyến tính** bằng tổng của $p$ mẫu trong quá khứ $s[n-k]$ nhân với hệ số $\alpha_k$. Còn $G u[n]$ là nguồn kích thích (excitation) từ thanh quản)._
- **Tham số Gain ($G$) (Câu 3):** Quyết định trực tiếp đến **biên độ (amplitude)** của tín hiệu trong miền thời gian. Giọng bạn nói to hay nhỏ được quyết định bởi tham số $G$ này.

**3. Điểm Cực (Poles) và Điểm Không (Zeros) (Câu 17)**

- **Trực quan vật lý:** Khi giải phương trình Z-transform của hệ thống LPC, ta có các Poles và Zeros.
    - **Poles (Điểm cực):** Đại diện cho các tần số cộng hưởng của khoang miệng (Formants). Nó làm khuếch đại một dải âm thanh.
    - **Zeros (Điểm không):** Đại diện cho các rãnh khuyết tần số (Notches), ví dụ khi luồng khí bị khoang mũi hấp thụ bớt năng lượng.



**4. Bậc của mô hình LPC (LPC Order $p$ - Câu 25)**

- **Tại sao đáp án đúng?** Việc tăng bậc $p$ (ví dụ từ 10 lên 12 hoặc 16) cung cấp cho phương trình nhiều hệ số $\alpha_k$ hơn, từ đó bám sát phổ âm thanh thực tế hơn, giúp **cải thiện độ chính xác của biểu diễn tín hiệu (Improved accuracy)**.
- **Lỗi sai phổ biến:** Sinh viên nghĩ rằng tăng $p$ lên vô hạn (ví dụ $p=100$) là tốt nhất. Không! Nếu $p$ quá lớn, mô hình sẽ bị "Overfitting" – nó học luôn cả phổ nhiễu hoặc cấu trúc sóng hài của pitch, làm mất đi hình dáng đường bao phổ (vocal tract envelope) cần thiết.


_(Bao trùm các câu: 26, 33, 38)_

LPC (Linear Predictive Coding) là nền tảng của hầu hết các codec nén giọng nói trên điện thoại (GSM) hoặc ứng dụng gọi điện (Skype, WhatsApp). Nó không nén file audio, nó "bắt chước" cổ họng con người!

**1. Formant là gì? (Câu 38)**

- **Đáp án:** Formant chính là **tần số cộng hưởng của tuyến âm (resonance frequency of the vocal tract)**.
- **Vật lý thực tiễn:** Hãy tưởng tượng thanh quản của bạn là một cái ống nhựa. Khi bạn đổi khẩu hình miệng để phát âm chữ /A/ hay /I/, bạn đang bóp méo cái ống đó, tạo ra các dải tần số cộng hưởng khác nhau ($F_1, F_2, F_3$). LPC sinh ra là để tìm các Formant này.

**2. Tín hiệu Lỗi dự đoán (Prediction Error Signal - Câu 26)**

- **Công thức LPC cốt lõi:** LPC dự đoán mẫu âm thanh hiện tại dựa trên $p$ mẫu trong quá khứ: $$\tilde{s}[n] = \sum_{k=1}^p \alpha_k s[n-k]$$ Tín hiệu lỗi $e[n]$ chính là **Sự chênh lệch giữa tín hiệu dự đoán và tín hiệu thực tế (The difference between predicted and actual speech signals)**: $$e[n] = s[n] - \tilde{s}[n]$$
- **Bản chất Kỹ sư:** Tại sao kỹ sư lại thích tín hiệu Lỗi $e[n]$ này? Vì sau khi trừ đi phần dự đoán (chính là bộ lọc Formant), $e[n]$ sẽ trở thành một dải âm thanh "phẳng" (spectral flattening), loại bỏ hoàn toàn ảnh hưởng của khẩu hình miệng. Lúc này, $e[n]$ chính là **nguồn kích thích từ dây thanh đới**. Ta có thể dùng nó để tìm Pitch (độ cao giọng) cực kỳ chính xác!



**3. Vai trò của tham số Gain ($G$) trong LPC (Câu 33)**

- **Công thức Phục hồi (Synthesis):** $$s[n] = \sum_{k=1}^p \alpha_k s[n-k] + G \cdot u[n]$$
- **Vai trò:** Các hệ số $\alpha_k$ chỉ lo tạo hình bộ lọc (Formant/khẩu hình), còn nguồn kích thích $u[n]$ chỉ là các xung nhịp hoặc nhiễu trắng chuẩn hóa. Do đó, **Gain $G$ có nhiệm vụ điều chỉnh lại biên độ (To adjust the amplitude of the prediction error)** sao cho năng lượng của giọng nói tổng hợp phát ra to bằng đúng giọng nói gốc. Nếu không có $G$, loa của bạn sẽ phát ra tiếng nói quá bé hoặc bị rè do quá tải (clipping).
Bạn có bao giờ thắc mắc tại sao gọi điện thoại qua Zalo/Messenger tốn rất ít dung lượng mạng (khoảng 8-10 kbps) mà vẫn nghe rõ tiếng người bên kia không? Đó là nhờ kỹ thuật **LPC (Linear Predictive Coding)**.


Bạn có bao giờ thắc mắc tại sao gọi điện thoại qua Zalo/Messenger tốn rất ít dung lượng mạng (khoảng 8-10 kbps) mà vẫn nghe rõ tiếng người bên kia không? Đó là nhờ kỹ thuật **LPC (Linear Predictive Coding)**.
**1. Tín hiệu Lỗi dự báo (Prediction Error Signal - Câu 51)**

- **Công thức cốt lõi:** Trong LPC, máy tính "dự đoán" mẫu âm thanh hiện tại $\tilde{s}[n]$ bằng cách lấy tổng có trọng số của $p$ mẫu trong quá khứ: $$\tilde{s}[n] = \sum_{k=1}^{p} \alpha_k s[n-k]$$
- Tín hiệu lỗi dự báo $e[n]$ (còn gọi là residual) chính là phần chênh lệch giữa thực tế và dự đoán: $$e[n] = s[n] - \tilde{s}[n]$$ _Tại sao câu 51 lại đúng?_ "By subtracting the model output from the original signal" chính xác là phép trừ toán học $s[n] - \tilde{s}[n]$. Về mặt vật lý, $e[n]$ này đã loại bỏ hoàn toàn ảnh hưởng của khẩu hình miệng (formant), nó chính là "nguồn kích thích" tinh khiết phát ra từ dây thanh đới!

**2. Phương pháp Bình phương Tối thiểu (Least Squares Method - Câu 41)**

- Làm sao để tìm ra bộ hệ số $\alpha_k$ tối ưu nhất? Các kỹ sư sử dụng **Phương pháp Bình phương Tối thiểu**.
- **Bản chất Toán học:** Ta muốn tổng bình phương tín hiệu lỗi (Mean-Squared Error) trong một khung $E_{\hat{n}}$ là nhỏ nhất: $$E_{\hat{n}} = \sum_{m} e^2[m] = \sum_{m} \left( s[m] - \sum_{k=1}^{p} \alpha_k s[m-k] \right)^2$$ Để $E_{\hat{n}}$ đạt cực tiểu, ta lấy đạo hàm theo từng hệ số $\alpha_k$ và cho bằng 0 ($\partial E_{\hat{n}}/\partial \alpha_k = 0$). Giải hệ phương trình tuyến tính này, ta sẽ được bộ hệ số $\alpha_k$ phản ánh chính xác cấu trúc ống phát âm của người nói.

**🇬🇧 1. The Core Purpose of LPC (Q73)**

- **Concept:** Linear Predictive Coding (LPC) assumes the human vocal tract is a plastic tube. The current speech sample can be **predicted based on past samples**.
- **Math:** $\tilde{s}[n] = \sum_{k=1}^{p} \alpha_k s[n-k]$.

**🇻🇳 1. Mục đích cốt lõi của LPC (Câu 73)**

- **Giải thích:** LPC mô phỏng ống phát âm của con người. Nó cho rằng mẫu âm thanh hiện tại hoàn toàn có thể được **dự đoán dựa trên các mẫu trong quá khứ (predict future speech samples based on past samples)** thông qua một phép tổng tuyến tính.

**🇬🇧 2. Formants and Prediction Error Filter (Q62, Q80, Q84)**

- **Concept:**
    - **Formants (Q62):** These are the **resonance frequencies of the vocal tract** (tần số cộng hưởng). They are what makes an "A" sound different from an "O".
    - **Estimating Formants (Q80):** Because LPC perfectly models the vocal tract envelope by drawing a smooth curve over the spectrum, **LPC is widely used to estimate formant frequencies**.
    - **Prediction Error Filter $A(z)$ (Q84):** The filter $A(z) = 1 - \sum \alpha_k z^{-k}$ is used to subtract the predicted speech from the actual speech. Its coefficients ($\alpha_k$) are optimized to minimize the energy of the prediction error signal $e[n]$.

**🇻🇳 2. Formant và Bộ lọc Lỗi Dự báo (Câu 62, 80, 84)**

- **Giải thích:** Formant chính là **các tần số cộng hưởng của ống phát âm (resonance frequency of the vocal tract)**. Để tìm ra Formant, kỹ sư AI thường dùng **mô hình LPC (Câu 80)** vì nó vẽ ra được đường bao phổ (spectral envelope) cực kỳ mượt.
- **Bản chất Bộ lọc Lỗi Dự báo (Câu 84):** Để tìm ra các hệ số $\alpha_k$ cho LPC, ta phải tạo ra một "Prediction Error Filter" (Bộ lọc lỗi dự báo). Hệ số của bộ lọc này được tính toán (derived) dựa trên việc cực tiểu hóa tín hiệu lỗi dự báo.