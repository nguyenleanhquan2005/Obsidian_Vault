**2. Mô hình thính giác (Auditory Models - Câu 11)**

- Tai người (ốc tai - cochlea) thực chất là một Filter bank sinh học tự nhiên cực kỳ tinh vi. Khả năng tai người phân tách các âm thanh phức tạp (như nghe được tiếng bạn bè gọi giữa một quán bar ồn ào) được mô phỏng trong AI bằng lý thuyết **Auditory scene analysis (Phân tích bối cảnh thính giác)**.

**🇬🇧 1. The Human Ear and Auditory System (Q66, Q75, Q76, Q82)**

- **Cochlea (Ốc tai - Q75):** The snail-shaped organ primarily **responsible for converting physical sound waves into electrical nerve signals**.
- **Basilar Membrane (Màng nền - Q66):** Located inside the cochlea. It acts like a mechanical filter bank to **separate sound frequencies and stimulate different hair cells**. High frequencies resonate at the base, low frequencies at the apex.
- **Place Theory Limitation (Q76):** Place theory says pitch is determined by _where_ the basilar membrane vibrates. **Limitation:** It **cannot explain the perception of very low-frequency sounds** (below 50Hz) because the membrane is too stiff. For low frequencies, the brain uses timing/volley theory instead.
- **Auditory Cortex (Vỏ não thính giác - Q82):** Once electrical signals reach the brain, the cortex's job is to **process and interpret complex auditory signals** (e.g., recognizing that a sound is your mother's voice).

**🇻🇳 1. Thính giác con người (Câu 66, 75, 76, 82)**

- **Giải thích:** Âm thanh vật lý biến thành điện não ở đâu? Chính là **Ốc tai (Cochlea - Câu 75)**. Bên trong Ốc tai có **Màng nền (Basilar membrane - Câu 66)** hoạt động như phím đàn piano để **tách các tần số khác nhau và kích thích tế bào lông**.
- Tuy nhiên, Lý thuyết Vị trí (Place Theory) có điểm yếu chí mạng: Nó **không thể giải thích cách ta nghe được âm trầm (low-frequency - Câu 76)**. Cuối cùng, tín hiệu điện chạy lên **Vỏ não thính giác (Auditory Cortex - Câu 82)** để bộ não **xử lý và diễn giải ý nghĩa**.

**🇬🇧 2. Phonetics & Bayesian Voicing Detection (Q61, Q67, Q69, Q79)**

- **Voicing (Tính thanh - Q61, Q67):** The vibration of the vocal cords. It is the primary **distinctive feature** that distinguishes consonants like /p/ (unvoiced) from /b/ (voiced).
- **Bayesian Approach (Q69, Q79):** Instead of using hard thresholds (if energy > 10 $\rightarrow$ Voiced), AI uses Bayesian probability. **Advantage (Q69):** It uses probabilities to **incorporate prior knowledge** (e.g., speech is usually voiced 60% of the time) **and adapt to different speech patterns**.

**🇻🇳 2. Ngữ âm học và Bộ dò âm Bayes (Câu 61, 67, 69, 79)**

- **Giải thích:** Trong tiếng Anh, đặc trưng khu biệt lớn nhất giữa các phụ âm là **Voicing (Sự rung dây thanh - Câu 61, 67)**. Ví dụ sờ tay lên cổ họng: /s/ không rung (Unvoiced), /z/ rung mạnh (Voiced).
- Để dạy AI phân biệt V/U, ta dùng **Bayesian approach (Phương pháp Bayes - Câu 79)**. Lợi thế tuyệt đối của Bayes là nó cho phép AI **tích hợp các tri thức tiên nghiệm (prior knowledge - Câu 69)** để phán đoán xác suất thông minh hơn thay vì chỉ dùng các luật cứng nhắc.