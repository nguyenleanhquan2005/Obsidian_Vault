---
tags:
  - speech-processing
  - TTS
  - speech-synthesis
  - chapter-13
aliases:
  - Text-to-Speech Synthesis
  - TTS Methods
  - Tổng Hợp Tiếng Nói
date: 2026-03-24
status: complete
---

# Chapter 13 — Text-to-Speech Synthesis Methods

> [!abstract] Tóm tắt chương
> Chương này trình bày toàn bộ pipeline của hệ thống TTS (Text-to-Speech): từ phân tích văn bản đầu vào, lịch sử tiến hóa các phương pháp tổng hợp, đến các hệ thống neural network hiện đại như WaveNet và Tacotron 2.

---

## Bản đồ nội dung

```
Text-to-Speech Synthesis Methods
├── 1. Text Analysis (Tiền xử lý văn bản)
│   ├── Tokenization
│   ├── Lexical Analysis (G2P)
│   └── Syntactic Parsing
├── 2. Lịch Sử Tiến Hóa TTS
│   ├── Formant Synthesis (LPC)
│   ├── Concatenative Synthesis
│   ├── Statistical Parametric (HMM/GMM)
│   ├── Neural Network-based (WaveNet)
│   └── End-to-End (Tacotron 2, FastSpeech)
├── 3. Early Approaches
│   ├── Formant Synthesis chi tiết
│   └── Articulatory Synthesis
├── 4. Unit Selection Methods
│   ├── Database creation
│   ├── Target cost & Join cost
│   └── Dynamic programming selection
└── 5. TTS Future Needs
    ├── Hạn chế hiện tại
    └── Emotion-aware TTS
```

---

## 1. Text Analysis — Tiền Xử Lý Văn Bản

### 1.1 Vai Trò Của Text Analysis

**Text analysis** là bước tiền xử lý bắt buộc trong TTS — biến đổi văn bản thô thành thông tin ngôn ngữ cần thiết để tạo tiếng nói:

```
"Hello, how are you?"
        │
        ▼ Text Analysis
Phonemes + Stress + Intonation + Duration
        │
        ▼ Synthesis
🔊 Giọng nói tự nhiên
```

### 1.2 Tokenization

Tách văn bản thành các đơn vị (tokens):

```python
Input:  "Hello, how are you?"
Output: ["Hello", ",", "how", "are", "you", "?"]
```

**Xử lý trường hợp đặc biệt:**
- Contractions: "can't" → ["can", "'t"]
- Abbreviations: "Dr." → "Doctor"
- Numbers: "100" → "one hundred"

### 1.3 Lexical Analysis (G2P)

**Lexical analysis** tra từ điển để lấy **phiên âm** và **thông tin ngôn ngữ**:

| Từ | Phiên âm | POS tag |
|----|----------|---------|
| "cat" | /k æ t/ | Noun |
| "read" | /r iː d/ hoặc /r ɛ d/ | Verb |
| "the" | /ðə/ hoặc /ðiː/ | Determiner |

**Out-of-vocabulary (OOV) words:** Dùng **Grapheme-to-Phoneme (G2P)** để tự động phiên âm từ chưa có trong từ điển — dựa trên quy tắc ngữ âm học hoặc neural G2P model.

### 1.4 Syntactic Parsing

Phân tích **cấu trúc ngữ pháp** để xác định prosody (nhấn mạnh, ngắt nghỉ):

```
Input: "The cat chased the mouse."
Parse Tree:
(S
  (NP (DT The) (NN cat))
  (VP (VBD chased)
    (NP (DT the) (NN mouse))))
```

**Tại sao cần parse tree?**
- Xác định **trọng âm** (stress): danh từ vs động từ
- Xác định **vị trí ngắt nghỉ** (pauses): mệnh đề, dấu phẩy
- Xác định **intonation contour**: câu hỏi hay khẳng định

---

## 2. Lịch Sử Tiến Hóa Các Phương Pháp TTS

### 2.1 Timeline Tổng Quan

```
1960s-70s          1980s-90s          2000s              2010s-nay
    │                  │                 │                   │
Formant          Concatenative    Statistical          Neural Network
Synthesis    →   Synthesis     →  Parametric      →   End-to-End
(LPC-based)     (Unit Selection)  (HMM/GMM)          (WaveNet, Tacotron)
```

### 2.2 So Sánh Các Thế Hệ

| Phương pháp | Chất lượng | Kích thước | Linh hoạt | Ví dụ |
|------------|-----------|-----------|----------|-------|
| **Formant** | Thấp — robotic | Nhỏ | Cao | LPC synth |
| **Concatenative** | Cao — natural | **Rất lớn** | Thấp | Unit selection |
| **Statistical Parametric** | Trung bình | Nhỏ vừa | Cao | HTS |
| **Neural Network** | **Rất cao** | Lớn | Cao | WaveNet |
| **End-to-End** | **Tốt nhất** | Lớn | Rất cao | Tacotron 2 |

---

## 3. Early Speech Synthesis Approaches

### 3.1 Formant Synthesis

**Công thức:** Mô phỏng vocal tract bằng cách tạo waveforms dựa trên **formant frequencies**:

```
Control parameters:
  Pitch (F0) + Volume + F1 + F2 + F3
        │
        ▼
Formant synthesizer
        │
        ▼
Speech waveform
```

**Kỹ thuật điển hình:** Linear Predictive Coding (LPC) synthesis

| Ưu điểm | Nhược điểm |
|---------|-----------|
| Kiểm soát tốt các tham số | Giọng nghe robotic, không tự nhiên |
| Dataset nhỏ | Khó tạo các âm chuyển tiếp mượt mà |
| Tính toán nhẹ | Thiếu naturalness |

### 3.2 Articulatory Synthesis

Mô phỏng **quá trình vật lý** của vocal tract — chuyển động của lưỡi, môi, hàm:

- Dùng **mô hình giải phẫu chi tiết** của vocal tract
- Mô phỏng airflow và pressure
- **Tự nhiên hơn** formant synthesis nhưng **phức tạp hơn nhiều**
- Ví dụ: mô hình của **Gunnar Fant** (cha đẻ của acoustic phonetics)

**1. Kỷ nguyên sơ khai của TTS (Câu 107)**

- **Bản chất (Đáp án D):** Phương pháp tổng hợp tiếng nói đầu tiên trong lịch sử sử dụng **Các máy móc cơ học (Mechanical speech synthesizers)**. Ví dụ điển hình là cỗ máy của Kratzenstein (1779) dùng các hộp cộng hưởng hình thù kỳ dị kết hợp với một ống sậy rung để tạo ra các nguyên âm mô phỏng giọng người. Nó hoàn toàn là cơ học, không có sự can thiệp của tín hiệu số.

**2. Kỷ nguyên hiện đại - Unit Selection Synthesis (Câu 115)**

- **Bản chất:** Siri hay Google Assistant hiện nay nghe tự nhiên đến rợn người là nhờ công nghệ "Tổng hợp Chọn đơn vị" (Unit Selection Synthesis).
- **Unit (Đơn vị) là gì? (Đáp án D):** "Unit" ở đây ám chỉ **một âm vị (phoneme) hoặc một cặp âm vị (diphone) được trích xuất từ một cơ sở dữ liệu ghi âm khổng lồ**.
- **Cách hoạt động:** Thay vì dùng toán học sinh ra sóng âm (như Formant Synthesizer), hệ thống này ghi âm hàng chục nghìn giờ giọng của một người thật. Khi bạn yêu cầu máy đọc một câu, thuật toán Viterbi sẽ lao vào kho dữ liệu, tìm các mảnh ghép (diphone) phù hợp nhất với ngữ cảnh, và ghép (concatenate) chúng lại với nhau. Giọng bạn nghe thấy chính là giọng thu âm thật được chắp vá đỉnh cao!

## **Nguyên lý hoạt động của Speech synthesis**

Speech synthesis hoạt động theo ba giai đoạn chính: chuyển văn bản thành từ, từ thành âm vị (phonemes) và từ âm vị thành âm thanh.

**Chuyển văn bản thành từ**

Ở bước này, hệ thống sẽ xử lý và chuẩn hóa văn bản đầu vào (như viết tắt, chữ số, ký hiệu…) để tránh gây nhầm lẫn trong quá trình chuyển đổi thành giọng nói. Việc này bao gồm chuyển đổi các số, ngày tháng, từ viết tắt, ký hiệu đặc biệt thành dạng từ ngữ dễ đọc. Quá trình này cũng xử lý các từ đồng âm khác nghĩa - những từ có cách viết giống nhau nhưng cách phát âm khác nhau tùy theo ngữ cảnh. Các mô hình như Hidden Markov hoặc mạng nơ-ron được sử dụng để xác định cách phát âm phù hợp nhất.

**Chuyển từ thành âm vị**

Sau khi xác định được từ, hệ thống sẽ phân tách từ thành các âm vị - những đơn vị âm thanh nhỏ nhất cấu thành nên từ đó. Ngoài ra, có thể phân tích từ theo các đơn vị chữ viết (graphemes) rồi áp dụng quy tắc để chuyển các đơn vị này thành âm vị tương ứng.

**Chuyển âm vị thành âm thanh**

Có ba cách phổ biến để tổng hợp âm thanh từ các âm vị:

- **Concatenative synthesis**: Sử dụng các đoạn ghi âm giọng người đã được lưu sẵn để ghép nối lại thành câu nói.
- **Formant synthesis**: Tạo âm thanh bằng cách mô phỏng các đặc điểm cộng hưởng trong giọng nói, không dùng dữ liệu ghi âm.
- **Articulatory synthesis**: Mô phỏng cơ chế phát âm của hệ thanh quản con người để tạo giọng nói một cách chi tiết và tự nhiên.

![Nguyên lý hoạt động của speech systhesis](https://vnptai.io/storage/thumbnail/nguyen%20ly%20hoat%20dong%20cua%20speech%20synthesis.jpg)

 Speech synthesis chuyển văn bản thành giọng nói qua phân tích và tổng hợp âm thanh

## **Các kỹ thuật tổng hợp giọng nói**

Hiện nay, tổng hợp giọng nói thường dựa trên bốn kỹ thuật chính:

- **Concatenative Synthesis (Tổng hợp nối ghép)**: Kỹ thuật này ghép nối các đoạn âm thanh đã được ghi âm từ giọng nói thật, sau đó xử lý để các đoạn nối liền mượt mà và tự nhiên hơn.
- **Formant Synthesis (Tổng hợp cộng hưởng)**: Sử dụng các mô hình toán học để mô phỏng hoạt động của bộ phận phát âm trong cơ thể người, tạo ra âm thanh rõ ràng nhưng thường kém tự nhiên so với giọng thật.
- **Articulatory Synthesis (Tổng hợp mô phỏng phát âm)**: Mô phỏng cách hoạt động của miệng, lưỡi và dây thanh quản khi phát âm giúp tạo ra giọng nói nhân tạo một cách chi tiết hơn.
- **Deep Learning-Based Synthesis (Tổng hợp dựa trên học sâu)**: Áp dụng [trí tuệ nhân tạo](https://vnptai.io/vi/blog/detail/tri-tue-nhan-tao-ai-la-gi) và [mạng nơ-ron](https://vnptai.io/vi/blog/detail/neural-network-la-gi), sử dụng tập dữ liệu giọng nói quy mô lớn để học các mẫu nói tự nhiên, từ đó tạo ra giọng tổng hợp gần giống giọng người thật nhất.

---

## 4. Unit Selection Methods

### 4.1 Nguyên Lý

**Unit selection synthesis** ghép nối các đơn vị tiếng nói được ghi sẵn từ **database lớn**:

```
Input text
    │
    ▼ Text Analysis → phoneme sequence
    │
    ▼ Unit Selection → chọn units tốt nhất từ database
    │
    ▼ Concatenation → ghép units lại
    │
    ▼ Post-processing → làm mượt transitions
    │
    ▼ 🔊 Natural speech output
```

### 4.2 Quy Trình Xây Dựng Database

1. **Thu âm** một corpus tiếng nói lớn (nhiều giờ)
2. **Phân đoạn** thành các units: phonemes, diphones, syllables
3. **Trích xuất features** từng unit: pitch, duration, energy, spectral

### 4.3 Hai Hàm Chi Phí — Cốt Lõi Của Unit Selection

**Target Cost** — đánh giá unit có phù hợp với **ngữ cảnh ngôn ngữ** không:
- Phoneme identity
- Part-of-speech
- Stress position

**Join Cost** — đánh giá chất lượng **ghép nối** giữa hai units liền nhau:
- Pitch continuity (không bị nhảy đột ngột)
- Spectral similarity (không bị "click" khi ghép)

**Tổng chi phí:**
$$C_{total} = w_t \cdot C_{target} + w_j \cdot C_{join}$$

### 4.4 Dynamic Programming Selection

Dùng **dynamic programming** để tìm sequence tối ưu:

$$\text{Best path} = \arg\min \sum_i \left(C_{target}(u_i) + C_{join}(u_{i-1}, u_i)\right)$$

| Ưu điểm | Nhược điểm |
|---------|-----------|
| Chất lượng rất cao với database lớn | Database **rất lớn** (GB) |
| Tiếng nói tự nhiên | Khó thay đổi style/emotion |
| Đã được dùng thương mại lâu | Transitions đôi khi không mượt |

---

## 5. Neural Network-Based Synthesis

### 5.1 WaveNet (Google DeepMind, 2016)

**WaveNet** là **deep generative model** tạo ra waveform sample-by-sample:

$$P(x) = \prod_{t=1}^{T} P(x_t | x_1, \ldots, x_{t-1})$$

- Dùng **dilated causal convolutions** để có receptive field lớn
- Chất lượng gần như không phân biệt được với người thật
- **Nhược điểm ban đầu:** Rất chậm — ~1 giây/giây (real-time factor = 1)

### 5.2 Tacotron 2 (Google, 2017)

**End-to-end model** tích hợp toàn bộ TTS pipeline:

```
Text input
    │
    ▼ [Encoder] — character/phoneme embeddings
    │
    ▼ [Attention mechanism] — align text with speech
    │
    ▼ [Decoder] — tạo Mel spectrogram
    │
    ▼ [WaveNet vocoder] — Mel spectrogram → waveform
    │
    ▼ 🔊 Natural speech
```

| Ưu điểm | Nhược điểm |
|---------|-----------|
| Pipeline đơn giản | Cần **nhiều data** (hàng chục giờ) |
| Chất lượng tốt nhất | Tính toán nặng |
| Có thể học style/emotion | Khó kiểm soát chi tiết |

### 5.3 FastSpeech (Microsoft, 2019)

Cải tiến Tacotron — **non-autoregressive** (song song hóa) → nhanh hơn nhiều lần trong inference.

---

## 6. TTS Future Needs

### 6.1 Hạn Chế Hiện Tại

| Thách thức | Mô tả |
|-----------|-------|
| **Naturalness** | Vẫn còn "uncanny valley" — nghe gần như người nhưng chưa hoàn toàn |
| **Expressiveness** | Khó truyền tải cảm xúc tinh tế, intonation phức tạp |
| **Data efficiency** | Cần nhiều dữ liệu → khó cho ngôn ngữ thiểu số |
| **Computational cost** | Neural TTS nặng → khó chạy on-device |

### 6.2 Hướng Phát Triển

- **Zero-shot voice cloning** — clone giọng từ vài giây mẫu
- **Emotion-aware TTS** — kiểm soát cảm xúc trong giọng nói
- **Multilingual TTS** — một model cho nhiều ngôn ngữ
- **Efficient models** — chạy real-time trên thiết bị nhỏ

> [!example] Hệ thống TTS cảm xúc
> **Mục tiêu:** Text + Emotion label → Speech với cảm xúc phù hợp
>
> **Các bước:**
> 1. Thu thập emotional speech dataset (happy, sad, angry, neutral...)
> 2. Implement emotion-aware feature extraction
> 3. Train model với emotion conditioning
> 4. **Input:** "I'll be there soon" + 😊 → giọng vui
> 5. **Input:** "I'll be there soon" + 😢 → giọng buồn

## 7. Lịch Sử Sơ Khai — Mechanical Speech Synthesizers

### 7.1 Kỷ Nguyên Cơ Học

> [!info] Phương pháp đầu tiên trong lịch sử TTS
> Phương pháp tổng hợp tiếng nói đầu tiên trong lịch sử sử dụng **các máy móc cơ học (Mechanical speech synthesizers)**.
> Ví dụ: Cỗ máy của **Kratzenstein (1779)** dùng các hộp cộng hưởng hình thù kỳ dị + ống sậy rung để tạo nguyên âm mô phỏng giọng người — hoàn toàn cơ học, không có tín hiệu số.

### 7.2 Hạn Chế Của Early TTS

> [!warning] Nhược điểm chí mạng của TTS sơ khai
> Các hệ thống TTS sơ khai (formant synthesizer, giọng Stephen Hawking) bị giới hạn bởi **độ rõ chữ và tính tự nhiên cực thấp (Low intelligibility and naturalness)** — nghe rất giống robot.

---

## 8. Sự Chuyển Dịch Từ Concatenative → Parametric

### 8.1 Tại Sao Phải Chuyển?

**Unit Selection (Concatenative)** nghe rất tự nhiên nhưng:
- Database **quá khổng lồ** (hàng chục GB)
- Không thể thay đổi **cảm xúc giọng nói** (buồn/vui/tức giận)

→ Giới nghiên cứu dịch chuyển sang **Statistical Parametric Synthesis (SPS)**:
- Chỉ lưu **tham số toán học** ($F_0$, formants) — vài MB thay vì hàng chục GB
- Có thể tự do biến đổi giọng nam → nữ, đều đều → vui vẻ
- Nhét vừa vào **đồng hồ thông minh**!

### 8.2 Lưu Ý Về Formant Synthesis vs Articulatory Synthesis

> [!warning] Phân biệt quan trọng
> - **Formant Synthesis** (Statistical Parametric): điều khiển trực tiếp $F_1, F_2, F_3$ → đây mới là phương pháp dùng "formant models"
> - **Articulatory Synthesis**: mô phỏng vật lý chuyển động môi/răng/lưỡi — **không** dùng formant trực tiếp

### 8.3 Unit Selection — Cơ Chế Hoạt Động Chi Tiết

**Unit** trong Unit Selection là **phoneme hoặc diphone** được trích xuất từ database ghi âm khổng lồ.

**Kiến trúc chuẩn:**
```
Text Input
    │
    ▼ 1. Text Analysis (Phân tích văn bản)
Phoneme sequence + prosody
    │
    ▼ 2. Unit Selection Algorithm (Viterbi/Dynamic Programming)
Tìm trong database các mảnh ghép phù hợp nhất
    │
    ▼ 3. Waveform Concatenation (Ghép nối sóng âm)
    │
    ▼ 🔊 Natural speech
```

> Siri và Alexa nghe tự nhiên vì **chọn và ghép (concatenate) các đơn vị từ database ghi âm người thật** — không sinh toán học.

---

## Tóm Tắt

```
Văn bản đầu vào
        │
        ▼ Text Analysis
Tokenization → G2P → Syntactic Parsing
        │
        ▼
Phoneme sequence + Prosody info
        │
        ├──→ Formant Synthesis    (1960s - robotic)
        ├──→ Concatenative        (1990s - natural, large DB)
        ├──→ Statistical (HMM)   (2000s - flexible)
        └──→ Neural / End-to-End (2016+ - state-of-the-art)
                │
                ▼ WaveNet / Tacotron 2 / FastSpeech
        🔊 Natural Speech Output
```

| Phương pháp | Năm | Đặc trưng |
|------------|-----|----------|
| **Formant Synthesis** | 1960s | LPC, nhỏ gọn, robotic |
| **Articulatory** | 1970s | Mô phỏng vật lý, phức tạp |
| **Unit Selection** | 1990s | Natural, database lớn |
| **HMM-based (HTS)** | 2000s | Statistical, flexible |
| **WaveNet** | 2016 | Neural, nearly human-level |
| **Tacotron 2** | 2017 | End-to-end, attention |
| **FastSpeech** | 2019 | Non-autoregressive, fast |

---

## Liên Kết

- [[Chapter 9]] — Algorithms for Estimating Speech Parameters
- [[Chapter 11]] — Automatic Speech Recognition and NLU
- [[Chapter 3]] — Human Speech Production (Formants, Vocal Tract)
- [[Chapter 8]] — Linear Predictive Analysis (LPC Synthesis)
- [[MFCCs]]
- [[LPC]]
- [[Formants]]

---

*Chapter 13 · Text-to-Speech Synthesis Methods · Rabiner & Schafer · Tự học*

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
