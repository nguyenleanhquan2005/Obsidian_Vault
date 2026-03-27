---
tags:
  - speech-processing
  - cepstrum
  - homomorphic
  - chapter-8
aliases:
  - Cepstrum
  - Homomorphic Speech Processing
  - Phân Tích Cepstrum
date: 2026-03-24
status: complete
---

# Chapter 8 — The Cepstrum and Homomorphic Speech Processing

> [!abstract] Tóm tắt chương
> Cepstrum là một trong những kỹ thuật phân tích tiếng nói mạnh nhất — tách riêng thông tin vocal tract (formants) và glottal excitation (pitch) ra khỏi nhau, việc mà phổ thông thường không làm được. Homomorphic processing cung cấp nền tảng toán học tổng quát cho kỹ thuật này.

---

## Bản đồ nội dung

```
The Cepstrum and Homomorphic Speech Processing
├── 1. Mô Hình Tiếng Nói — Source-Filter Model
│   └── Convolution trong time domain ↔ Add trong cepstral domain
├── 2. Homomorphic Systems for Convolution
│   ├── Định nghĩa & nguyên lý
│   └── Complex Cepstrum
├── 3. Cepstrum — Định Nghĩa & Tính Toán
│   ├── Real Cepstrum
│   ├── Complex Cepstrum
│   └── Quefrency domain
├── 4. Short-Time Cepstrum
│   └── Ứng dụng phân tích tiếng nói
├── 5. Liftering — Tách Pitch và Vocal Tract
│   ├── Low-time lifter → Vocal tract
│   └── High-time lifter → Pitch
├── 6. Cepstrum Distance Measures
│   └── Ứng dụng trong ASR, Speaker ID
└── 7. MFCCs — Ứng dụng Thực Tế Của Cepstrum
```

---

## 1. Mô Hình Tiếng Nói — Source-Filter Model

### 1.1 Speech = Excitation ✱ Vocal Tract

Tiếng nói được tạo ra bởi **tích chập (convolution)** của hai thành phần:

$$s[n] = e[n] * h[n]$$

- $e[n]$: **Excitation** (nguồn kích thích từ glottis) — mang thông tin **Pitch**
- $h[n]$: **Vocal tract impulse response** — mang thông tin **Formants/Vowel identity**

```
e[n] (Excitation)     h[n] (Vocal Tract)      s[n] (Speech)
  Pitch pulses    *    Formant filter      =    Tiếng nói
  (periodic)           (IIR filter)
```

### 1.2 Vấn Đề: Tách Hai Thành Phần

**Bài toán:** Từ $s[n]$ (đã observe), tách riêng $e[n]$ và $h[n]$.

Trong miền tần số: $S(\omega) = E(\omega) \cdot H(\omega)$ — tích, không phải tổng → khó tách.

**Giải pháp:** Chuyển sang miền **cepstrum** — biến tích thành tổng → tách dễ dàng!

---

## 2. Homomorphic Systems for Convolution

### 2.1 Nguyên Lý Homomorphic

**Homomorphic system** là hệ thống biến đổi một phép toán thành phép toán khác:

$$\mathcal{D}_*: \text{Convolution} \rightarrow \text{Addition}$$

```
x₁[n] * x₂[n]
       │
       ▼ Characteristic system D*
x̂₁[n] + x̂₂[n]
       │
       ▼ Linear filter (trong quefrency domain)
       │
       ▼ Inverse characteristic system D*⁻¹
Tách riêng x₁[n] hoặc x₂[n]
```

### 2.2 Complex Cepstrum — Cơ Sở Toán Học

**Complex cepstrum** $\hat{x}[n]$ của tín hiệu $x[n]$:

$$\hat{x}[n] = \mathcal{F}^{-1}\{\log X(\omega)\} = \mathcal{F}^{-1}\{\log|X(\omega)| + j\angle X(\omega)\}$$

**Tính chất quan trọng:**

$$\widehat{x_1 * x_2}[n] = \hat{x}_1[n] + \hat{x}_2[n]$$

→ Convolution trong time domain = **Cộng** trong cepstral domain!

---

## 3. Cepstrum — Định Nghĩa & Tính Toán

### 3.1 Real Cepstrum (Cepstrum Thực)

$$c[n] = \mathcal{F}^{-1}\{\log|X(\omega)|\}$$

- Chỉ dùng log-magnitude spectrum (bỏ phase)
- Đơn giản hơn complex cepstrum
- Đủ cho nhiều ứng dụng (pitch detection, MFCC)

### 3.2 Quefrency Domain

> [!info] Tên gọi đặc biệt
> Miền của cepstrum được gọi là **"quefrency"** (anagram của "frequency"). Đơn vị là **giây (seconds)** — như thời gian, không phải tần số.

| Time domain | Frequency domain | Quefrency domain (Cepstral) |
|-------------|-----------------|--------------------------|
| $x[n]$ | $X(\omega)$ | $c[n]$ |
| Convolution | Multiplication | Addition |
| Filter | Transfer function | **Lifter** |
| Filtering | Windowing | **Liftering** |

### 3.3 Quy Trình Tính Real Cepstrum

```
x[n]
  │
  ▼ DFT
X[k]
  │
  ▼ |·| (magnitude)
|X[k]|
  │
  ▼ log
log|X[k]|
  │
  ▼ IDFT
c[n]  ← Real Cepstrum
```

---

## 4. Short-Time Cepstrum

### 4.1 Tại Sao Cần Short-Time?

Vì tiếng nói **non-stationary** → chia thành frames ngắn (~20ms) rồi tính cepstrum từng frame:

$$c_{\hat{n}}[k] = \mathcal{F}^{-1}\left\{\log\left|\mathcal{F}\{x[\hat{n}+m] \cdot w[m]\}\right|\right\}$$

### 4.2 Cấu Trúc Của Short-Time Cepstrum

Trong quefrency domain, cepstrum của tiếng nói có cấu trúc rõ ràng:

```
|c[n]|
  ↑
  │  Vocal tract info        Excitation (Pitch)
  │  (smooth envelope)       (periodic spikes)
  │  ██████                      │
  │  ██████                      ▼
  │  ██████          ...........│...........
  └──────────────────────────────────────→ Quefrency (ms)
     0      Low-time           High-time
            (< ~2ms)           (≈ 1/F0 ≈ 5-10ms)
```

---

## 5. Liftering — Tách Pitch và Vocal Tract

### 5.1 Low-Time Lifter (Vocal Tract)

Nhân với **cửa sổ low-time** trong quefrency domain → giữ thành phần tần thấp → **chỉ còn vocal tract info (formants)**:

$$\hat{c}_{VT}[n] = c[n] \cdot l_{low}[n]$$

### 5.2 High-Time Lifter (Pitch/Excitation)

Nhân với **cửa sổ high-time** → giữ thành phần tần cao → **chỉ còn pitch/excitation info**:

$$\hat{c}_{exc}[n] = c[n] \cdot l_{high}[n]$$

> [!example] Ứng dụng: Pitch Detection bằng Cepstrum
> Peak trong vùng high-quefrency (~5–10 ms) tương ứng với **pitch period** $T_0 = 1/F_0$. Đây là một trong những phương pháp pitch detection chính xác nhất!

### 5.3 Tóm Tắt Liftering

```
c[n] (full cepstrum)
  │
  ├──→ × l_low[n]  →  c_VT[n]  →  IFFT → |H(ω)|  → Formants
  │
  └──→ × l_high[n] →  c_exc[n] →  Pitch period T₀ = argmax
```

---

## 6. Cepstrum Distance Measures

### 6.1 Tại Sao Cần Distance Measures?

Trong **ASR** và **Speaker Recognition**, cần đo "khoảng cách" giữa hai đặc trưng cepstral:

$$d(c_1, c_2) = \sqrt{\sum_{k=1}^{p} (c_1[k] - c_2[k])^2}$$

### 6.2 Weighted Cepstral Distance

Trọng số $w_k$ tăng độ chính xác:

$$d_w(c_1, c_2) = \sqrt{\sum_{k=1}^{p} w_k (c_1[k] - c_2[k])^2}$$

**Ứng dụng:**
- **ASR:** So sánh acoustic model với observed features
- **Speaker ID:** Đo khoảng cách giữa voiceprints
- **Speech coding:** Đánh giá chất lượng codec

---

## 7. MFCCs — Ứng Dụng Thực Tế Của Cepstrum

**MFCCs (Mel-Frequency Cepstral Coefficients)** là phiên bản thực tế của cepstrum, được thiết kế dựa trên mô hình thính giác:

```
Speech frame
    │
    ▼ DFT → Power Spectrum
    │
    ▼ Mel Filterbank (24-40 filters, log scale)
       (mô phỏng Critical Bands của tai người)
    │
    ▼ Log
    │
    ▼ DCT (≈ Real Cepstrum nhưng rời rạc, hữu hạn)
    │
    ▼ MFCCs [c₀, c₁, ..., c₁₂]
```

**Tại sao MFCCs thay thế raw cepstrum trong thực tế:**
- Mel scale → mô phỏng tai người tốt hơn
- DCT → decorrelate các hệ số (tốt cho Gaussian models)
- Finite, low-dimensional → tính toán hiệu quả

> [!info] Liên hệ với Cepstrum
> MFCCs về bản chất là **cepstrum của log mel-filterbank output** — một biến thể thực tế và mô hình thính giác hơn của real cepstrum.

---

## Tóm Tắt

```
Speech s[n] = e[n] * h[n]
                │
                ▼ log|FFT|
       log|S(ω)| = log|E(ω)| + log|H(ω)|
                │
                ▼ IFFT
    c[n] = ĉ_exc[n] + ĉ_VT[n]  (cộng trong quefrency)
                │
    ┌───────────┴────────────┐
    ▼                        ▼
Low-time lifter          High-time lifter
    │                        │
Vocal tract info          Pitch period
(Formants)                (F0 = 1/T₀)
```

| Khái niệm | Ý nghĩa |
|-----------|---------|
| **Cepstrum** | IFFT của log-magnitude spectrum |
| **Quefrency** | Trục của cepstrum (đơn vị: giây) |
| **Lifter** | "Bộ lọc" trong quefrency domain |
| **Low-time lifter** | Tách vocal tract (formants) |
| **High-time lifter** | Tách pitch/excitation |
| **MFCCs** | Cepstrum + Mel scale + DCT (thực tế nhất) |

---

## Liên Kết

- [[Chapter 7]] — Frequency-Domain Representations (STFT, Spectrogram)
- [[Chapter 9]] — Linear Predictive Analysis (LPC, Formants)
- [[Chapter 10]] — Algorithms for Estimating Speech Parameters (Pitch, Formant estimation)
- [[Chapter 5]] — Sound Propagation (Vocal tract model)
- [[MFCCs]]
- [[Formants]]

---

*Chapter 8 · The Cepstrum and Homomorphic Speech Processing · Rabiner & Schafer · Tự học*
