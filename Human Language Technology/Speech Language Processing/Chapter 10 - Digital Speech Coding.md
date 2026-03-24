**3. Khử nhiễu (Noise Reduction - Câu 12)**

- Làm sao để lọc tiếng ồn quạt máy hay tiếng điều hòa ra khỏi tín hiệu? Trong DSP, phương pháp kinh điển và hiệu quả nhất là **Trừ phổ (Spectral Subtraction)**. Ta ước lượng phổ của tiếng ồn trong những đoạn "Silence" (tính bằng thuật toán ở Domain 2), sau đó lấy phổ của toàn bộ tín hiệu trừ đi phổ tiếng ồn này.
- **Sai lầm phổ biến:** Sinh viên nghĩ rằng Spectral Subtraction sẽ trả lại âm thanh trong vắt. Thực tế, phép trừ này tạo ra các dải phổ âm (negative spectrum), khi dùng hàm trị tuyệt đối để bù lại, nó gây ra hiệu ứng "Musical Noise" (tiếng nhiễu ríu rít như tiếng chim hót/nước chảy róc rách) rất đặc trưng trong các ứng dụng gọi video (như Zoom) nếu không có thuật toán làm mượt (smoothing).

**3. Thuật toán làm mượt Median (Câu 40)**

- **Bản chất:** Median Smoothing (lấy trung vị) dùng để loại bỏ các điểm nhiễu đột biến (outliers), ví dụ bộ dò Pitch bỗng nhiên nhảy vọt lên do lỗi thuật toán.
- **Thách thức (All of the above):** Nhược điểm chết người của bộ lọc Median là nó làm mất đi các chi tiết mịn, biến đồ thị thành các hình bậc thang góc cạnh ("block-like artifacts"). Do đó, kỹ sư không bao giờ dùng Median đứng một mình, mà luôn phải kết hợp với bộ lọc tuyến tính (Linear Smoother) ở phía sau để làm tròn các góc cạnh (gọi là Tukey's combination smoother).

**2. Phương pháp Bình phương Tối thiểu (Least Squares Method - Câu 41)**

- Làm sao để tìm ra bộ hệ số $\alpha_k$ tối ưu nhất? Các kỹ sư sử dụng **Phương pháp Bình phương Tối thiểu**.
- **Bản chất Toán học:** Ta muốn tổng bình phương tín hiệu lỗi (Mean-Squared Error) trong một khung $E_{\hat{n}}$ là nhỏ nhất: $$E_{\hat{n}} = \sum_{m} e^2[m] = \sum_{m} \left( s[m] - \sum_{k=1}^{p} \alpha_k s[m-k] \right)^2$$ Để $E_{\hat{n}}$ đạt cực tiểu, ta lấy đạo hàm theo từng hệ số $\alpha_k$ và cho bằng 0 ($\partial E_{\hat{n}}/\partial \alpha_k = 0$). Giải hệ phương trình tuyến tính này, ta sẽ được bộ hệ số $\alpha_k$ phản ánh chính xác cấu trúc ống phát âm của người nói.

**3. Ứng dụng nén tiếng nói (Speech Compression - Câu 42)**

- **Hiểu lầm phổ biến:** Sinh viên thường nghĩ "nén âm thanh" giống như nén file .ZIP. Không phải!
- **Sự thật (Câu 42 đúng):** LPC được dùng để nén vì thay vì phải truyền đi 8000 mẫu biên độ âm thanh mỗi giây, thuật toán chỉ truyền đi bộ hệ số $\alpha_k$, tần số Pitch và mức năng lượng $G$. Tổng cộng chỉ tốn khoảng 2400 - 9600 bps mà vẫn tái tạo (synthesize) lại được giọng nói.


**3. Tại sao không lấy mẫu với tần số cực cao? (Câu 60)**

- _Câu 60 chỉ ra nhược điểm chính:_ Tần số lấy mẫu cao (như 192kHz) đồng nghĩa với số lượng dữ liệu khổng lồ. Điều này tạo ra **gánh nặng tính toán cực lớn (increased computational load)** cho CPU/DSP chip mà lại không mang thêm giá trị thông tin ngôn ngữ (bởi giọng người chủ yếu nằm dưới 8kHz).

**3. Autocorrelation vs. AMDF trong dò Pitch (Câu 48, 53)**

- **Autocorrelation (STACF - Câu 53):** Hàm tự tương quan sử dụng phép NHÂN ($R[k] = \sum x[m]x[m+k]$). Nó dịch chuyển tín hiệu đi một độ trễ $k$, nhân và cộng lại. Mục đích chính là tìm ra các đỉnh lặp lại để **xác định tần số cơ bản (F0) của tín hiệu tuần hoàn**.
- **AMDF (Câu 48):** Hàm sai biệt biên độ trung bình sử dụng phép TRỪ ($\gamma[k] = \sum |x[m] - x[m-k]|$). Khi tín hiệu lặp lại một chu kỳ, hiệu số của chúng sẽ tiến về 0 (tạo ra một "Thung lũng" - Valley). _Mục đích của AMDF cũng là để ước lượng Pitch_.
- _Tại sao kỹ sư lại thích AMDF?_ Vì phép trừ (Subtraction) và lấy trị tuyệt đối chạy trên các chip vi điều khiển (DSP/IoT) nhanh hơn phép nhân (Multiplication) rất nhiều!


**1. Tính toán Tham số Gain (G) trong LPC (Câu 111)**

- **Công thức Tổng quát LPC Bắt buộc:** $$s[n] = \sum_{k=1}^{p} a_k s[n-k] + G \cdot u[n]$$ _(Ý nghĩa: Mẫu tiếng nói hiện tại $s[n]$ được dự đoán từ $p$ mẫu quá khứ, cộng thêm nguồn kích thích $u[n]$ được khuếch đại bởi Gain $G$)._
- **Tính $G$ như thế nào? (Đáp án B):** Để mô hình phát ra âm thanh có năng lượng bằng đúng giọng thật, tham số Gain $G$ thường được tính toán dựa trên **Hàm tự tương quan của tín hiệu tiếng nói (The autocorrelation of the speech signal)**.
    - _Công thức năng lượng lỗi (bằng $G^2$):_ $G^2 = R - \sum_{k=1}^{p} \alpha_k R[k]$ Trong đó $R[k]$ chính là các hệ số tự tương quan (autocorrelation). Việc giải phương trình Durbin-Levinson không chỉ cho ta bộ lọc $a_k$ mà còn trực tiếp cho ta tham số $G$ này!

**2. Bộ lọc Trung vị (Median Smoothing) (Câu 114)**

- **Bản chất:** Lọc trung vị là sắp xếp các giá trị trong một cửa sổ theo thứ tự từ bé đến lớn rồi lấy giá trị ở giữa.
- **Tại sao nó hiệu quả với Nhiễu xung (Impulse Noise - Đáp án A)?** Nhiễu xung là những điểm sai số nhảy vọt (outliers). Ví dụ: Thuật toán dò Pitch đang chạy mượt ở 120Hz, bỗng nhiên có một khung bị lỗi nhảy vọt lên 400Hz.
- **Lỗi sai phổ biến:** Nếu bạn dùng bộ lọc Trung bình (Linear/Mean filter), giá trị 400Hz khổng lồ này sẽ bị "cào bằng" và kéo toàn bộ đồ thị sai theo. Bộ lọc Trung vị thì khác, nó hoàn toàn phớt lờ và "vứt bỏ" con số 400Hz dị biệt đó, giữ cho đường contour pitch của giọng nói mượt mà hoàn hảo.