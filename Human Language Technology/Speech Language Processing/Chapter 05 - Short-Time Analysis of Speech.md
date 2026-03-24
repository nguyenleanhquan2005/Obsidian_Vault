**3. Năng lượng ngắn hạn (Short-Time Energy) và phân loại V/U (Câu 22)**

- **Công thức:** $E[\hat{n}] = \sum_{m=0}^{L-1} (x[\hat{n}+m]w[m])^2$
- **Bản chất vật lý:** Âm hữu thanh (Voiced - như /a/, /e/) sinh ra do dây thanh đới rung đập mạnh, tạo ra áp suất khí lớn. Âm vô thanh (Unvoiced - như /s/, /f/) chỉ là luồng khí rít qua kẽ răng. Do đó, **âm hữu thanh luôn có năng lượng (energy) cao hơn rất nhiều so với âm vô thanh**. Các kỹ sư dùng STE để thiết kế hệ thống VAD (Voice Activity Detection), giúp Google Assistant biết khi nào bạn đang nói và khi nào bạn đang im lặng để ngắt mic.


**2. Dải tới hạn (Critical Band) và Mô hình Thính giác (Câu 35)**

- **Bản chất:** Tai người không nghe mọi tần số một cách tuyến tính. Ốc tai chia âm thanh thành khoảng 24 dải tần gọi là **Dải tới hạn (Critical Bands)**.
- **Hiệu ứng Masking (Đáp án D):** Nó xác định băng thông mà tại đó **hiện tượng che khuất thính giác (auditory masking)** xảy ra. Nếu có một tiếng trống đập rất to ở tần số 1000Hz, tai bạn sẽ bị "điếc tạm thời" và không thể nghe thấy tiếng vĩ cầm chơi nhỏ ở tần số 1050Hz (vì nó nằm trong cùng một dải tới hạn). Kỹ sư nén audio lợi dụng điều này để... xóa luôn tiếng vĩ cầm đi cho nhẹ file, vì đằng nào con người cũng không nghe thấy!


**🇬🇧 1. Handling Non-Stationary Signals with STFT (Q65, Q68)**

- **Concept:** Speech is **non-stationary** (it changes constantly). Taking a Fourier transform of a whole 5-second sentence gives a useless, blurry spectrum. The solution? **STFT (Short-Time Fourier Transform)**. We divide the signal into **short overlapping segments** (frames) to analyze the **frequency content over short time intervals** where the vocal tract is assumed to be stationary (not moving).
- **Math:** $X_n(e^{j\omega}) = \sum_{m=-\infty}^{\infty} x[m]w[n-m]e^{-j\omega m}$ (where $w[n-m]$ is the sliding window).

**🇻🇳 1. Xử lý tín hiệu không dừng bằng STFT (Câu 65, 68)**

- **Giải thích:** Tiếng nói thay đổi liên tục (**non-stationary**). Để phân tích, STFT **chia tín hiệu thành các đoạn ngắn chồng lấp lên nhau (short overlapping segments)**. Tại mỗi đoạn ngắn này (khoảng 20ms), ta coi như mồm và lưỡi người nói đang đứng im, từ đó trích xuất được **nội dung tần số trong khoảng thời gian ngắn đó (frequency content over short time intervals)**.

**🇬🇧 2. The Window Length Trade-off (Q63)**

- **Concept:** This is the Heisenberg Uncertainty Principle in DSP! If you increase the window length $L$, you capture more wave cycles (better frequency resolution), but you lose exact timing (worse time resolution).
    - **Rule:** As window length increases $\rightarrow$ **Time resolution decreases, but frequency resolution increases.**

**🇻🇳 2. Sự đánh đổi kích thước cửa sổ (Câu 63)**

- **Giải thích:** Đây chính là Nguyên lý Bất định Heisenberg trong âm thanh! Khi bạn tăng chiều dài cửa sổ (window length) lên, bạn gom được nhiều chu kỳ sóng hơn $\rightarrow$ **Độ phân giải tần số tăng (nhìn rõ các vạch Formant)**. Nhưng bù lại, bạn sẽ không biết chính xác âm thanh đó phát ra ở mili-giây nào $\rightarrow$ **Độ phân giải thời gian giảm**.

**🇬🇧 3. Zero-Crossing Rate - ZCR (Q81, Q83)**

- **Concept:** ZCR measures **the rate at which the signal's amplitude crosses zero** (from positive to negative volts).
    - **Unvoiced sounds (Âm vô thanh - like /s/, /f/):** High frequency noise $\rightarrow$ **Higher ZCR**.
    - **Voiced sounds (Âm hữu thanh - like vowels):** Low frequency $\rightarrow$ Lower ZCR.

**🇻🇳 3. Tỷ lệ qua điểm không - ZCR (Câu 81, 83)**

- **Giải thích:** ZCR đơn giản là đếm **tốc độ tín hiệu cắt qua trục hoành (crosses zero)**. Âm vô thanh (như chữ /s/) là nhiễu tần số rất cao, sóng dao động cực nhanh nên cắt trục hoành liên tục $\rightarrow$ **ZCR rất cao**. Âm hữu thanh dao động chậm nên ZCR thấp.



