**3. Tổng hợp tiếng nói (Speech Synthesis) & Sự nhầm lẫn của đề thi (Câu 13)**

- Như chúng ta đã từng phân tích, câu hỏi yêu cầu tìm phương pháp dùng "formant models". Đáp án đúng của hệ thống quiz ghi là "Articulatory synthesis" - Đây là một **ĐÁP ÁN LỖI** của người ra đề.
    - _Tại sao Articulatory sai?_ Nó mô phỏng vật lý chuyển động của môi, răng, lưỡi, không dùng formant.
    - _Tại sao Statistical Parametric đúng (ở cấp độ thực tiễn) nhưng không được tick?_ Vì Parametric (hoặc Formant Synthesis - như giọng cũ của Stephen Hawking) mới thực sự điều khiển các bộ lọc cộng hưởng (formants $F_1, F_2, F_3$) để tạo ra tiếng nói. Là một kỹ sư, bạn phải tỉnh táo trước các câu hỏi có đáp án được gán sai bởi hệ thống.


**2. Tổng hợp chọn đơn vị - Unit Selection Synthesis (Câu 28)**

- Làm sao để máy tính phát âm giống người nhất? Cách tốt nhất hiện nay (trước khi Deep Learning bùng nổ) là thu âm giọng của một người thật khoảng hàng ngàn giờ, cắt thành các đơn vị nhỏ (diphone/âm tiết), và ráp chúng lại.
- **Kiến trúc hệ thống chuẩn:** Đầu tiên là **Phân tích văn bản (Text analysis)** để biết cần phát âm chữ gì, sau đó dùng thuật toán **Unit selection algorithm (thường dùng Dynamic Programming/Viterbi)** để bới trong database tìm ra các mảnh ghép khớp nhất, và cuối cùng là **Ghép nối sóng âm (Waveform concatenation)** để phát ra loa.\

**3. Sự tiến hóa của Tổng hợp tiếng nói (Câu 31)**

- **Đáp án C - Chuyển từ ghép nối sang tham số hóa (Transition from concatenative synthesis to parametric synthesis):**
- **Góc nhìn Kỹ sư Senior:** Tại sao lại có sự chuyển dịch này? Phương pháp Unit Selection (Concatenative) nghe rất tự nhiên nhưng bộ database quá khổng lồ (hàng chục GB) và không thể thay đổi cảm xúc giọng nói (buồn/vui/tức giận). Do đó, giới nghiên cứu đã dịch chuyển sang **Statistical Parametric Synthesis (SPS)** (Tổng hợp Tham số Thống kê - thường dùng HMMs). Trong phương pháp này, thay vì lưu file WAV, máy tính chỉ lưu các _tham số toán học (F0, Formants)_. Nó giúp mô hình cực nhẹ (vài MB, nhét vừa vào đồng hồ thông minh) và có thể tự do biến đổi giọng nam thành nữ, giọng đều đều thành giọng vui vẻ.


**3. Sự tiến hóa của Text-to-Speech (TTS - Câu 44, 58)**

- **Quá khứ (Câu 44):** Các hệ thống tổng hợp tiếng nói sơ khai (Early TTS) như máy Voder hay formant synthesizer (ví dụ giọng nói của Stephen Hawking) gặp một hạn chế chí mạng: **Độ rõ chữ và tính tự nhiên cực thấp (Low intelligibility and naturalness)**, nghe rất giống robot.
- **Hiện đại (Unit Selection - Câu 58):** Để giải quyết vấn đề trên, Apple hay Google thu âm hàng trăm ngàn giờ giọng người thật, cắt thành các đơn vị âm (diphones). Khi bạn nhập Text, thuật toán Viterbi sẽ lục tìm trong kho dữ liệu và **Chọn ra các đơn vị ghi âm phù hợp nhất với ngữ cảnh (Selecting the most appropriate recorded units for each context)** để ghép lại, giúp giọng nói mượt mà và tự nhiên nhất.

**🇬🇧 1. The Dangers of Median Smoothing (Unnumbered Q, Q77)**

- **Concept:** Median smoothing is great for removing sudden spikes (outliers) in pitch tracking. But it has critical flaws.
    - **Delay (Q77):** To find the median of the next 5 frames, the system _must wait_ for those 5 frames to be spoken. This **introduces a significant delay in real-time processing**. (Imagine Auto-Tune lagging by 50ms during a live concert!).
    - **Over-smoothing (Unnumbered Q):** It creates "blocky" artifacts and can **blur important short features** (like a quick consonant). Thus, for the unnumbered question, challenges include computational load, varying levels, and over-smoothing $\rightarrow$ **All of the above (c)**.

**🇻🇳 1. Điểm yếu của Bộ lọc Trung vị (Câu không số, Câu 77)**

- **Giải thích:** Median Smoothing (lấy trung vị) dùng để lọc nhiễu đột biến cực tốt. NHƯNG: Để tính trung vị của 5 mẫu tương lai, máy tính phải "ngồi đợi" người dùng nói xong 5 mẫu đó $\rightarrow$ **Gây ra độ trễ cực lớn trong xử lý thời gian thực (introduces significant delay - Câu 77)**. Hơn nữa, nó dẽ làm mất các chi tiết mịn (over-smoothing). Do đó đáp án câu không số đầu tiên là **All of the above**.

**🇬🇧 2. Unit Selection TTS & Multimodal UI (Q70, Q71, Q72)**

- **Unit Selection (Q72):** Siri and Alexa sound human because they don't generate math waves; they **select and concatenate (join) units from a massive database of recorded human speech**.
- **Formant Estimation in Noise (Q71):** To find formants in a noisy room, engineers combine LPC, spectral smoothing, and temporal tracking (All of the above).
- **Multimodal UI (Q70):** Modern interfaces combine speech recognition with touch, gestures, and eye-tracking (All of the above) for seamless user experiences.

**🇻🇳 2. Tổng hợp giọng nói & Giao diện đa phương thức (Câu 70, 71, 72)**

- **Giải thích:** Các hệ thống AI hiện đại (Siri) nghe rất thật vì chúng dùng phương pháp **Unit Selection (Chọn đơn vị - Câu 72)**: Nó lục tìm trong một database ghi âm khổng lồ, **chọn các âm thanh phù hợp và ghép (concatenate) chúng lại**. Khi tương tác, AI thường kết hợp nhận dạng giọng nói với cảm ứng, ánh mắt tạo thành **Multimodal UI (All of the above - Câu 70)**.

**1. Kỷ nguyên sơ khai của TTS (Câu 107)**

- **Bản chất (Đáp án D):** Phương pháp tổng hợp tiếng nói đầu tiên trong lịch sử sử dụng **Các máy móc cơ học (Mechanical speech synthesizers)**. Ví dụ điển hình là cỗ máy của Kratzenstein (1779) dùng các hộp cộng hưởng hình thù kỳ dị kết hợp với một ống sậy rung để tạo ra các nguyên âm mô phỏng giọng người. Nó hoàn toàn là cơ học, không có sự can thiệp của tín hiệu số.

**2. Kỷ nguyên hiện đại - Unit Selection Synthesis (Câu 115)**

- **Bản chất:** Siri hay Google Assistant hiện nay nghe tự nhiên đến rợn người là nhờ công nghệ "Tổng hợp Chọn đơn vị" (Unit Selection Synthesis).
- **Unit (Đơn vị) là gì? (Đáp án D):** "Unit" ở đây ám chỉ **một âm vị (phoneme) hoặc một cặp âm vị (diphone) được trích xuất từ một cơ sở dữ liệu ghi âm khổng lồ**.
- **Cách hoạt động:** Thay vì dùng toán học sinh ra sóng âm (như Formant Synthesizer), hệ thống này ghi âm hàng chục nghìn giờ giọng của một người thật. Khi bạn yêu cầu máy đọc một câu, thuật toán Viterbi sẽ lao vào kho dữ liệu, tìm các mảnh ghép (diphone) phù hợp nhất với ngữ cảnh, và ghép (concatenate) chúng lại với nhau. Giọng bạn nghe thấy chính là giọng thu âm thật được chắp vá đỉnh cao!
