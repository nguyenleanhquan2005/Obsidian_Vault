---
tags:
  - speech-processing
  - audio-coding
  - MP3
  - subband
  - chapter-12
aliases:
  - Frequency-Domain Coding
  - MP3 Coding
  - Mã Hóa Miền Tần Số
date: 2026-03-24
status: complete
---

# Chapter 12 — Frequency-Domain Coding of Speech and Audio

> [!abstract] Tóm tắt chương
> Trong khi Ch11 dùng LPC (mô hình vocal tract) để nén tiếng nói, chương này dùng **miền tần số** để nén: Subband Coding, Adaptive Transform Coding, và đặc biệt là **MP3/MPEG Audio** — khai thác Auditory Masking để xóa những gì tai người không nghe thấy.

---

## Bản đồ nội dung

```
Frequency-Domain Coding of Speech and Audio
├── 1. Tại Sao Mã Hóa Miền Tần Số?
├── 2. Subband Coding (SBC)
│   ├── Filter bank phân tích
│   ├── Quantization từng subband
│   └── Liên hệ với Maximally Decimated FB
├── 3. Adaptive Transform Coding (ATC)
│   ├── DCT / KLT
│   └── Bit allocation động
├── 4. Perception Model — Auditory Masking ★
│   ├── Simultaneous masking
│   ├── Temporal masking
│   └── Critical bands
├── 5. MPEG-1 Audio Coding (MP3) ★
│   ├── Kiến trúc MP3
│   ├── Psychoacoustic model
│   └── Kết quả: 10x compression
└── 6. Other Standards: AAC, Opus
```

---

## 1. Tại Sao Mã Hóa Miền Tần Số?

### 1.1 Hạn Chế Của LPC Coding

LPC (Ch11) tuyệt vời cho **tiếng nói** nhưng không tốt cho **âm nhạc** vì:
- LPC giả định vocal tract model → chỉ đúng với giọng người
- Âm nhạc có cấu trúc phổ phức tạp hơn, không xấp xỉ được bằng all-pole

### 1.2 Ý Tưởng Tần Số

Thay vì mô hình hóa nguồn phát âm, **phân tích trực tiếp phổ tần số** và:
1. Loại bỏ các thành phần tần số ít quan trọng (perceptually)
2. Phân bổ bits nhiều hơn cho tần số quan trọng

---

## 2. Subband Coding (SBC)

### 2.1 Nguyên Lý

Chia tín hiệu thành $M$ dải tần (subbands) → quantize từng dải riêng với bitrate khác nhau:

```
Input x[n]
    │
    ├──→ [H₀: 0-1kHz]   → ↓M → Quantize (nhiều bits) → ↑M → [G₀] ──┐
    ├──→ [H₁: 1-2kHz]   → ↓M → Quantize (trung bình) → ↑M → [G₁] ──┤→ ŷ[n]
    ├──→ [H₂: 2-4kHz]   → ↓M → Quantize (ít bits)    → ↑M → [G₂] ──┤
    └──→ [H₃: 4-8kHz]   → ↓M → Quantize (rất ít bits)→ ↑M → [G₃] ──┘
```

### 2.2 Bit Allocation

**Nguyên tắc:** Cấp phát bits tỉ lệ với **variance** của từng subband:
- Dải tần thấp (giọng nói) → nhiều bits hơn
- Dải tần cao (ít năng lượng) → ít bits hơn

### 2.3 Liên Hệ Với Maximally Decimated Filter Bank (Ch7)

SBC chính là **ứng dụng trực tiếp** của Maximally Decimated Filter Bank:
- $M$ kênh lọc = $M$ subbands
- Hệ số giảm mẫu = $M$ (maximally decimated)

---

## 3. Adaptive Transform Coding (ATC)

### 3.1 Nguyên Lý

Thay vì filter banks, dùng **biến đổi tuyến tính** (DCT, KLT) để transform speech frame → tìm basis vectors tốt nhất:

$$\mathbf{y} = \mathbf{T} \cdot \mathbf{x}$$

Các hệ số $y_k$ sau transform có **phân bố không đều** → quantize hiệu quả hơn.

### 3.2 DCT — Discrete Cosine Transform

DCT gần tối ưu với speech và tính toán nhanh → được dùng trong MPEG Audio:

$$X[k] = \sum_{n=0}^{N-1} x[n] \cos\left(\frac{\pi k (2n+1)}{2N}\right)$$

### 3.3 Adaptive Bit Allocation

Phân bổ bits **động** theo năng lượng từng hệ số:
- Hệ số lớn → nhiều bits
- Hệ số nhỏ → ít bits (hoặc bỏ qua)

---

## 4. Perception Model — Auditory Masking ★

### 4.1 Auditory Masking Là Gì?

> Nếu một âm thanh **to** ở một tần số, nó sẽ "che khuất" (mask) các âm **nhỏ hơn** ở tần số lân cận → tai người **không nghe thấy** những âm bị che khuất.

### 4.2 Simultaneous Masking (Masking đồng thời)

```
Năng lượng
  ↑
  │      Masker (1000Hz, to)
  │           ███
  │          █████
  │         ███████  Masking threshold
  │  ......███████████........
  │                   Maskee
  │                   (1050Hz, nhỏ — không nghe thấy!)
  └─────────────────────────────→ Tần số
```

**Critical Bands** xác định phạm vi masking: âm trong cùng Critical Band dễ bị mask nhau nhất.

### 4.3 Temporal Masking

Masking cũng xảy ra **theo thời gian**:
- **Pre-masking:** ~5–20 ms TRƯỚC khi masker xuất hiện
- **Post-masking:** ~50–200 ms SAU khi masker kết thúc

### 4.4 Ứng Dụng Trong Audio Coding

> [!example] Tại sao MP3 nhỏ mà nghe vẫn tốt?
> MP3 tính **masking threshold** cho từng frame → bất kỳ thành phần tần số nào **dưới ngưỡng** này → **xóa hoàn toàn** (tai người không nghe thấy dù sao).
> Kết quả: loại bỏ 80-90% dữ liệu mà chất lượng cảm nhận gần như không đổi!

---

## 5. MPEG-1 Audio Coding — MP3 ★

### 5.1 Kiến Trúc MP3

```
PCM Audio (1411 kbps cho CD)
        │
        ▼
[Polyphase Filter Bank]
32 subbands, Maximally Decimated
        │
        ├──────────────────────────→ [Psychoacoustic Model]
        │   (song song)                      │
        │                           Tính masking threshold
        │                                    │
        ▼                                    ▼
[MDCT trong mỗi subband]            Masking thresholds
        │                                    │
        └──────────────┬─────────────────────┘
                       ▼
              [Adaptive Bit Allocation]
              Cấp bits dựa trên masking threshold
                       │
                       ▼
              [Quantization + Huffman Coding]
                       │
                       ▼
              MP3 Bitstream (128 kbps ≈ 10x compression)
```

### 5.2 Psychoacoustic Model

MP3 Layer III dùng **psychoacoustic model** tính toán:
1. **Spreading function** — masking lan sang tần số lân cận bao nhiêu
2. **Masking threshold** — ngưỡng tối thiểu tai người nghe thấy
3. **Signal-to-Mask Ratio (SMR)** — tỉ số tín hiệu / ngưỡng masking

### 5.3 Kết Quả

| | PCM | MP3 128kbps | MP3 320kbps |
|-|-----|-------------|-------------|
| **Bitrate** | 1411 kbps | 128 kbps | 320 kbps |
| **Compression** | 1x | **~11x** | ~4.5x |
| **Chất lượng** | Gốc | Rất tốt | Gần gốc |

> [!info] Maximally Decimated FB trong MP3
> MP3 dùng **32-channel Maximally Decimated Filter Bank** — kỹ thuật từ Ch7 — là xương sống của toàn bộ hệ thống. Sau đó MDCT cho độ phân giải tần số cao hơn trong từng subband.

---

## 6. Other Audio Coding Standards

### 6.1 AAC (Advanced Audio Coding)

- Chuẩn kế tiếp sau MP3 (MPEG-2/4 AAC)
- Cải thiện psychoacoustic model, dùng MDCT tốt hơn
- **Better quality ở cùng bitrate** so với MP3
- Dùng trong: iTunes, YouTube, iOS (AAC 256 kbps)

### 6.2 Opus

- Codec mã nguồn mở hiện đại nhất (2012)
- Kết hợp **SILK** (speech) + **CELT** (audio) → tốt cho cả tiếng nói và âm nhạc
- Dùng trong: WebRTC, Discord, Zoom, Spotify
- Bitrate: 6 kbps (voice) đến 510 kbps (music)

### 6.3 So Sánh Standards

| Codec | Năm | Bitrate | Tốt cho |
|-------|-----|---------|---------|
| **MP3** | 1993 | 32–320 kbps | Music |
| **AAC** | 1997 | 16–320 kbps | Music + Multimedia |
| **G.729** | 1996 | 8 kbps | Speech only |
| **Opus** | 2012 | 6–510 kbps | **Universal** |

---

## Tóm Tắt

```
Audio Signal
        │
        ▼ Frequency analysis
Subband / Transform coefficients
        │
        ▼ Psychoacoustic model
Masking thresholds per frequency band
        │
        ▼ Adaptive bit allocation
Bits → Important components (nhiều bits)
Bits → Masked components (0 bits — xóa đi)
        │
        ▼ Quantize + Entropy code
Compressed bitstream
        │
        ▼ 10x smaller, same perceptual quality
```

| Kỹ thuật | Ứng dụng |
|---------|---------|
| **Subband Coding** | Nền tảng MP3, phân tích dải tần |
| **Adaptive Transform (DCT/MDCT)** | MP3, AAC — tần số resolution cao |
| **Auditory Masking** | Xóa thành phần không nghe thấy |
| **Psychoacoustic model** | Tính masking threshold chính xác |

---

## Liên Kết

- [[Chapter 7]] — Frequency-Domain Representations (Filter Banks, STFT)
- [[Chapter 11]] — Digital Coding of Speech (LPC, CELP)
- [[Chapter 4]] — Hearing & Auditory Models (Critical Bands, Masking)
- [[Chapter 5]] — Sound Propagation

---

*Chapter 12 · Frequency-Domain Coding of Speech and Audio · Rabiner & Schafer · Tự học*
