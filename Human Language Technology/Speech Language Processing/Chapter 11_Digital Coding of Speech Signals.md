---
tags:
  - speech-processing
  - speech-coding
  - LPC
  - compression
  - chapter-11
aliases:
  - Digital Coding of Speech
  - Speech Compression
  - Mã Hóa Tiếng Nói Số
date: 2026-03-24
status: complete
---

# Chapter 11 — Digital Coding of Speech Signals

> [!abstract] Tóm tắt chương
> Chương này trình bày các phương pháp mã hóa và nén tiếng nói số: từ quantization cơ bản, LPC-based coding (cốt lõi của điện thoại GSM, Zalo), ADPCM, đến các hệ thống Analysis-by-Synthesis như CELP — chuẩn nén hiện đại nhất. Mục tiêu: truyền tiếng nói chất lượng cao với băng thông tối thiểu.

---

## Bản đồ nội dung

```
Digital Coding of Speech Signals
├── 1. Tại Sao Cần Mã Hóa Tiếng Nói?
│   └── Bitrate vs Quality trade-off
├── 2. Statistical Model for Speech
│   ├── PDF của tiếng nói
│   └── Non-uniform distribution
├── 3. Quantization (Lượng Tử Hóa)
│   ├── Uniform quantization
│   ├── Non-uniform (μ-law, A-law)
│   └── Adaptive quantization
├── 4. LPC-Based Speech Coding ★
│   ├── Tại sao LPC nén được?
│   ├── Công thức synthesis
│   └── Ứng dụng: GSM, Zalo
├── 5. ADPCM — Differential Coding
│   ├── DPCM nguyên lý
│   └── Adaptive DPCM
├── 6. Analysis-by-Synthesis: CELP ★
│   ├── Code-Excited Linear Prediction
│   └── Ứng dụng: điện thoại di động
└── 7. Open-Loop Speech Coders
    └── Autocorrelation vs AMDF
```

---

## 1. Tại Sao Cần Mã Hóa Tiếng Nói?

### 1.1 Vấn Đề Bitrate

Raw PCM audio:
- $F_s = 8$ kHz, 16-bit → **128 kbps**
- $F_s = 16$ kHz, 16-bit → **256 kbps**

Đây là quá nhiều cho điện thoại di động hay VoIP! Mục tiêu:

| Codec | Bitrate | Ứng dụng |
|-------|---------|---------|
| **PCM (G.711)** | 64 kbps | Điện thoại cố định |
| **ADPCM (G.726)** | 32 kbps | ISDN |
| **GSM (LPC-based)** | 13 kbps | Điện thoại di động |
| **CELP (G.729)** | 8 kbps | VoIP (Zalo, Skype) |
| **LPC-10** | 2.4 kbps | Military, satellite |

### 1.2 Tại Sao Không Lấy Mẫu Với Tần Số Cao?

> [!warning] Cao sample rate = tốn tài nguyên vô ích
> Tần số lấy mẫu cao (như 192 kHz) tạo ra **gánh nặng tính toán cực lớn (increased computational load)** mà không mang thêm giá trị ngôn ngữ — vì giọng người chủ yếý nằm dưới 8 kHz.

---

## 2. Statistical Model for Speech

### 2.1 Phân Phối Xác Suất Của Tiếng Nói

Tiếng nói **không phân phối đều (non-uniform)** — hầu hết thời gian biên độ nhỏ (silence, quiet segments), thỉnh thoảng mới có biên độ lớn (stressed vowels):

```
PDF p(x)
  ↑
  │  ████
  │  ████
  │  ██████
  │  ████████
  │  ██████████████
  └──────────────────→ Amplitude x
      Tập trung ở giá trị nhỏ
```

→ **Non-uniform quantization** hiệu quả hơn uniform.

---

## 3. Quantization (Lượng Tử Hóa)

### 3.1 Uniform Quantization (Lượng Tử Đều)

Chia toàn bộ range thành $2^B$ bước đều nhau (B = bit depth).

**Nhược điểm:** Lãng phí bits cho biên độ lớn ít gặp.

### 3.2 Non-Uniform Quantization: μ-law và A-law

Nén biên độ lớn, mở rộng biên độ nhỏ → cùng số bits nhưng SNR tốt hơn:

| Chuẩn | Vùng | Ứng dụng |
|-------|------|---------|
| **μ-law** (mu-law) | Bắc Mỹ, Nhật | G.711 North America |
| **A-law** | Châu Âu | G.711 Europe/ITU |

### 3.3 Adaptive Quantization

**Step size thay đổi** theo từng frame dựa trên năng lượng tín hiệu → tốt hơn fixed quantization.

---

## 4. LPC-Based Speech Coding ★

### 4.1 Tại Sao LPC Nén Được?

> Thay vì truyền 8000 mẫu biên độ/giây (128 kbps), LPC chỉ truyền:
> - Bộ hệ số $\alpha_k$ (~10–16 số)
> - Pitch period $T_0$
> - Gain $G$
> - Voiced/Unvoiced flag
>
> **Tổng cộng: 2400–9600 bps** — nhưng vẫn tái tạo được giọng nói!

### 4.2 Công Thức LPC Synthesis

$$s[n] = \sum_{k=1}^{p} \alpha_k s[n-k] + G \cdot u[n]$$

**Decoder phía nhận:**
1. Nhận $\{\alpha_k, G, T_0, V/U\}$
2. Tạo $u[n]$: nếu Voiced → chuỗi xung với period $T_0$; nếu Unvoiced → white noise
3. Lọc qua $H(z) = G/A(z)$ → phục hồi tiếng nói

### 4.3 Tính Gain $G$ — Dùng Autocorrelation

$$G^2 = R[0] - \sum_{k=1}^{p} \alpha_k R[k]$$

> **Tham số Gain $G$ được tính dựa trên hàm autocorrelation của tiếng nói** — đây là điểm mấu chốt để biết hệ số khuếch đại phù hợp.


**2. Phương pháp Bình phương Tối thiểu (Least Squares Method - Câu 41)**

- Làm sao để tìm ra bộ hệ số $\alpha_k$ tối ưu nhất? Các kỹ sư sử dụng **Phương pháp Bình phương Tối thiểu**.
- **Bản chất Toán học:** Ta muốn tổng bình phương tín hiệu lỗi (Mean-Squared Error) trong một khung $E_{\hat{n}}$ là nhỏ nhất: $$E_{\hat{n}} = \sum_{m} e^2[m] = \sum_{m} \left( s[m] - \sum_{k=1}^{p} \alpha_k s[m-k] \right)^2$$ Để $E_{\hat{n}}$ đạt cực tiểu, ta lấy đạo hàm theo từng hệ số $\alpha_k$ và cho bằng 0 ($\partial E_{\hat{n}}/\partial \alpha_k = 0$). Giải hệ phương trình tuyến tính này, ta sẽ được bộ hệ số $\alpha_k$ phản ánh chính xác cấu trúc ống phát âm của người nói.
### 4.4 Ứng Dụng Thực Tế

| Codec | Kỹ thuật | Bitrate | Dùng trong |
|-------|---------|---------|-----------|
| **LPC-10** | Pure LPC | 2.4 kbps | Military |
| **GSM FR** | RPE-LTP | 13 kbps | 2G phones |
| **AMR** | Multi-rate LPC | 4.75–12.2 kbps | 3G/4G |
| **iLBC** | LPC variant | 15.2 kbps | WebRTC |

> [!example] Zalo/Messenger gọi điện ~8–10 kbps
> Gọi điện qua Zalo tốn rất ít dung lượng mà vẫn nghe rõ — đó là nhờ LPC không truyền file WAV mà truyền **bộ tham số mô phỏng cổ họng** người nói!

---

## 5. ADPCM — Differential Coding

### 5.1 DPCM Nguyên Lý

**Differential PCM** chỉ truyền **sự khác biệt** giữa mẫu hiện tại và mẫu dự đoán:

$$d[n] = s[n] - \hat{s}[n]$$

$d[n]$ có phương sai nhỏ hơn $s[n]$ nhiều → cần ít bits hơn!

### 5.2 ADPCM (Adaptive DPCM)

**Step size thay đổi theo thời gian** — thích nghi với tiếng nói:

- **G.726 ADPCM:** 32 kbps (giảm từ 64 kbps PCM) — dùng trong ISDN, VoIP cũ
- Tiêu chuẩn ITU-T được dùng rộng rãi nhất trong lịch sử

### 5.3 General Theory of Differential Quantization

Tối ưu hóa bộ dự đoán $\hat{s}[n] = \sum_k \alpha_k s[n-k]$ dùng **Least Squares Method**:

$$E = \sum_n \left(s[n] - \sum_{k=1}^p \alpha_k s[n-k]\right)^2 \rightarrow \text{minimize}$$

---

## 6. Analysis-by-Synthesis: CELP ★

### 6.1 Vấn Đề Của LPC Đơn Giản

LPC truyền thống giả định excitation là xung hoặc noise → nghe không tự nhiên lắm.

**CELP** cải thiện bằng cách **tìm kiếm codebook** để tìm excitation tốt nhất.

### 6.2 CELP — Code Excited Linear Prediction

```
Encoder:
  Speech s[n]
      │
      ▼
  LPC Analysis → {αₖ, G}
      │
      ▼
  Codebook Search: tìm vector u* trong codebook
  sao cho s[n] ≈ H(z) * G * u*[n]
      │
      ▼
  Truyền đi: {αₖ, G, codebook index}

Decoder:
  {αₖ, G, index}
      │
      ▼
  Lookup codebook → u[n]
      │
      ▼
  s[n] = H(z) * G * u[n]
```

### 6.3 Analysis-by-Synthesis Principle

Thay vì chỉ phân tích một lần → CELP **tổng hợp lại và so sánh** với tiếng gốc, chọn codebook entry nào cho sai số nhỏ nhất (perceptually weighted error).

| Codec | Kỹ thuật | Bitrate |
|-------|---------|---------|
| **G.729** | CS-ACELP | 8 kbps |
| **G.723.1** | MP-MLQ / ACELP | 5.3/6.3 kbps |
| **AMR-NB** | ACELP | 4.75–12.2 kbps |
| **AMR-WB (G.722.2)** | ACELP wideband | 6.6–23.85 kbps |

---

## 7. Autocorrelation vs AMDF Trong Pitch Estimation

*(Áp dụng trong các open-loop speech coders)*

| | **Autocorrelation** | **AMDF** |
|-|--------------------|----|
| **Công thức** | $R[k] = \sum x[m]x[m+k]$ | $\gamma[k] = \sum \|x[m]-x[m-k]\|$ |
| **Phép tính** | Nhân | Trừ + trị tuyệt đối |
| **Tốc độ** | Chậm hơn | **Nhanh hơn** trên chip |
| **Nhận dạng pitch** | Đỉnh (peak) | Thung lũng (valley) |

> Kỹ sư embedded thường chọn AMDF vì **phép trừ và abs** nhanh hơn **phép nhân** nhiều trên DSP/IoT chip.

---

## Tóm Tắt

```
Speech Signal (128 kbps raw)
        │
        ▼ LPC Analysis
{αₖ (vocal tract) + G (gain) + T₀ (pitch) + V/U}
        │
        ├──→ Simple LPC-10        → 2.4 kbps
        ├──→ GSM RPE-LTP          → 13 kbps
        ├──→ ADPCM G.726          → 32 kbps
        └──→ CELP G.729           → 8 kbps  ← VoIP chuẩn
```

| Phương pháp | Bitrate | Chất lượng | Độ phức tạp |
|------------|---------|-----------|------------|
| **PCM G.711** | 64 kbps | Tốt nhất | Thấp |
| **ADPCM G.726** | 32 kbps | Tốt | Thấp |
| **LPC-10** | 2.4 kbps | Chấp nhận | Trung bình |
| **CELP G.729** | 8 kbps | Tốt | **Cao** |

---

## Liên Kết

- [[Chapter 9]] — Linear Predictive Analysis (LPC, Poles, Prediction Error)
- [[Chapter 10]] — Algorithms for Estimating Speech Parameters (Pitch, AMDF)
- [[Chapter 12]] — Frequency-Domain Coding (MP3, Subband)
- [[Chapter 5]] — Sound Propagation (Vocal tract, Tube model)
- [[LPC]]
- [[CELP]]

---

*Chapter 11 · Digital Coding of Speech Signals · Rabiner & Schafer · Tự học*

**3. Ứng dụng nén tiếng nói (Speech Compression - Câu 42)**

- **Hiểu lầm phổ biến:** Sinh viên thường nghĩ "nén âm thanh" giống như nén file .ZIP. Không phải!
- **Sự thật (Câu 42 đúng):** LPC được dùng để nén vì thay vì phải truyền đi 8000 mẫu biên độ âm thanh mỗi giây, thuật toán chỉ truyền đi bộ hệ số $\alpha_k$, tần số Pitch và mức năng lượng $G$. Tổng cộng chỉ tốn khoảng 2400 - 9600 bps mà vẫn tái tạo (synthesize) lại được giọng nói.