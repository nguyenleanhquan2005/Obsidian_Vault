---
tags:
  - speech-processing
  - digital-signal
  - chapter-1
aliases:
  - DSP Chapter 1
  - Intro Speech Processing
date: 2026-03-24
status: complete
---

# Chapter 1 — Introduction to Digital Speech Processing

> [!abstract] Tóm tắt chương
> Chương này giới thiệu nền tảng của Digital Speech Processing: bản chất tín hiệu tiếng nói, quá trình số hóa, các phương pháp phân tích, và các ứng dụng thực tế quan trọng.

---

## 1. Tổng Quan (Overview)

**Xử lý tiếng nói kỹ thuật số** (Digital Speech Processing) là lĩnh vực nghiên cứu cách máy tính **thu nhận, phân tích, biểu diễn và tổng hợp** tiếng nói của con người.

Đây là nền tảng của nhiều ứng dụng hiện đại như:
- Trợ lý giọng nói (Voice Assistant)
- Nhận dạng tiếng nói (Speech Recognition)
- Chuyển văn bản thành giọng nói (Text-to-Speech)

**1. Ứng dụng tiêu biểu của DSP (Câu 109)**

- **Đáp án A:** Tất cả các kỹ thuật STFT, LPC, Cepstrum cuối cùng đều phục vụ cho một ứng dụng khổng lồ: **Hệ thống nhận dạng giọng nói (Voice recognition systems)**. Nó là tinh hoa của ngành Xử lý tín hiệu số (DSP).
---

## 2. Tín Hiệu Tiếng Nói (Speech Signal)

Tín hiệu tiếng nói là một **dạng sóng thay đổi theo thời gian** (time-varying waveform), truyền đi dưới dạng **sóng áp suất trong không khí**. Nó mang thông tin ngôn ngữ qua ba thành phần cơ bản:

```
Speech Signal
├── Phonemes (Âm vị)
├── Syllables (Âm tiết)
└── Prosodic Features (Đặc trưng ngữ điệu)
```

### 2.1 Âm Vị (Phonemes)

> Đơn vị âm thanh **nhỏ nhất có khả năng phân biệt nghĩa** trong một ngôn ngữ.

Âm vị không phải âm thanh vật lý cụ thể — chúng là những "loại âm" **trừu tượng** trong tâm trí người nói.

| Ngôn ngữ | Ví dụ |
|----------|-------|
| Tiếng Việt | /b/, /t/, /s/ → **ba** ≠ **ta** ≠ **sa** |
| Tiếng Anh | /p/ vs /b/ → **pit** ≠ **bit** |

### 2.2 Âm Tiết (Syllables)

Âm tiết là đơn vị tổ chức âm thanh **lớn hơn âm vị**, có cấu trúc 3 phần:

$$\text{Syllable} = \underbrace{\text{Onset}}_{\text{phụ âm đầu}} + \underbrace{\text{Nucleus}}_{\text{nguyên âm}} + \underbrace{\text{Coda}}_{\text{phụ âm cuối}}$$

> [!example] Ví dụ
> **"cat"** → Onset: /k/ | Nucleus: /æ/ | Coda: /t/

### 2.3 Đặc Trưng Ngữ Điệu (Prosodic Features)

| Đặc trưng | Mô tả | Vai trò |
|-----------|-------|---------|
| **Pitch (F0)** | Tần số dao động sóng âm | Tông giọng, cảm xúc — pitch ↑ ở cuối câu hỏi |
| **Intensity** | Mức năng lượng âm thanh | Trọng âm (stress), nhấn mạnh |
| **Duration** | Thời gian phát âm | Nhịp điệu (rhythm), tốc độ nói |
| **Pauses** | Khoảng ngắt nghỉ | Phân chia cụm từ, giải mơ hồ ngữ pháp |
![[Pasted image 20260324001646.png]]
---

## 3. Analog vs. Digital Speech

### So Sánh

| Tiêu chí | Analog | Digital |
|----------|--------|---------|
| **Định nghĩa** | Âm thanh tự nhiên, liên tục | Phiên bản số hóa |
| **Loại tín hiệu** | Liên tục (time & amplitude) | Rời rạc (discrete) |
| **Dạng sóng** | Làn sóng mượt | Tập hợp điểm mẫu |
| **Lưu trữ** | Không lưu trực tiếp được | Binary numbers |
| **Xử lý** | Khó xử lý bằng máy tính | Dễ xử lý, chỉnh sửa, truyền |
| **Độ chính xác** | Chính xác tuyệt đối | Phụ thuộc sampling & quantization |
| **Ví dụ** | Micro analog, giọng nói thật | MP3, WAV, âm thanh smartphone |

### 3.1 Quy Trình Số Hóa

```
Analog Signal
     │
     ▼
┌─────────────┐
│  Sampling   │  → Lấy mẫu: tín hiệu liên tục → rời rạc
└─────────────┘
     │
     ▼
┌──────────────────┐
│  Quantization    │  → Lượng tử hóa: biên độ → giá trị số
└──────────────────┘
     │
     ▼
  Digital Signal (Binary)
```

> [!info] Định lý Nyquist
> Tần số lấy mẫu phải **≥ 2× tần số cao nhất** của tín hiệu.
> Với tiếng nói người (< 8 kHz) → tần số lấy mẫu tối thiểu = **16 kHz**

**Bit depth (độ sâu bit):** 8-bit → 16-bit → 24-bit → độ chính xác tăng dần.

---

## 4. Cách Tiếng Nói Được Truyền Đi

Tiếng nói truyền dưới dạng **sóng áp suất** trong không khí. Phân tích phổ tần số cho thấy hai thành phần:

- **Formants** — vùng năng lượng tập trung trong phổ → đặc trưng cho nguyên âm
- **Harmonics** — bội số của F0 → tạo nên âm sắc (timbre) của giọng nói

---

## 5. Trích Xuất Đặc Trưng (Feature Extraction)

> Chuyển đổi tín hiệu thô → đặc trưng có ý nghĩa để máy tính học và nhận dạng.

### 5.1 Short-Time Energy

- Đo **năng lượng tín hiệu** trong các khung thời gian ngắn
- Dùng để phân biệt **voiced** (có tiếng nói) vs **silence/unvoiced**

### 5.2 Zero Crossing Rate (ZCR)

- Đếm số lần tín hiệu **đổi dấu** (qua 0) trong một frame
- `ZCR thấp` → âm hữu thanh (voiced)
- `ZCR cao` → âm vô thanh (unvoiced)

### 5.3 MFCCs (Mel Frequency Cepstral Coefficients)

> [!important] Quan trọng nhất
> MFCCs là đặc trưng **quan trọng nhất** trong nhận dạng tiếng nói — hoạt động như "fingerprint" của giọng nói.

- Mô phỏng cách **tai người** cảm nhận âm thanh (thang Mel — phi tuyến)
- Nắm bắt đặc trưng phổ tần hiệu quả
- Dùng rộng rãi trong **ASR** và **Speaker Identification**

---

## 6. Phân Tích Tần Số

### 6.1 Fourier Transform

Phân tách tín hiệu thành các **thành phần tần số** — cho biết tần số nào có trong tín hiệu và với cường độ bao nhiêu. Đây là nền tảng phân tích phổ âm thanh.

### 6.2 Short-Time Fourier Transform (STFT)

Vì tiếng nói **thay đổi theo thời gian**, ta chia nhỏ tín hiệu thành các frame ngắn rồi phân tích từng frame → theo dõi sự thay đổi tần số theo thời gian.

```
Tín hiệu dài → [frame 1] [frame 2] [frame 3] ... → FFT từng frame → STFT
```

### 6.3 Spectrogram

**Spectrogram** = biểu diễn 2D trực quan của time-frequency content:

| Trục | Biểu diễn |
|------|-----------|
| Trục X | Thời gian |
| Trục Y | Tần số |
| Màu sắc | Cường độ năng lượng |

> [!tip] Ghi nhớ
> Spectrogram = "dấu vân tay hình ảnh" của tiếng nói

---

## 7. Speech Processing Stack

Toàn bộ pipeline xử lý tiếng nói:

```
[Microphone]
     │  Thu tín hiệu
     ▼
[Signal Acquisition]  ← Noise reduction, amplification, filtering
     │
     ▼
[Signal Processing]   ← Beamforming, Echo Cancellation
     │
     ▼
[Feature Extraction]  ← MFCCs, ZCR, Short-Time Energy
     │
     ▼
[ASR / NLP]           ← Acoustic model + Language model
     │
     ▼
[Dialog Management]   ← Intent, context, response
     │
     ▼
[TTS Output]          ← Text → Speech
```

### 7.1 Thu Nhận Tín Hiệu

| Loại Micro | Đặc điểm | Dùng khi |
|------------|----------|----------|
| Condenser | Nhạy, chất lượng cao | Studio, hội nghị |
| Dynamic | Bền, ít nhạy với noise | Ngoài trời |

**Preprocessing:** Noise reduction → Signal amplification → Filtering

### 7.2 Xử Lý Tín Hiệu

- **Beamforming** — tập trung vào nguồn tiếng nói, loại bỏ nhiễu từ hướng khác
- **Echo Cancellation** — loại bỏ vọng âm (quan trọng trong video call)

### 7.3 NLP Layer

- **Syntax & Semantics** — phân tích cú pháp, hiểu nghĩa câu nói
- **Dialog Management** — duy trì ngữ cảnh hội thoại qua nhiều lượt

---

## 8. Thách Thức

> [!warning] Các vấn đề thực tế
> - **Noise & Distortion** — tiếng ồn môi trường làm giảm chất lượng và độ rõ ràng
> - **Variability** — khác biệt về giọng, tốc độ nói, phong cách giữa người dùng
> - **Speaker & Language Variations** — cần thích nghi với nhiều ngôn ngữ và giọng địa phương

---

## 9. Ứng Dụng (Applications)

### Tổng Quan

| Ứng dụng | Mô tả | Ví dụ |
|----------|-------|-------|
| **ASR** | Giọng nói → Văn bản | Google STT, Whisper |
| **TTS** | Văn bản → Giọng nói | WaveNet, ElevenLabs |
| **Speaker ID** | Nhận diện người nói | Ngân hàng số, điểm danh |
| **Voice Assistant** | ASR + NLP + TTS | Siri, Alexa, Google Assistant |

### 9.1 Automatic Speech Recognition (ASR)

Chuyển **giọng nói → văn bản** theo thời gian thực.

```
Audio → Acoustic Model → Phonemes → Language Model → Text
```

- Kết hợp **acoustic model** (mô hình âm học) + **language model** (mô hình ngôn ngữ)
- Hệ thống hiện đại dùng deep learning: **Wav2Vec**, **Whisper** — độ chính xác rất cao

### 9.2 Text-to-Speech (TTS)

Tổng hợp **giọng nói tự nhiên từ văn bản**. Hai kỹ thuật chính:

| Kỹ thuật | Cách hoạt động | Ưu/Nhược |
|----------|---------------|----------|
| **Concatenative** | Ghép nối đoạn ghi sẵn | Đơn giản, thiếu tự nhiên |
| **Parametric** | Mô hình hóa vocal tract | Linh hoạt, phức tạp hơn |

> [!note]
> **WaveNet** (Google) dùng neural network — tạo giọng gần như không phân biệt được với người thật.

### 9.3 Speaker Identification

Nhận diện danh tính người nói qua **voiceprint** — đặc trưng giọng độc nhất như dấu vân tay.

**Ứng dụng:** Xác thực ngân hàng số · Kiểm soát an ninh · Điểm danh tự động

### 9.4 Voice Assistant & Dialog Systems

Ứng dụng phức tạp nhất — kết hợp **toàn bộ speech stack**:

```
ASR (nghe) → NLP (hiểu) → Dialog Mgmt (phản hồi) → TTS (nói)
```

**Ví dụ:** Amazon Alexa · Google Assistant · Siri · ChatGPT Voice

---

## Tóm Tắt

```
Tín hiệu tiếng nói
    ↓ Số hóa (Sampling + Quantization)
Digital Signal
    ↓ Trích xuất đặc trưng (MFCC, ZCR, Energy)
Features
    ↓ Phân tích (STFT, Spectrogram)
Representations
    ↓ Ứng dụng
ASR · TTS · Speaker ID · Voice Assistant
```

---

## Liên Kết

- [[Chapter 2]] — (tiếp theo)
- [[MFCC]]
- [[Fourier Transform]]
- [[ASR Pipeline]]

---

*Chapter 1 · Digital Speech Processing · Tự học*
