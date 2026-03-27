---
tags:
  - speech-processing
  - phonetics
  - chapter-3
aliases:
  - Human Speech Production
  - Quá trình phát âm
date: 2026-03-24
status: complete
---

# Chapter 3 — Human Speech Production

> [!abstract] Tóm tắt chương
> Chương này giải thích cơ chế sinh lý và thần kinh của quá trình tạo ra tiếng nói, bao gồm giải phẫu bộ máy phát âm, phân tích STFT, âm vị học âm học, và các đặc trưng phân biệt âm vị tiếng Anh.

---

## Bản đồ nội dung

```
Human Speech Production
├── 1. Quá trình phát âm
│   ├── Giải phẫu (Respiratory, Phonatory, Articulatory)
│   ├── Quá trình phát âm (Phonation)
│   ├── Khớp âm (Articulation)
│   ├── Điều khiển thần kinh (Neural Control)
│   └── Các giai đoạn phát âm
├── 2. Short-Time Fourier Representation
│   ├── STFT là gì
│   └── Ứng dụng phân tích tiếng nói
├── 3. Âm vị học âm học (Acoustic Phonetics)
│   ├── F0, Formants (định nghĩa & cơ chế)
│   ├── Spectral characteristics
│   ├── Phân tích nguyên âm & phụ âm
│   └── Frequency Theory vs Place Theory ★
└── 4. Đặc trưng phân biệt âm vị tiếng Anh
    ├── Voicing, Place, Manner
    ├── Nasality
    └── Vowel Height & Backness
```

---

## 1. Quá Trình Phát Âm (Speech Production)

### 1.1 Định Nghĩa

**Speech production** là quá trình con người tạo ra ngôn ngữ nói thông qua sự phối hợp của nhiều cơ quan giải phẫu. Hiểu quá trình này quan trọng cho:
- Nghiên cứu **rối loạn ngôn ngữ** (speech disorders)
- Thiết kế **công nghệ tiếng nói** (ASR, TTS)
- Cải thiện **học ngôn ngữ và giao tiếp**

### 1.2 Giải Phẫu Bộ Máy Phát Âm

Ba hệ thống phối hợp với nhau:

| Hệ thống | Bộ phận | Chức năng |
|----------|---------|-----------|
| **Respiratory** (Hô hấp) | Cơ hoành, cơ liên sườn, phổi, khí quản | Kiểm soát luồng khí từ phổi lên vocal tract |
| **Phonatory** (Phát âm) | Thanh quản (larynx), dây thanh (vocal folds) | Dây thanh rung khi khí đi qua → tạo âm hữu thanh |
| **Articulatory** (Khớp âm) | Lưỡi, môi, răng, vòm miệng, hàm | Định hình luồng khí thành các âm cụ thể |

### 1.3 Quá Trình Phát Âm (Phonation)

**Glottis** là khe hở giữa hai dây thanh. Phonation xảy ra khi dây thanh rung do luồng khí đi qua.

**Ba kiểu phát âm:**
- **Modal voice** — phát âm bình thường
- **Breathy voice** — luồng khí tăng, giọng thở
- **Creaky voice** — luồng khí giảm, giọng khàn/rè

### 1.4 Khớp Âm (Articulation)

Các **articulators** (môi, lưỡi, răng, vòm miệng, hàm) định hình vocal tract để tạo các âm khác nhau. Âm được phân loại theo:

- **Place of articulation** — vị trí tắc nghẽn: bilabial, alveolar, velar...
- **Manner of articulation** — cách tạo âm: stops, fricatives, nasals...

### 1.5 Điều Khiển Thần Kinh (Neural Control)

| Vùng não | Chức năng |
|----------|-----------|
| **Motor Cortex** | Lập kế hoạch và thực thi vận động tự nguyện, bao gồm khớp âm |
| **Broca's Area** (thùy trán) | Lập kế hoạch vận động trong phát âm |
| **Cerebellum** | Phối hợp và tinh chỉnh vận động — đảm bảo khớp âm chính xác |
| **Brainstem** | Điều phối cơ bắp qua các dây thần kinh sọ não |

### 1.6 Các Giai Đoạn Phát Âm

```
[Conceptualization]
Hình thành ý tưởng ngôn ngữ,
chọn từ và câu phù hợp
        │
        ▼
[Motor Planning]
Tín hiệu thần kinh chuyển
biểu diễn ngôn ngữ → lệnh
vận động cho bộ máy phát âm
        │
        ▼
[Motor Execution]
Các cơ trong vocal tract
thực thi chuyển động chính
xác để tạo ra tiếng nói
```

---

## 2. Short-Time Fourier Representation of Speech

### 2.1 Tại Sao Cần STFT?

Tiếng nói là tín hiệu **non-stationary** — đặc tính tần số thay đổi theo thời gian. Fourier Transform thông thường chỉ cho thấy phổ **toàn cục**, không biết tần số đó xuất hiện **khi nào**.

**STFT (Short-Time Fourier Transform)**. We divide the signal into **short overlapping segments** (frames) to analyze the **frequency content over short time intervals** where the vocal tract is assumed to be stationary (not moving).
- **Math:** $$X_n(e^{j\omega}) = \sum_{m=-\infty}^{\infty} x[m]w[n-m]e^{-j\omega m}$$ (where $w[n-m]$ is the sliding window).


**STFT** giải quyết bằng cách:
1. Chia tín hiệu thành các đoạn ngắn (frames)
2. Áp dụng Fourier Transform cho từng frame
3. Ghép lại → có được **time-varying frequency content**

### 2.2 Ứng Dụng STFT trong Speech Processing

- **Speech recognition** — nhận dạng tiếng nói
- **Speaker identification** — nhận diện người nói
- **Speech enhancement** — tăng cường chất lượng tiếng nói

> [!tip] Thực hành Python
> **Thư viện cần:** NumPy, SciPy, Matplotlib
> **Các bước:** Load file WAV → Windowing → Tính STFT → Vẽ spectrogram

---

## 3. Âm Vị Học Âm Học (Acoustic Phonetics)

### 3.1 Định Nghĩa

**Acoustic phonetics** — thay vì nghiên cứu ngữ âm học theo kiểu ngôn ngữ học trừu tượng, acoustic phonetics phân tích trực tiếp sóng âm thông qua các thuộc tính vật lý: **Tần số (Frequency)**, Biên độ, và Phổ.

### 3.2 Các Đặc Trưng Âm Học Chính

| Đặc trưng | Mô tả | Đơn vị |
|-----------|-------|--------|
| **F0 (Fundamental Frequency)** | Tốc độ rung của dây thanh — cảm nhận là độ cao giọng (pitch) | Hz |
| **Formants (F1, F2, F3)** | Tần số cộng hưởng của vocal tract — đặc trưng nguyên âm | Hz |
| **Spectral Characteristics** | Mẫu phổ đặc trưng của từng âm do cộng hưởng vocal tract | — |

### 3.2.1 Formant — "Dấu Vân Tay" Của Nguyên Âm

> [!important] Định nghĩa chuẩn
> **Formant** ($F_1, F_2, F_3...$) là các **tần số cộng hưởng của vocal tract** (resonance frequencies of the vocal tract).

**1. Formant là gì? (Câu 38)**

- **Đáp án:** Formant chính là **tần số cộng hưởng của tuyến âm (resonance frequency of the vocal tract)**.
- **Vật lý thực tiễn:** Hãy tưởng tượng thanh quản của bạn là một cái ống nhựa. Khi bạn đổi khẩu hình miệng để phát âm chữ /A/ hay /I/, bạn đang bóp méo cái ống đó, tạo ra các dải tần số cộng hưởng khác nhau ($F_1, F_2, F_3$). LPC sinh ra là để tìm các Formant này.

**Cơ chế hoạt động:**
- Dây thanh chỉ tạo ra **âm gốc (Pitch)**
- Khoang miệng/lưỡi/mũi uốn éo → khuếch đại các dải tần số khác nhau → đó là **Formant**

> [!example] Ví dụ thực tế
> Khi nói /A/ hay /I/, dây thanh rung **giống hệt nhau** (cùng Pitch). Nhưng do thay đổi khẩu hình (uốn lưỡi, mở môi), khoang miệng khuếch đại các dải tần khác nhau → tạo ra Formant khác nhau. **Siri phân biệt "Cat" và "Cut" hoàn toàn dựa vào Formant** (trích xuất qua MFCC).

### 3.3 Kỹ Thuật Đo Lường

- **Waveform analysis** — biên độ theo thời gian (time domain)
- **Spectrogram analysis** — phân bố năng lượng theo tần số-thời gian
- **Pitch & Formant analysis** — phân tích F0 và các formant qua kỹ thuật phổ

### 3.4 Âm Học Nguyên Âm (Vowels)

Nguyên âm được đặc trưng bởi **mẫu hình formant**:

| Nguyên âm | F1 | F2 | Ví dụ |
|-----------|----|----|-------|
| /i/ (high front) | Thấp | Cao | "see" |
| /a/ (low back) | Thấp hơn | Cao | "father" |
| /u/ (high back) | Thấp | Thấp | "boot" |

### 3.5 Âm Học Phụ Âm (Consonants)

Phụ âm phân biệt nhau qua:
- **Place of articulation** — thay đổi phổ tần do vị trí tắc nghẽn (/p/ vs /t/ vs /k/)
- **Manner of articulation** — đặc trưng thời gian và phổ (stops, fricatives, nasals)

### 3.6 Thuyết Thính Giác: Frequency Theory vs Place Theory

Làm thế nào con người phân biệt âm trầm và âm bổng? Não dùng **hai thuyết song song**:

| Thuyết | Cơ chế | Áp dụng cho |
|--------|--------|-------------|
| **Place Theory** (Thuyết Vị trí) | Tần số khác nhau → rung ở **vị trí khác nhau** trên màng nền ốc tai | Âm bổng (> 1000 Hz) |
| **Frequency Theory / Volley Theory** (Thuyết Tần số) | Tần số được mã hóa bằng **tốc độ bắn tín hiệu (firing rate)** của dây thần kinh thính giác | Âm trầm (< 1000 Hz) |

> [!example] Ví dụ trực quan — Frequency Theory
> Âm thanh 100 Hz vào tai → dây thần kinh "bắn" xung điện lên não đúng **100 lần/giây**.

> [!warning] Điểm yếu của Place Theory
> Place Theory **không thể giải thích** cách nghe âm trầm rất thấp (dưới ~50 Hz) vì màng nền quá cứng ở vùng đó. Đây là lúc Volley Theory bù vào.

### 3.7 Xu Hướng Nghiên Cứu

- **Machine learning & Deep learning** đang thay đổi nghiên cứu acoustic phonetics
- **Multimodal approaches** — kết hợp dữ liệu âm học với articulatory và linguistic
- Nghiên cứu **cross-linguistic**, **speech synthesis**, **neurophonetics**

- **Bản chất Ngữ âm học (Acoustic Phonetics):** Trong ngữ âm học âm hưởng, các phụ âm được phân biệt với nhau bằng các tín hiệu âm thanh đặc thù dựa trên hai hệ quy chiếu chính: **vị trí cấu âm (place of articulation)** và **phương thức cấu âm (manner of articulation)**.
- **Vai trò của Voicing:** "Voicing" (đặc tính hữu thanh/vô thanh) là một trong những đặc trưng phân loại (distinctive feature) quan trọng nhất thuộc phương thức cấu âm. Đặc trưng này chỉ ra việc dây thanh đới có rung hay không rung trong quá trình luồng khí đi qua để tạo ra phụ âm

---

## 4. Đặc Trưng Phân Biệt Âm Vị Tiếng Anh

**Distinctive features** là các thuộc tính cụ thể của âm thanh dùng để **phân biệt các phoneme** trong một ngôn ngữ.

### 4.1 Voicing (Hữu Thanh / Vô Thanh)

Dây thanh có rung không trong khi phát âm?

| Loại | Ví dụ | Cặp tối thiểu |
|------|-------|--------------|
| Voiced (hữu thanh) | /b/, /z/ | "bat" /bæt/ |
| Voiceless (vô thanh) | /p/, /s/ | "pat" /pæt/ |

### 4.2 Place of Articulation (Vị Trí Khớp Âm)

Luồng khí bị cản ở đâu trong vocal tract?

| Vị trí | Âm | Ví dụ |
|--------|-----|-------|
| **Bilabial** (hai môi) | /p/, /b/ | "pat" |
| **Alveolar** (chân răng) | /t/, /d/ | "tat" |
| **Velar** (vòm mềm) | /k/, /g/ | "cat" |

### 4.3 Manner of Articulation (Cách Khớp Âm)

Luồng khí bị điều chỉnh như thế nào?

| Cách | Âm | Đặc điểm |
|------|-----|----------|
| **Stops** | /p/, /t/, /k/ | Tắc hoàn toàn rồi bật ra |
| **Fricatives** | /f/, /s/, /ʃ/ | Ma sát liên tục |
| **Affricates** | /tʃ/, /dʒ/ | Stop + Fricative |
| **Nasals** | /m/, /n/, /ŋ/ | Khí qua khoang mũi |

### 4.4 Nasality (Mũi Tính)

Khí có đi qua khoang mũi không?
- **Nasal** (/m/, /n/, /ŋ/): "man" /mæn/
- **Oral** (/b/, /d/): "pan" /pæn/

### 4.5 Vowel Height & Backness (Chiều Cao & Chiều Sâu Nguyên Âm)

**Vowel Height** — vị trí lưỡi theo chiều dọc:

| Độ cao | Âm | Ví dụ |
|--------|-----|-------|
| High | /i/, /u/ | "see", "boot" |
| Mid | /ɛ/, /ʌ/ | "bed", "but" |
| Low | /æ/, /ɑ/ | "cat", "father" |

**Vowel Backness** — vị trí lưỡi theo chiều trước-sau:

| Vị trí | Âm | Ví dụ |
|--------|-----|-------|
| Front | /i/, /ɛ/ | "see", "bed" |
| Central | /ʌ/, /ə/ | "but", "about" |
| Back | /u/, /ɔ/ | "boot", "thought" |

### 4.6 Rhoticity (Âm R)

Sự có mặt hay vắng mặt của /r/ trong phát âm nguyên âm:

| Phương ngữ | Ví dụ | Phiên âm |
|-----------|-------|----------|
| American English (rhotic) | "car" | /kɑr/ |
| British English (non-rhotic) | "car" | /kɑː/ |

---

## Tóm Tắt

```
Ý tưởng ngôn ngữ
        │ Neural Control (Motor Cortex, Broca's Area)
        ▼
Lệnh vận động → Cơ bắp thực thi
        │ Respiratory + Phonatory + Articulatory
        ▼
Tín hiệu tiếng nói (Speech Signal)
        │ Acoustic Analysis
        ▼
F0 · Formants · Spectral Features
        │ STFT / Spectrogram
        ▼
Phân tích & Nhận dạng âm vị
```

---

## Liên Kết

- [[Chapter 2]] — DSP Fundamentals
- [[Chapter 4]] — Hearing & Auditory Models
- [[Chapter 6]] — Frequency-Domain Representations
- [[STFT]]
- [[Phonemes]]
- [[Formants]]

---

*Chapter 3 · Human Speech Production · Tự học*
