---
tags:
  - machine-learning
status: "⬜ chưa học"
created: 2025-01-01
---

# Time Series Forecasting

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Nội dung

*(Bổ sung khi học)*
Chào bạn! Rất tinh mắt. Mặc dù ở phần trước tôi đã lướt qua câu hỏi này, nhưng dưới góc độ của một **Senior AI Engineer**, đây thực sự là một câu hỏi "bẫy" cực kỳ kinh điển trong các buổi phỏng vấn vị trí Data Scientist hoặc Time Series Forecasting.

Nó chạm đến phần cốt lõi nhất của Xử lý tín hiệu số (DSP) và Học máy: **Làm sao để tách nhiễu và những chu kỳ lặp lại ra khỏi tín hiệu gốc?**

Dưới đây là bản "giải phẫu" toàn diện cho câu hỏi này dựa trên các tài liệu chuyên sâu của bạn.

---

### Câu hỏi 3: How can seasonality be addressed in time series analysis?

_(Làm thế nào để xử lý tính mùa vụ trong phân tích chuỗi thời gian?)_

**Đáp án của chuyên gia:** Phụ thuộc vào trường phái bạn đang sử dụng:

- Nếu theo **Trường phái Thống kê & Xử lý tín hiệu (DSP/Statistical)**: Đáp án là **B. By using a rolling mean to smooth the data** (Sử dụng trung bình trượt để làm mượt dữ liệu) kết hợp với Differencing (Lấy sai phân),.
- Nếu theo **Trường phái Học máy Truyền thống (Tabular Machine Learning)**: Đáp án là **C. By incorporating dummy variables for each season** (Thêm biến giả cho từng mùa),.

Trong phần lớn các bài thi trắc nghiệm căn bản, **B** hoặc **C** đều được chấp nhận tùy vào bối cảnh câu hỏi trước đó. Tuy nhiên, chúng ta sẽ mổ xẻ bản chất toán học của cả hai để bạn thực sự làm chủ hệ thống.

---

### 1. Bản chất Vật lý & Toán học của Tính mùa vụ (Seasonality)

Bất kỳ dữ liệu chuỗi thời gian nào (chứng khoán, lượng khách mua hàng, lưu lượng truy cập web) đều tuân theo phương trình phân rã (Decomposition) cơ bản,: $$ Y_t = Trend_t + Seasonality_t + Cyclic_t + Noise_t $$

Mùa vụ (Seasonality) là những biến động lặp đi lặp lại với một tần số cố định. Trong một hệ thống Học máy, sự lặp lại này phá vỡ **Tính dừng (Stationarity)** – tức là kỳ vọng và phương sai của chuỗi bị thay đổi liên tục theo thời gian,. Nếu nhồi trực tiếp $Y_t$ vào mô hình, mạng Nơ-ron sẽ bị "mù" và chỉ học thuộc lòng nhiễu thay vì quy luật thực sự.

---

### 2. Giải phẫu các phương án (Tại sao đúng, tại sao sai?)

#### Tại sao B đúng? (Góc nhìn Xử lý Tín hiệu & Thống kê)

**Option B: By using a rolling mean to smooth the data.** Đây là kỹ thuật cốt lõi trong slide của bạn-. Phương pháp Simple Moving Average (SMA - Trung bình trượt) có công thức: $$ SMA_t = \frac{X_{t-1} + X_{t-2} + ... + X_{t-n}}{n} $$

- **Bản chất Vật lý (Liên hệ với DSP):** SMA thực chất là một **Bộ lọc thông thấp (Low-pass filter)**. Khi bạn kéo một "cửa sổ trượt" (rolling window) có độ dài $n$ bằng chính xác chu kỳ của mùa vụ (ví dụ $n=365$ cho dữ liệu năm, hoặc $n=12$ cho dữ liệu tháng), hàm tổng sẽ **triệt tiêu hoàn toàn các sóng lặp lại** (sóng tần số cao), để lại một đường thẳng mượt mà chỉ chứa Xu hướng dài hạn (Trend).
- Tuy nhiên, kỹ sư bậc thầy sẽ không chỉ dùng Smoothing. Họ kết hợp nó với **Differencing (Sai phân)**,: $$ Y'_t = Y_t - Y_{t-n} $$ Bằng cách trừ thẳng giá trị hiện tại cho giá trị của chu kỳ trước (ví dụ $t-365$), bạn xóa sổ vĩnh viễn mùa vụ ra khỏi phương trình để hệ thống đưa về trạng thái ổn định (Stationarity),. Khi dự báo xong, ta mới làm thao tác **Khôi phục (Restoring)** bằng cách cộng ngược lại: $Forecast = SMA_{diff} + Y_{t-365}$.

#### Tại sao C đúng? (Góc nhìn Kỹ nghệ Đặc trưng - Feature Engineering)

**Option C: By incorporating dummy variables for each season.** Trong slide của bạn có đề cập đến "Machine Learning Regression Models" (Linear Regression, Random Forest, Gradient Boosting) và "Feature Engineering".

- Các mô hình dạng bảng (Tabular) như Random Forest không hiểu được "thứ tự thời gian" một cách tự nhiên như mạng RNN/LSTM.
- Để mô hình hiểu được Mùa vụ, ta phải dùng **One-hot Encoding** (Dummy Variables) để giải thích cho nó. Ví dụ: Tạo 12 cột cho 12 tháng. Cột `Tháng_12` = 1, các cột khác bằng 0. Toán học tuyến tính của mô hình lúc này sẽ trở thành: $$ \hat{Y} = W_1X_1 + ... + W_{Thang_12}(1) + b $$ Lúc này, trọng số $W_{Thang_12}$ sẽ đóng vai trò trực tiếp là mức độ bùng nổ doanh số của tháng 12, mô hình xử lý tính mùa vụ một cách hoàn hảo.

#### Tại sao A và D sai lầm nghiêm trọng?

- **A (Removing all time-dependent features):** Dữ liệu Time Series được định nghĩa bởi sự phụ thuộc thời gian (Dependency on Time). Xóa bỏ nó đi thì dữ liệu trở thành các điểm I.I.D rời rạc vô nghĩa.
- **D (Dimensionality reduction):** Kỹ thuật này (như PCA, SVD mà bạn có trong giáo trình Machine Learning cơ bản-) dùng để triệt tiêu các "đặc trưng không gian" dư thừa (VD: giảm từ 3000 pixel ảnh xuống 100 thành phần chính), hoàn toàn không thể dùng để xử lý sóng lặp lại trên trục thời gian của một chiều dữ liệu.

---

### 3. Sai lầm phổ biến của Kỹ sư mới (Junior Mistakes)

**1. Data Leakage (Rò rỉ dữ liệu) khi làm mượt (Smoothing):** Slide của bạn chỉ ra cực kỳ tinh tế sự khác biệt giữa **Trailing Window** (Cửa sổ kéo đuôi) và **Centered Window** (Cửa sổ căn giữa).

- Nhiều Junior dùng hàm `pandas.rolling(window=12, center=True).mean()` để lấy trung bình mượt. Lỗi chí mạng! Khi dùng Center Window, để tính $Y_t$, bạn đang lén lấy cả dữ liệu của tương lai ($Y_{t+1}, Y_{t+2}$) nhét ngược vào quá khứ. Điều này gây ra **Data Leakage**. Mô hình huấn luyện ra kết quả sai số bằng 0, nhưng khi đưa lên production sẽ chết ngay lập tức vì ở thực tế không ai biết tương lai.
- _Cách làm chuẩn của Senior:_ Luôn dùng **Trailing Window** (chỉ nhìn về quá khứ) để tính moving average cho các giá trị hiện tại (present values).

**2. Quên khôi phục dữ liệu (Inverse Transform):** Sau khi dùng Differencing $Y'_t = Y_t - Y_{t-n}$ để gạt bỏ hoàn toàn mùa vụ, Junior train mô hình RNN/LSTM và xuất ra biểu đồ. Tuy nhiên, họ lại mang y nguyên kết quả dự báo của $Y'_t$ báo cáo cho sếp. Biểu đồ trông rất đẹp nhưng giá trị nằm ở thang $[-10, 10]$ thay vì dải giá trị thật của giá cổ phiếu là hàng ngàn USD. Nhớ rằng: Làm kỹ thuật gì để xử lý mùa vụ lúc Train, thì lúc Dự báo phải làm phép toán **cộng dồn ngược lại (Restoring)**, để trả về giá trị vật lý gốc.

---

_Như vậy, nếu đây là một bài kiểm tra cho tín chỉ TensorFlow / Time Series Forecasting của bạn, hãy ưu tiên khoanh vào **B**, vì "Moving Average" và "Smoothing" là phương pháp được trình bày nguyên một cụm slide cực kỳ đồ sộ từ đến. Chúc bạn đạt điểm tuyệt đối!_
---

## Related
- [[🗺️ MOC - Machine Learning]]
