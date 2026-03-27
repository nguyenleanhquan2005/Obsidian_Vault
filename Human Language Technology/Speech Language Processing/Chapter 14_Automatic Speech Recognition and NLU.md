---
tags:
  - speech-processing
  - ASR
  - NLU
  - chapter-14
aliases:
  - Automatic Speech Recognition
  - ASR
  - NLU
  - Nhận Dạng Tiếng Nói Tự Động
date: 2026-03-24
status: complete
---

# Chapter 14 — Automatic Speech Recognition and NLU

> [!abstract] Tóm tắt chương
> Chương này trình bày toàn bộ pipeline của hệ thống ASR hiện đại: công thức toán học nền tảng, các thành phần acoustic model, language model, và decoding, kết hợp với NLU để tạo ra hệ thống hiểu ngôn ngữ nói. Bao gồm cả giao diện người dùng giọng nói (VUI) và Multimodal UI.

---

## Bản đồ nội dung

```
Automatic Speech Recognition and NLU
├── 1. Basic ASR Formulation
│   ├── Công thức Bayes nền tảng ★
│   ├── Acoustic Modeling (HMM, DNN)
│   ├── Language Modeling (N-gram, Transformer)
│   └── Decoding (Viterbi, Beam Search)
├── 2. Overall Speech Recognition Process
│   ├── Pipeline đầy đủ
│   ├── Preprocessing
│   └── Feature Extraction (MFCC, LPC)
└── 3. User Interfaces & Multimodal UI
    ├── GUI, VUI, Multimodal
    └── NLU: Intent & Entity
```

---

## 1. Basic ASR Formulation

### 1.1 Công Thức Nền Tảng — Bayes' Rule

**Bài toán ASR:** Cho tín hiệu âm thanh $\mathbf{X}$, tìm chuỗi từ $\mathbf{W}$ có xác suất cao nhất:

$$\hat{\mathbf{W}} = \arg\max_{\mathbf{W}} P(\mathbf{W} | \mathbf{X})$$

Áp dụng Bayes' Rule:

$$\hat{\mathbf{W}} = \arg\max_{\mathbf{W}} \underbrace{P(\mathbf{X} | \mathbf{W})}_{\text{Acoustic Model}} \cdot \underbrace{P(\mathbf{W})}_{\text{Language Model}}$$

> [!info] Giải thích
> - **$P(\mathbf{X} | \mathbf{W})$** — Acoustic Model: "Nếu người nói đang nói $\mathbf{W}$, xác suất nghe thấy $\mathbf{X}$ là bao nhiêu?"
> - **$P(\mathbf{W})$** — Language Model: "Chuỗi từ $\mathbf{W}$ có tự nhiên trong ngôn ngữ không?"

### 1.2 Acoustic Modeling

**Acoustic model** học mối quan hệ giữa **acoustic features** và **phonemes**:

```
Audio frames (MFCCs)
        │
        ▼ Acoustic Model
Phoneme probabilities: P(X|phoneme)
```

**Các kiến trúc:**

| Kiến trúc | Mô tả | Thời kỳ |
|-----------|-------|---------|
| **GMM-HMM** | Gaussian Mixture Model + Hidden Markov Model | Truyền thống |
| **DNN-HMM** | Deep Neural Network thay GMM | 2011+ |
| **End-to-End (CTC, Attention)** | Trực tiếp audio → text | 2015+ |
| **Wav2Vec 2.0, Whisper** | Self-supervised pre-training | 2020+ |

**MFCCs là features chính** cho acoustic model:

```
Raw audio → STFT → Mel filterbank → Log → DCT → MFCCs
                                              ↓
                                    [c0, c1, ..., c12]
                                    + Delta + Delta-Delta
                                    = 39-dimensional feature vector
```

### 1.3 Language Modeling

**Language model** ước lượng xác suất của chuỗi từ — giúp ASR chọn đúng từ có nghĩa trong ngữ cảnh:

$$P(\mathbf{W}) = P(w_1) \cdot P(w_2|w_1) \cdot P(w_3|w_1,w_2) \cdots$$

**Các loại language model:**

| Loại | Công thức | Ví dụ |
|------|-----------|-------|
| **N-gram** | $P(w_n | w_{n-1}, \ldots, w_{n-N+1})$ | Bigram, Trigram |
| **RNN/LSTM** | Học dependencies dài hơn | RNNLM |
| **Transformer** | Attention — state-of-the-art | GPT, BERT |

> [!example] Tại sao Language Model quan trọng?
> Acoustic model nghe "recognize speech" ≈ "wreck a nice beach" (phát âm giống nhau!)
> → Language model biết "recognize speech" có xác suất cao hơn trong ngữ cảnh → chọn đúng.

### 1.4 Decoding — Tìm Chuỗi Từ Tốt Nhất

**Decoding** kết hợp acoustic scores + language scores để tìm $\hat{\mathbf{W}}$:

**Viterbi Decoding:**
- Tìm path tối ưu qua HMM states
- Đảm bảo tìm được **giải pháp tối ưu toàn cục**
- Phức tạp $O(N^2 T)$

**Beam Search:**
- Chỉ giữ **top-K hypotheses** tại mỗi bước
- Không đảm bảo tối ưu nhưng **nhanh hơn nhiều**
- Phổ biến hơn trong hệ thống thực tế

```
Time: t=1    t=2    t=3    t=4
       [the]─[cat]─[sat]─[down]  score: -5.2  ← best
       [the]─[car]─[sat]─[down]  score: -7.1
       [a]──[cat]─[sat]─[down]   score: -6.8
              ...
       (Beam width K = 10: chỉ giữ 10 paths tốt nhất)
```

**1. Mục tiêu và Kiến trúc ASR (Câu 8, 15, 21, 23)**

- **Mục tiêu (Câu 8, 23):** DSP sinh ra để phân tích, thao tác và tổng hợp tiếng nói. Đối với ASR, mục tiêu tối thượng là dịch tiếng nói thành văn bản (Speech to Text). Các hệ thống này giao tiếp với người dùng thông qua **VUI (Voice User Interface)** (ví dụ: nói "Hey Siri").
- **Front-End Processing (Câu 9, 15):** Máy tính không "nghe" được file WAV. Khối Front-End làm nhiệm vụ tiền xử lý, trích xuất đặc trưng (Feature Extraction - như MFCC) để **tìm ra các mẫu hình có ý nghĩa (meaningful patterns)** và **chuyển đổi tín hiệu thành biểu diễn số hóa** dưới dạng vector. Đặc trưng khu biệt này (Acoustic-phonetic feature) giúp máy tính phân biệt được các âm vị khác nhau (như /b/ khác /p/).

**2. Khối Giải mã (Decoder) và Mô hình Ngôn ngữ (Câu 6)**

- Dữ liệu từ Front-End chỉ là các phổ âm thanh. Khối **Decoder (Bộ giải mã)** sẽ dùng thuật toán Viterbi kết hợp với Mô hình Ngôn ngữ (Language Model) để **áp dụng các quy tắc ngôn ngữ nhằm tạo ra văn bản mạch lạc (coherent text)**.
    - _Ví dụ:_ Front-end nghe được âm thanh giống "ai lóp diu". Decoder dùng xác suất ngôn ngữ để biết đó là "I love you" chứ không phải "Eye lob yew".




**1. Giao diện Người dùng Giọng nói - VUI (Câu 29)**

- Trong chu trình giao tiếp tự nhiên với máy (Speech Dialog Circle), hệ thống được thiết kế đặc biệt để xử lý các lệnh bằng ngôn ngữ tự nhiên được gọi là **Voice User Interface (VUI)**. Khác với GUI (Graphic User Interface) dùng chuột và màn hình, VUI cho phép bạn nói "Siri, đặt báo thức 7h sáng mai" và máy tự hiểu.

---

## 2. Overall Speech Recognition Process

### 2.1 Pipeline Đầy Đủ

```
🎤 Microphone Input
        │
        ▼ Signal Acquisition
Raw Audio (16kHz, 16-bit PCM)
        │
        ▼ Preprocessing
Noise Reduction → Normalization → Segmentation
        │
        ▼ Feature Extraction
MFCCs / LPC / Filterbank features
(Every 10ms frame, 25ms window)
        │
        ▼ Acoustic Model
P(X|phonemes) — HMM/DNN/Transformer
        │
        ▼ Language Model
P(W) — N-gram/LSTM/Transformer
        │
        ▼ Decoder
Viterbi / Beam Search → Best word sequence
        │
        ▼ Post-processing
Punctuation, capitalization, formatting
        │
        ▼ 📝 Text Output
```

### 2.2 Preprocessing

| Bước | Mục đích |
|------|---------|
| **Noise reduction** | Loại bỏ background noise để tăng speech clarity |
| **Normalization** | Điều chỉnh amplitude về mức chuẩn |
| **Segmentation** | Chia audio thành chunks có thể xử lý được |
| **VAD** | Chỉ xử lý vùng có tiếng nói — tiết kiệm compute |

**3. Khử nhiễu (Noise Reduction - Câu 12)**

- Làm sao để lọc tiếng ồn quạt máy hay tiếng điều hòa ra khỏi tín hiệu? Trong DSP, phương pháp kinh điển và hiệu quả nhất là **Trừ phổ (Spectral Subtraction)**. Ta ước lượng phổ của tiếng ồn trong những đoạn "Silence" (tính bằng thuật toán ở Domain 2), sau đó lấy phổ của toàn bộ tín hiệu trừ đi phổ tiếng ồn này.
- **Sai lầm phổ biến:** Sinh viên nghĩ rằng Spectral Subtraction sẽ trả lại âm thanh trong vắt. Thực tế, phép trừ này tạo ra các dải phổ âm (negative spectrum), khi dùng hàm trị tuyệt đối để bù lại, nó gây ra hiệu ứng "Musical Noise" (tiếng nhiễu ríu rít như tiếng chim hót/nước chảy róc rách) rất đặc trưng trong các ứng dụng gọi video (như Zoom) nếu không có thuật toán làm mượt (smoothing).
### 2.3 Feature Extraction

**MFCCs** là feature phổ biến nhất:
- **13 MFCC coefficients** (c0–c12)
- **13 Delta** (tốc độ thay đổi)
- **13 Delta-Delta** (gia tốc thay đổi)
- **Tổng: 39 features** mỗi frame

**LPC** cũng được dùng:
- Mô hình hóa vocal tract
- Ít chiều hơn MFCC nhưng diễn giải được về vật lý

### 2.4 Thế Hệ ASR Hiện Đại

**Whisper (OpenAI, 2022):**
- Trained trên **680,000 giờ** audio đa ngôn ngữ
- End-to-end: audio spectrogram → Transformer encoder-decoder → text
- Hỗ trợ **99 ngôn ngữ**, transcription và translation

**Wav2Vec 2.0 (Meta, 2020):**
- **Self-supervised pre-training** trên unlabeled audio
- Fine-tune với ít labeled data → tiết kiệm annotation cost

---

## 3. Natural Language Understanding (NLU)

### 3.1 ASR vs NLU

| | **ASR** | **NLU** |
|-|---------|---------|
| **Input** | Audio | Text (từ ASR) |
| **Output** | Text | Meaning/Intent |
| **Câu hỏi** | "Người đó nói gì?" | "Người đó muốn gì?" |

### 3.2 NLU Components

**Intent Recognition** — người dùng muốn làm gì?

```
"Set an alarm for 7am"  →  Intent: SET_ALARM
"What's the weather?"   →  Intent: GET_WEATHER
"Play some jazz"        →  Intent: PLAY_MUSIC
```

**Entity Extraction** — các thông tin cụ thể trong câu:

```
"Set an alarm for 7am tomorrow"
         │              │
    Time entity    Date entity
     "7am"         "tomorrow"
```

**Dialog Management** — duy trì ngữ cảnh hội thoại:

```
Turn 1: "Book a flight to Hanoi"    → Intent: BOOK_FLIGHT, Dest: Hanoi
Turn 2: "Make it next Friday"       → Date: next Friday (nhờ context từ Turn 1)
Turn 3: "And return on Sunday"      → Return date: Sunday (context vẫn giữ)
```

---

## 4. User Interfaces & Multimodal UI

### 4.1 Các Loại Giao Diện

| Loại UI | Mô tả | Ví dụ |
|---------|-------|-------|
| **GUI** (Graphical) | Visual elements: buttons, icons, menus | Desktop apps |
| **VUI** (Voice) | Tương tác bằng giọng nói | Siri, Alexa |
| **Multimodal** | Kết hợp nhiều phương thức: voice + touch + gesture | Modern smartphones |

### 4.2 Voice User Interface (VUI)

**VUI** tích hợp ASR + NLU để cho phép tương tác tự nhiên:

```
User: "Turn on the lights"
        │
        ▼ ASR
Text: "Turn on the lights"
        │
        ▼ NLU
Intent: CONTROL_DEVICE
Entity: Device="lights", Action="on"
        │
        ▼ Action execution
💡 Lights ON
        │
        ▼ TTS response
🔊 "Okay, turning on the lights"
```

**Thiết kế VUI tốt:**
- **Intuitive** — lệnh tự nhiên, không cần nhớ syntax
- **Responsive** — phản hồi nhanh (< 1 giây)
- **Clear feedback** — user biết hệ thống đã hiểu hay chưa
- **Error recovery** — xử lý tốt khi không hiểu ("Sorry, could you repeat that?")

### 4.3 Multimodal UI

**Multimodal UI** kết hợp nhiều modalities — linh hoạt và accessible hơn:

```
Voice input    ──┐
Touch input    ──┤ Sensor fusion → Unified understanding → Response
Gesture input  ──┘
```

> [!example] Ví dụ thực tế
> - Nói "Show me restaurants nearby" + chỉ tay vào bản đồ → hệ thống kết hợp cả hai để hiểu "nearby" nghĩa là vùng đang chỉ
> - Gõ lệnh trên bàn phím kết hợp với voice confirmation

**🇬🇧 2. Unit Selection TTS & Multimodal UI (Q70, Q71, Q72)**

- **Unit Selection (Q72):** Siri and Alexa sound human because they don't generate math waves; they **select and concatenate (join) units from a massive database of recorded human speech**.
- **Formant Estimation in Noise (Q71):** To find formants in a noisy room, engineers combine LPC, spectral smoothing, and temporal tracking (All of the above).
- **Multimodal UI (Q70):** Modern interfaces combine speech recognition with touch, gestures, and eye-tracking (All of the above) for seamless user experiences.

**🇻🇳 2. Tổng hợp giọng nói & Giao diện đa phương thức (Câu 70, 71, 72)**

- **Giải thích:** Các hệ thống AI hiện đại (Siri) nghe rất thật vì chúng dùng phương pháp **Unit Selection (Chọn đơn vị - Câu 72)**: Nó lục tìm trong một database ghi âm khổng lồ, **chọn các âm thanh phù hợp và ghép (concatenate) chúng lại**. Khi tương tác, AI thường kết hợp nhận dạng giọng nói với cảm ứng, ánh mắt tạo thành **Multimodal UI (All of the above - Câu 70)**.

## 5. HMM trong ASR

### 5.1 Tại Sao Dùng HMM?

Tiếng nói là chuỗi tín hiệu với độ dài ngẫu nhiên. **Hidden Markov Model (HMM)** cho phép tính xác suất chuyển trạng thái:

$$\text{Silence} \rightarrow \text{Unvoiced} \rightarrow \text{Voiced} \rightarrow \text{Silence}$$

một cách trơn tru, dẻo dai với nhiễu môi trường — thay vì dùng if/else cứng nhắc.

### 5.2 Ứng Dụng HMM: Voiced/Unvoiced Detection

```
State: Silence  →  Unvoiced  →  Voiced  →  Silence
         │              │           │
    P(stay)=0.9    P(stay)=0.8  P(stay)=0.85
    P(go)=0.1      P(go)=0.2    P(go)=0.15
```

HMM học được xác suất chuyển trạng thái và xác suất phát ra observation (features) → phân loại chính xác hơn luật cứng.

---

## 6. Decoding & Language Model

### 6.1 Decoding — Bước Khó Nhất

Sau khi có vector MFCC, bước **Decoding (Giải mã)** khớp các vector với từ điển:

> **Decoding = Quá trình khớp các từ được nói với từ điển định sẵn (matching spoken words to a pre-defined vocabulary)** để tìm chuỗi từ có xác suất cao nhất.

### 6.2 Language Model — Vai Trò Thiết Yếu

$$\hat{W} = \arg\max_W \underbrace{P(X|W)}_{\text{Acoustic}} \cdot \underbrace{P(W)}_{\text{Language Model}}$$

> [!example] Language Model cứu ASR khỏi nhầm lẫn
> "I write with a **pen**" vs "I write with a **pan**" — sóng âm gần giống nhau.
> Acoustic Model bối rối, nhưng **Language Model (N-gram)** biết xác suất "I write with a pen" cao hơn "I write with a pan" hàng nghìn lần → ASR chọn đúng!

**Vai trò của Language Model:** Cải thiện độ chính xác bằng cách **dự đoán xác suất của các chuỗi từ (predicting the probability of word sequences)**.

---

## 7. Front-End Processing

**Front-End** làm nhiệm vụ tiền xử lý:
- Trích xuất MFCC → **tìm ra các mẫu hình có ý nghĩa (meaningful patterns)**
- **Chuyển đổi tín hiệu thành biểu diễn số hóa** dưới dạng vector
- Acoustic-phonetic features → phân biệt các âm vị (/b/ khác /p/)

---

## 8. Multimodal UI — Thách Thức Đồng Bộ Hóa

### 8.1 Các Loại Input

| Modality | Sensor | Latency |
|----------|--------|---------|
| Voice | Microphone | ~10-50 ms |
| Touch | Touchscreen | ~5-20 ms |
| Gesture | Camera | ~33-100 ms |
| Eye tracking | IR sensor | ~10-30 ms |

### 8.2 Thách Thức Lớn Nhất

> [!warning] Synchronization Problem
> **Thách thức lớn nhất của Multimodal UI là đồng bộ hóa tín hiệu đầu vào từ nhiều phương thức khác nhau (Synchronizing input from multiple modalities).**

> [!example] Ví dụ thực tế
> Bạn vừa chỉ tay vào bản đồ trên xe vừa nói "Dẫn đường tới **đây**". Từ "đây" và ngón tay chạm màn hình xảy ra trên 2 phần cứng khác nhau với latency khác nhau.
>
> Việc đồng bộ timestamp để AI hiểu "đây" = tọa độ ngón tay là một **cơn ác mộng lập trình hệ thống**.

---

## Tóm Tắt

```
🎤 Audio Input
        │
        ▼
Preprocessing (Noise reduction, VAD)
        │
        ▼
Feature Extraction (MFCCs, 39-dim)
        │
        ▼
Acoustic Model          Language Model
P(X|W)                  P(W)
    └──────────┬─────────────┘
               ▼
          Decoder (Beam Search)
               │
               ▼
          📝 Text (ASR Output)
               │
               ▼
     NLU: Intent + Entity Extraction
               │
               ▼
     Dialog Management (Context)
               │
               ▼
     Action → TTS Response → 🔊
```

| Thành phần | Vai trò | Công nghệ hiện đại |
|-----------|---------|-------------------|
| **Acoustic Model** | Audio → Phonemes | Wav2Vec, Whisper |
| **Language Model** | Chuỗi từ tự nhiên | GPT, BERT |
| **Decoder** | Tìm chuỗi từ tốt nhất | Beam Search |
| **NLU** | Hiểu ý định | BERT fine-tuned |
| **Dialog Manager** | Duy trì ngữ cảnh | State machine / Neural |
| **TTS** | Phản hồi bằng giọng | Tacotron 2, WaveNet |

---

## Liên Kết

- [[Chapter 10]] — Text-to-Speech Synthesis Methods
- [[Chapter 8]] — Linear Predictive Analysis (LPC, Features)
- [[Chapter 5]] — Short-Time Analysis (MFCCs, STE, ZCR)
- [[Chapter 4]] — Hearing & Auditory Models
- [[MFCCs]]
- [[HMM]]
- [[Beam Search]]
- [[Transformer]]

---

*Chapter 14 · Automatic Speech Recognition and NLU · Rabiner & Schafer · Tự học*

**1. Mô hình HMM (Câu 50)**

- Tiếng nói là chuỗi tín hiệu thời gian với độ dài ngắn ngẫu nhiên. Để xác định các vùng Hữu thanh/Vô thanh hoặc nhận diện một âm vị, người ta không dùng các luật logic (if/else) cứng nhắc.
- Thay vào đó, thuật toán **Hidden Markov Model (HMM)** (thuộc trường phái Bayesian/Xác suất thống kê) được sử dụng rộng rãi nhất. HMM cho phép tính toán xác suất chuyển trạng thái từ vùng Âm lặng (Silence) $\rightarrow$ Vô thanh (Unvoiced) $\rightarrow$ Hữu thanh (Voiced) một cách trơn tru, dẻo dai với nhiễu môi trường.

**2. Giai đoạn Decoding (Giải mã - Câu 45)**

- Sau khi chuyển sóng âm thành các Vector đặc trưng (MFCC), máy tính vẫn chưa biết bạn nói gì. Giai đoạn khó nhất là đưa các Vector này đối chiếu với một từ điển (Lexicon) và mô hình ngôn ngữ (Language Model).
- Quá trình **khớp các từ được nói với một từ điển định sẵn** (matching spoken words to a pre-defined vocabulary) để tìm ra chuỗi từ (sentence) có xác suất cao nhất chính là **Decoding (Giải mã)**.


Chúng ta kết thúc bằng việc nhìn vào bức tranh toàn cảnh của hệ thống ASR.



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