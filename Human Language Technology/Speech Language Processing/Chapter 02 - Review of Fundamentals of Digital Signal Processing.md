---
tags:
  - speech-processing
  - DSP
  - chapter-2
aliases:
  - DSP Chapter 2
  - Digital Signal Processing Fundamentals
date: 2026-03-24
status: complete
---

# Chapter 2 — Review of Fundamentals of Digital Signal Processing

> [!abstract] Tóm tắt chương
> Chương này xây dựng nền tảng toán học và kỹ thuật cần thiết để xử lý tiếng nói: từ cách số hóa tín hiệu, phân tích miền tần số, đến thiết kế bộ lọc và hệ thống LTI.

---

## Bản đồ nội dung

```
DSP Fundamentals
├── 1. Tín hiệu số (Digital Signals)
├── 2. Số hóa: Sampling & Quantization
│   ├── Định lý Nyquist
│   └── Aliasing
├── 3. Phân tích miền tần số
│   ├── DTFT
│   ├── DFT / FFT
│   └── Z-Transform + ROC
├── 4. Hệ thống LTI
│   ├── Tính tuyến tính
│   └── Tính bất biến thời gian
└── 5. Bộ lọc số
    ├── FIR
    └── IIR
```

---

## 1. Bản Chất Tín Hiệu Số (Digital Signals)

Máy tính không hiểu sóng âm liên tục $x_a(t)$. Ta phải **lấy mẫu** (sampling) để có tín hiệu rời rạc:

$$x[n] = x_a(nT) \quad \text{với } T = \frac{1}{F_s}$$

- $x[n]$ chỉ tồn tại tại các giá trị thời gian **nguyên** $n = 0, 1, 2, \ldots$
- Dưới tầng sâu nhất, máy tính lưu các mẫu dưới dạng **chuỗi nhị phân** (binary sequence)

> [!warning] Hiểu lầm phổ biến
> Tín hiệu rời rạc **không có giá trị** ở giữa 2 mẫu. Máy tính hoàn toàn "mù" với những gì xảy ra giữa mốc $n$ và $n+1$.

---

## 2. Số Hóa Tín Hiệu (Sampling & Quantization)

### 2.1 Lấy Mẫu (Sampling) & Định Lý Nyquist

Tốc độ lấy mẫu $F_s$ phải thỏa mãn:

$$F_s \geq 2 \cdot F_{max}$$

| Tham số | Ý nghĩa |
|---------|---------|
| $F_s$ | Tần số lấy mẫu (sampling rate) |
| $F_{max}$ | Tần số cao nhất trong tín hiệu |
| $2 \cdot F_{max}$ | Tốc độ Nyquist — ngưỡng tối thiểu |

> [!example] Ứng dụng với tiếng nói
> Tiếng nói người có $F_{max} < 8\text{ kHz}$ → cần $F_s \geq 16\text{ kHz}$

### 2.2 Aliasing — Hiện Tượng Chồng Phổ

Nếu lấy mẫu **chậm hơn** tốc độ Nyquist (under-sampling), các tần số cao bị **"gập" ngược** xuống tần số thấp → âm thanh bị méo nặng.

> [!example] Ví dụ trực quan
> Xem phim thấy bánh xe ngựa **quay ngược** dù xe đang chạy tới — đó chính là Aliasing trong hình ảnh (camera chụp khung hình chậm hơn tốc độ quay bánh xe). Trong âm thanh, Aliasing tạo ra tiếng ồn chói tai.

### 2.3 Lượng Tử Hóa (Quantization)

Biến đổi biên độ tín hiệu thành giá trị số nguyên. **Bit depth** càng cao → độ chính xác càng tốt.

| Bit depth | Số mức lượng tử | Ứng dụng |
|-----------|----------------|----------|
| 8-bit | 256 | Điện thoại cũ |
| 16-bit | 65,536 | CD, âm thanh chuẩn |
| 24-bit | 16,777,216 | Studio, chuyên nghiệp |

---

## 3. Phân Tích Miền Tần Số

> **Vấn đề cốt lõi:** Trong ASR, máy tính "điếc" với sóng âm thời gian thực. Ta phải chuyển sang **miền tần số** để máy tính nhìn thấy "màu sắc" của âm thanh.

### 3.1 DTFT — Biến Đổi Fourier Rời Rạc Theo Thời Gian

**Mục đích:** Phân tích thành phần tần số (frequency content) của tín hiệu rời rạc — chuyển từ trục thời gian $n$ sang trục tần số liên tục $\omega$.

$$X(e^{j\omega}) = \sum_{n=-\infty}^{\infty} x[n] \cdot e^{-j\omega n}$$

- $x[n]$: mẫu tín hiệu thứ $n$
- $\omega$: tần số góc
- $e^{-j\omega n}$: hàm sin/cos cơ sở — dò xem tín hiệu có chứa tần số $\omega$ không

**Tính tuần hoàn với chu kỳ $2\pi$:**

$$e^{-j(\omega+2\pi)n} = e^{-j\omega n} \cdot \underbrace{e^{-j2\pi n}}_{=1 \text{ vì } n \in \mathbb{Z}} = e^{-j\omega n}$$

→ Phổ DTFT **lặp lại** sau mỗi khoảng $2\pi$.

> [!warning] DTFT vs DFT — Đừng nhầm!
> - **DTFT** → phổ **liên tục** → máy tính **không tính được trực tiếp**
> - **DFT** → lấy mẫu DTFT trên miền tần số → máy tính tính được
> - **FFT** → thuật toán tính **nhanh** DFT


DTFT cho ra phổ _liên tục_, máy tính không tính được. Trong thực tế, ta phải lấy mẫu trên miền tần số, đó chính là DFT (được tính nhanh bằng thuật toán FFT).
### 3.2 Z-Transform — "Vũ Khí Tối Thượng" Phân Tích Hệ Thống

**Mục đích:** Phân tích **toàn bộ hệ thống** — độ ổn định, thiết kế bộ lọc — trong miền tần số.

$$X(z) = \sum_{n=-\infty}^{\infty} x[n] \cdot z^{-n}$$

với $z = r \cdot e^{j\omega}$ là số phức trên mặt phẳng Z.

> [!tip] Mối quan hệ với DTFT
> DTFT chỉ là **trường hợp đặc biệt** của Z-Transform khi $r = 1$ (xét trên vòng tròn đơn vị).

**Ứng dụng thực tế:** Tìm **Poles** và **Zeros** của hệ thống LPC → biết hệ thống có bị mất ổn định (hú/rít loa) hay không.

### 3.3 ROC — Vùng Hội Tụ (Region of Convergence)

ROC là tập hợp các điểm trên mặt phẳng Z mà tại đó chuỗi tổng $X(z)$ **hội tụ** (không bị "nổ tung").

> [!example] Ví dụ trực quan
> Đưa micro lại gần loa và nghe tiếng **rít chói tai** — đó là khi hệ thống mất ổn định, các nghiệm của hệ thống **rơi ra khỏi vùng an toàn ROC**!

---

## 4. Hệ Thống LTI (Linear Time-Invariant)

> Mọi hệ thống xử lý tiếng nói đều được xây dựng trên nền tảng LTI.

Hệ thống LTI có hai đặc tính:

### 4.1 Tính Tuyến Tính (Linearity)

Tuân theo **nguyên lý xếp chồng** (Superposition):

$$\text{Đầu vào: } a \cdot x_1[n] + b \cdot x_2[n] \implies \text{Đầu ra: } a \cdot y_1[n] + b \cdot y_2[n]$$

### 4.2 Tính Bất Biến Theo Thời Gian (Time-Invariance)

Nếu đầu vào bị trễ $k$ mẫu → đầu ra cũng bị trễ đúng $k$ mẫu, **không thay đổi hình dáng**:

$$x[n-k] \implies y[n-k]$$

### 4.3 Tại Sao LTI Quan Trọng?

Nhờ LTI, ta có thể dùng **phép chập** (Convolution):

$$y[n] = \sum_{k=-\infty}^{\infty} x[k] \cdot h[n-k]$$

> [!info] Ứng dụng trong ASR
> Bộ máy phát âm của con người trong một khung **20ms** được coi là hệ thống LTI → cho phép lọc bỏ tạp âm và phân tích âm thanh dễ dàng.

---

## 5. Bộ Lọc Số (Digital Filters)

> **Nguyên tắc:** Đưa một xung lực (impulse) vào hệ thống → lấy đầu ra (impulse response $h[n]$) → áp dụng Fourier → vẽ ra chính xác tần số nào bị cắt/giữ lại.

### So Sánh FIR và IIR

| Tiêu chí | FIR | IIR |
|----------|-----|-----|
| **Tên đầy đủ** | Finite Impulse Response | Infinite Impulse Response |
| **Feedback** | ❌ Không có | ✅ Có vòng phản hồi |
| **Dữ liệu dùng** | Chỉ đầu vào quá khứ $x[n-k]$ | Đầu vào + đầu ra quá khứ $y[n-k]$ |
| **Độ ổn định** | Luôn ổn định | Có thể mất ổn định |
| **Tốc độ** | Chậm hơn | Nhanh hơn |
| **Độ phức tạp** | Cần nhiều tham số | Bộ lọc phức tạp với ít tham số |

### 5.1 FIR — Đáp Ứng Xung Hữu Hạn

- Đưa xung lực vào → đầu ra **dập tắt về 0** sau số mẫu hữu hạn
- Không bao giờ bị cộng hưởng vô tận
- **Luôn ổn định**

### 5.2 IIR — Đáp Ứng Xung Vô Hạn

Phương trình sai phân:

$$y[n] = \sum_{k=0}^{M} b_k x[n-k] - \sum_{k=1}^{N} a_k y[n-k]$$

- Phần $\sum b_k x[n-k]$: dùng **đầu vào** quá khứ
- Phần $\sum a_k y[n-k]$: dùng **đầu ra** quá khứ → đây là **vòng phản hồi**

> [!warning] Rủi ro của IIR
> IIR tính toán rất nhanh nhưng dễ **mất ổn định** — nguyên nhân gây tiếng rít loa khi micro đặt gần loa.

---

## Tóm Tắt

```
Analog Signal xa(t)
        │
        ▼ Sampling (Nyquist: Fs ≥ 2·Fmax)
Discrete Signal x[n]         ← Cẩn thận Aliasing!
        │
        ▼ Frequency Analysis
   DTFT / Z-Transform         ← Phân tích tần số & ổn định hệ thống
        │
        ▼ LTI System
   Convolution y[n] = x[n]*h[n]
        │
        ▼ Digital Filter
   FIR (ổn định) / IIR (nhanh, cần cẩn thận)
```

| Công cụ | Dùng để |
|---------|---------|
| **DTFT** | Phân tích phổ tần của tín hiệu rời rạc |
| **DFT/FFT** | Tính toán thực tế trên máy tính |
| **Z-Transform** | Phân tích toàn bộ hệ thống, tìm poles/zeros |
| **ROC** | Xác định vùng ổn định của hệ thống |
| **LTI** | Nền tảng lý thuyết cho mọi bộ lọc |
| **FIR/IIR** | Thiết kế bộ lọc thực tế |

---

## Liên Kết

- [[Chapter 1]] — Introduction to Digital Speech Processing
- [[Chapter 3]] — (tiếp theo)
- [[DTFT]]
- [[Z-Transform]]
- [[MFCCs]]
- [[ASR Pipeline]]

---

*Chapter 2 · Digital Signal Processing Fundamentals · Tự học*
