---
tags:
  - speech-processing
  - auditory
  - perception
  - chapter-4
aliases:
  - Hearing and Auditory Models
  - Speech Perception
  - Nghe và Tri Giác Tiếng Nói
date: 2026-03-24
status: complete
---

# Chapter 4 — Hearing, Auditory Models & Speech Perception

> [!abstract] Tóm tắt chương
> Chương này khám phá cách con người nghe và hiểu tiếng nói: từ cơ chế sinh lý của tai, các mô hình tính toán mô phỏng hệ thống thính giác, đến cách máy tính học nhận dạng và tái tạo quá trình tri giác tiếng nói.

---

## Bản đồ nội dung

```
Hearing, Auditory Models & Speech Perception
├── 1. Hearing (Thính Giác)
│   ├── Giải phẫu: Cochlea, Basilar Membrane ★
│   ├── Place Theory & giới hạn ★
│   ├── Auditory Cortex
│   └── Quá trình tri giác tiếng nói
├── 2. Auditory Models (Mô Hình Thính Giác)
│   ├── Cochlea = Biological Filter Bank ★
│   ├── Critical Bands & Auditory Masking ★
│   ├── Feature extraction (MFCC, Spectral)
│   ├── Voicing Detection & Bayesian Approach ★
│   └── Gammatone filterbank & Auditory nerve models
└── 3. Speech Perception (Tri Giác Tiếng Nói)
    ├── MFCC, Prosodic features
    └── Speech recognition models (HMM, Deep Learning)
```

---

## 1. Hearing — Thính Giác

### 1.1 Giải Phẫu Hệ Thống Thính Giác

```
Outer Ear (Tai ngoài)
    Pinna (vành tai) → thu âm
        │
        ▼
Middle Ear (Tai giữa)
    Eardrum (màng nhĩ) + Ossicles (xương con) → khuếch đại rung động
        │
        ▼
Inner Ear (Tai trong)
    Cochlea (ốc tai) → chuyển rung động thành tín hiệu thần kinh  ← QUAN TRỌNG NHẤT
        │
        ▼
Auditory Nerve → Auditory Cortex → Não
```
![[Pasted image 20260325151810.png]]
### 1.2 Cochlea & Basilar Membrane — Chi Tiết

**Cochlea (Ốc tai)** là cơ quan hình ốc sên, chịu trách nhiệm chính **chuyển đổi sóng âm vật lý thành tín hiệu thần kinh điện**. (**responsible for converting physical sound waves into electrical nerve signals**)

Bên trong cochlea có **Basilar Membrane (Màng nền)** — hoạt động như một **cơ học filter bank** (giống phím đàn piano) **tách các tần số khác nhau và kích thích tế bào lông** :
(**separate sound frequencies and stimulate different hair cells**)

| Vị trí trên màng | Nhạy cảm với    | Tương tự            |
| ---------------- | --------------- | ------------------- |
| **Base** (gốc)   | Tần số **cao**  | Phím cao đàn piano  |
| **Apex** (đỉnh)  | Tần số **thấp** | Phím trầm đàn piano |

> [!info] Tại sao Cochlea quan trọng với AI?
> Cochlea = **biological filter bank** tự nhiên. Thang **Mel** trong MFCC được thiết kế dựa trên chính cách cochlea phân tích tần số — phi tuyến, dày ở tần thấp, thưa ở tần cao.

### 1.3 Place Theory & Giới Hạn

**Place Theory (Thuyết Vị trí):** Pitch được xác định bởi **vị trí** màng nền rung động.

> [!warning] Giới hạn của Place Theory
> Place Theory **không thể giải thích** cách nghe âm trầm rất thấp (dưới ~50 Hz) vì màng nền ở vùng đó quá cứng, không rung được đủ để phân biệt.
> → Đối với âm trầm, não dùng **Volley Theory** (tốc độ bắn tín hiệu của dây thần kinh) thay thế.


### 1.4 Auditory Cortex

Sau khi tín hiệu điện đến não, **Auditory Cortex (Vỏ não thính giác)** đảm nhiệm **xử lý và diễn giải các tín hiệu thính giác phức tạp** — ví dụ: nhận ra đây là giọng của mẹ bạn giữa đám đông.

Once electrical signals reach the brain, the cortex's job is to **process and interpret complex auditory signals** (e.g., recognizing that a sound is your mother's voice).
### 1.5 Quá Trình Tri Giác Tiếng Nói Ở Người

**Speech Processing Pathway:**

```
Tín hiệu âm thanh đầu vào
        │
        ▼
Auditory Cortex
    → Nhận diện phonemes (đơn vị âm thanh)
    → Lắp ráp thành từ và câu
        │
        ▼
Higher-level Cognitive Processing
    → Tích hợp ngữ cảnh ngôn ngữ
    → Ngữ nghĩa (semantics)
    → Kiến thức nền (prior knowledge)
        │
        ▼
Hiểu ngôn ngữ nói
```

**Yếu tố nhận thức ảnh hưởng đến perception:**
- **Attention** (chú ý) — tập trung vào đâu
- **Memory** (trí nhớ) — ngữ cảnh trước đó
- **Language proficiency** (trình độ ngôn ngữ) — quen thuộc với ngôn ngữ

---

## 2. Auditory Models — Mô Hình Thính Giác

### 2.1 Cochlea Là Một Biological Filter Bank

> Tai người (ốc tai - cochlea) thực chất là một **filter bank sinh học tự nhiên** cực kỳ tinh vi.

Khả năng tai người phân tách các âm thanh phức tạp (nghe được tiếng bạn gọi giữa quán bar ồn ào) được mô phỏng trong AI bằng lý thuyết **Auditory Scene Analysis (Phân tích bối cảnh thính giác)**.

**Ứng dụng:** Speech recognition · Music analysis · Biomedical engineering

### 2.2 Critical Bands & Auditory Masking

**Critical Bands (Dải tới hạn):** Tai người không nghe mọi tần số một cách tuyến tính. Ốc tai chia âm thanh thành khoảng **24 dải tần gọi là Critical Bands**.

> [!example] Hiệu ứng Auditory Masking (Che khuất thính giác)
> Một tiếng trống đập rất to ở 1000 Hz → tai bạn "điếc tạm thời" và **không nghe thấy** tiếng vĩ cầm nhỏ ở 1050 Hz (cùng dải tới hạn).
>
> **Ứng dụng thực tế:** Kỹ sư nén audio (MP3) lợi dụng điều này — xóa luôn tiếng vĩ cầm vì đằng nào con người cũng không nghe thấy → file nhẹ hơn mà chất lượng không thay đổi trong nhận thức!

**Critical Band xác định:** Băng thông mà tại đó hiện tượng **auditory masking** xảy ra.

### 2.3 Voicing Detection & Bayesian Approach

**Voicing (Tính thanh)** là sự rung động của dây thanh — đặc trưng khu biệt **quan trọng nhất** giữa các phụ âm:


| | Voiced (Hữu thanh) | Unvoiced (Vô thanh) |
|--|----|----|
| **Ví dụ** | /b/, /z/ | /p/, /s/ |
| **Kiểm tra** | Sờ cổ họng → rung | Sờ cổ họng → không rung |
Ví dụ sờ tay lên cổ họng: /s/ không rung (Unvoiced), /z/ rung mạnh (Voiced)
- **Voicing (Tính thanh):** The vibration of the vocal cords. It is the primary **distinctive feature** that distinguishes consonants like /p/ (unvoiced) from /b/ (voiced).

**Bayesian Voicing Detection:**

Thay vì dùng luật cứng (`if energy > 10 → Voiced`), AI dùng **xác suất Bayes**:

$$P(\text{Voiced} | \text{features}) \propto P(\text{features} | \text{Voiced}) \cdot P(\text{Voiced})$$

> [!tip] Lợi thế của Bayesian Approach
> Cho phép AI **tích hợp prior knowledge** (tri thức tiên nghiệm) — ví dụ: tiếng nói thường hữu thanh ~60% thời gian — để phán đoán xác suất thông minh hơn, thích nghi tốt hơn với các mẫu tiếng nói khác nhau.

### 2.4 Vai Trò của Machine Learning

| Loại ML | Ứng dụng |
|---------|----------|
| **Supervised learning** (SVM, Neural Networks) | Phân loại âm thanh, nhận dạng tiếng nói |
| **Unsupervised learning** | Clustering và segmentation âm thanh |

**Lợi thế ML trong auditory processing:**
- Tự động hóa feature extraction và classification
- Không cần thiết kế thủ công từng đặc trưng

### 2.5 Trích Xuất Đặc Trưng Thính Giác

#### MFCCs (Mel-Frequency Cepstral Coefficients)

- Trích xuất **spectral features** — đặc trưng phổ tần
- Thu thập thông tin tần số theo **log-scale** (giống tai người)
- Đặc trưng quan trọng nhất cho audio classification

#### Spectral Features

| Đặc trưng | Ý nghĩa |
|-----------|---------|
| **Spectral Centroid** | "Trọng tâm" tần số của tín hiệu |
| **Spectral Bandwidth** | Độ rộng của phổ tần |
| **Spectral Rolloff** | Tần số mà dưới đó chứa X% năng lượng |
| **Energy-based features** | Đặc trưng dựa trên năng lượng âm |

> [!tip] Thư viện Python: Librosa
> ```python
> import librosa
> y, sr = librosa.load('audio.wav')
> mfcc = librosa.feature.mfcc(y=y, sr=sr, n_mfcc=13)
> spectrogram = librosa.stft(y)
> ```

### 2.6 Các Mô Hình Thính Giác Nâng Cao

#### Gammatone Filterbank
- Mô phỏng **lọc của cochlea** trong hệ thống thính giác
- Mỗi bộ lọc tương ứng với một dải tần — giống cách cochlea phân tích âm

#### Auditory Nerve Models
- Mô hình hóa **phản ứng thần kinh** với kích thích thính giác
- Dùng để hiểu cách tín hiệu thần kinh mã hóa thông tin âm thanh

### 2.7 Bài Tập Thực Hành

> [!example] Bài tập: Phân loại Speech vs Music
> **Mục tiêu:** Phân loại mẫu âm thanh thành speech hoặc music
>
> **Các bước:**
> 1. Thu thập dataset âm thanh (speech + music recordings)
> 2. Preprocess với Librosa
> 3. Trích xuất MFCC từ các file audio
> 4. Build và train SVM classifier
> 5. Đánh giá bằng accuracy metrics

---

## 3. Speech Perception — Tri Giác Tiếng Nói

### 3.1 Cơ Bản

**Speech perception** là quá trình **diễn giải và hiểu** ngôn ngữ nói. Bao gồm:

- Hệ thống thính giác nhận diện và xử lý âm thanh tiếng nói
- **Phonetics** nghiên cứu phonemes (đơn vị âm thanh riêng biệt) và prosody (ngữ điệu, nhịp, trọng âm)

### 3.2 Trích Xuất Đặc Trưng Tiếng Nói

| Đặc trưng | Mô tả |
|-----------|-------|
| **MFCCs** | Biểu diễn compact của short-term power spectrum — nắm bắt thông tin phonetic |
| **Pitch (F0)** | Tần số sóng âm — biểu thị tông giọng và cảm xúc |
| **Intensity** | Biên độ tín hiệu — thông tin về stress và emphasis |
| **Duration** | Thời gian các phân đoạn âm — ảnh hưởng đến nhịp điệu |

### 3.3 Các Mô Hình Nhận Dạng Tiếng Nói

#### Hidden Markov Models (HMMs)
- Dùng cho **acoustic modeling** và sequence alignment
- Là nền tảng của các hệ thống ASR truyền thống
- Mô hình hóa sự biến đổi thời gian của tiếng nói

#### Deep Learning Models

| Kiến trúc | Đặc điểm |
|-----------|----------|
| **LSTM** | Xử lý chuỗi dài, nhớ ngữ cảnh xa |
| **Transformers** | Attention mechanism — state-of-the-art hiện tại |
| **End-to-end** | Ánh xạ trực tiếp audio features → text sequences |

#### Training Pipeline

```
Audio Input
    │
    ▼
Acoustic Modeling
    → Nắm bắt thông tin phonetic từ audio features
    │
    ▼
Language Modeling
    → Tích hợp ngữ cảnh ngôn ngữ
    → Cải thiện độ chính xác nhận dạng
    │
    ▼
Decoding
    → Align audio features → sequence từ hoặc phonemes
    │
    ▼
Text Output
```

### 3.4 Tích Hợp Speech Features với ML Models

**Implementation workflow (Python):**
1. Transform audio features (MFCCs, prosodic) → input vectors
2. Train ML model (LSTM, CNN) trên labeled speech data
3. Evaluate với **accuracy**, **Word Error Rate (WER)**, **Confusion Matrix**

### 3.5 Bài Tập Thực Hành

> [!example] Bài tập: Xây dựng Speech Recognition System
> **Các bước:**
> 1. **Preprocess audio** — trích xuất MFCCs và prosodic features
> 2. **Implement model** — chọn LSTM, train trên dataset
> 3. **Evaluate** — dùng test data, phân tích error patterns
> 4. **Discuss improvements** — cách tăng robustness và accuracy

---

## Tóm Tắt

```
Âm thanh vào tai
        │ Outer → Middle → Inner Ear (Cochlea)
        ▼
Tín hiệu thần kinh
        │ Auditory Cortex
        ▼
Nhận diện Phonemes → Từ → Câu
        │ Higher Cognitive Processing
        ▼
Hiểu ngôn ngữ
```

| Khái niệm | Vai trò |
|-----------|---------|
| **Cochlea** | "Bộ phân tích tần số" sinh học — cơ sở của thang Mel |
| **MFCCs** | Đặc trưng mô phỏng cách tai người nghe |
| **Gammatone Filterbank** | Mô hình hóa bộ lọc cochlea |
| **HMM** | Nền tảng ASR truyền thống |
| **LSTM/Transformer** | State-of-the-art trong nhận dạng tiếng nói |

---

## Liên Kết

- [[Chapter 3]] — Human Speech Production
- [[Chapter 6]] — Frequency-Domain Representations
- [[MFCCs]]
- [[ASR Pipeline]]
- [[HMM]]
- [[STFT]]

---

*Chapter 4 · Hearing, Auditory Models & Speech Perception · Tự học*
