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


### 1.1 Mục Đích Trong Speech Processing

**Mục đích chính của bộ lọc số:** Loại bỏ nhiễu và cải thiện độ rõ nét của tiếng nói (remove noise and improve speech clarity).

**Các ứng dụng điển hình:**

| Loại bộ lọc | Mục đích | Ví dụ |
|------------|---------|-------|
| **Low-pass** | Cắt bỏ tần số cao không cần thiết | Anti-aliasing trước A/D |
| **High-pass** | Loại bỏ tiếng ồn tần số thấp (rung nền) | Lọc tiếng ồn micro |
| **Band-pass** | Giữ lại dải tần tiếng nói (300–3400 Hz) | Điện thoại thoại |
| **Notch** | Loại bỏ một tần số cụ thể | Khử tiếng hum 50/60 Hz |

### 1.2 Anti-Aliasing Filter

> [!important] Quy tắc bắt buộc
> Bộ lọc **Low-pass (Anti-aliasing)** luôn phải được đặt **TRƯỚC bộ A/D converter** để cắt bỏ mọi thành phần tần số vượt quá $F_{max}$ — ngăn chặn Aliasing trước khi lấy mẫu.

```
Tín hiệu analog
        │
        ▼
[Anti-aliasing LPF]  ← Cắt tần số > Fmax
        │
        ▼
[A/D Converter]       ← Lấy mẫu an toàn
        │
        ▼
Tín hiệu số x[n]
---
```


## 2. Số Hóa Tín Hiệu (Sampling & Quantization)

### 2.1 Lấy Mẫu (Sampling) & Định Lý Nyquist

Tốc độ lấy mẫu $F_s$ phải thỏa mãn:

$$F_s \geq 2 \cdot F_{max}$$

| Tham số           | Ý nghĩa                           |
| ----------------- | --------------------------------- |
| $F_s$             | Tần số lấy mẫu (sampling rate)    |
| $F_{max}$         | Tần số cao nhất trong tín hiệu    |
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

**3. Tại sao không lấy mẫu với tần số cực cao? (Câu 60)**

- _Câu 60 chỉ ra nhược điểm chính:_ Tần số lấy mẫu cao (như 192kHz) đồng nghĩa với số lượng dữ liệu khổng lồ. Điều này tạo ra **gánh nặng tính toán cực lớn (increased computational load)** cho CPU/DSP chip mà lại không mang thêm giá trị thông tin ngôn ngữ (bởi giọng người chủ yếu nằm dưới 8kHz).

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
**🇬🇧 1. The Nature of Digital Signals (Q64, Q74)**

- **Concept:** A microphone captures sound as a continuous analog wave $x_a(t)$. To process it in a computer, we must sample it. A discrete-time signal $x[n]$ is defined **only at integer values of time** ($n = 0, 1, 2...$) based on the sampling period $T$. Ultimately, computers store these discrete values as a **binary sequence** (0s and 1s).
- **Math:** $x[n] = x_a(nT)$ where $T = 1/F_s$.
- **Common Mistake:** Students think discrete signals exist "between" samples. They don't. The machine is completely blind to what happens between $n$ and $n+1$.

**🇻🇳 1. Bản chất tín hiệu số (Câu 64, 74)**

- **Giải thích:** Máy tính không hiểu sóng âm liên tục $x_a(t)$. Ta phải lấy mẫu (sampling). Tín hiệu rời rạc $x[n]$ **chỉ được định nghĩa tại các giá trị thời gian nguyên (integer values of time)** $n$. Dưới tầng vật lý sâu nhất của máy tính, tất cả các mẫu này được biểu diễn thành **chuỗi nhị phân (binary sequence)**.
- **Hiểu lầm phổ biến:** Nhiều sinh viên nghĩ tín hiệu rời rạc vẫn có giá trị ở giữa 2 mẫu. Sai! Máy tính hoàn toàn "mù" với những gì xảy ra giữa mốc $n$ và $n+1$.

**🇬🇧 2. FIR vs. IIR Filters (Q78)**

- **Concept:** Filters manipulate frequencies. The core difference is the **feedback loop**.
    - **FIR (Finite Impulse Response):** Only uses _past inputs_ ($x[n-k]$). No feedback. Always stable.
    - **IIR (Infinite Impulse Response):** Uses both _past inputs_ AND _past outputs_ ($y[n-k]$). **It has feedback (có vòng phản hồi)**.
- **Math (IIR):** $y[n] = \sum_{k=0}^{M} b_k x[n-k] - \sum_{k=1}^{N} a_k y[n-k]$ (The $a_k y[n-k]$ part is the feedback!).

**🇻🇳 2. Bộ lọc FIR và IIR (Câu 78)**

- **Giải thích:** Sự khác biệt cốt lõi nằm ở **vòng phản hồi (Feedback)**. FIR chỉ dùng dữ liệu đầu vào trong quá khứ nên không có phản hồi. IIR dùng cả kết quả đầu ra trong quá khứ ($y[n-k]$) để tính tiếp, do đó **IIR có vòng phản hồi (have feedback)**. Bộ lọc IIR tính toán rất nhanh nhưng dễ bị mất ổn định (rít loa).

Mọi hệ thống xử lý tiếng nói (từ bộ lọc nhiễu cho đến mô hình mô phỏng tuyến âm) đều được xây dựng dựa trên nền tảng của Hệ thống Tuyến tính Bất biến (LTI) và Biến đổi Z.

**1. Hệ thống LTI và Tính Bất biến theo thời gian (Câu 106)**

- **Bản chất:** LTI (Linear Time-Invariant) là hệ thống sở hữu hai đặc tính: Tuyến tính (Linear) và Bất biến theo thời gian (Time-shifting invariance).
    - _Tính tuyến tính:_ Tuân theo nguyên lý xếp chồng (Superposition). Nếu đầu vào là $a \cdot x_1[n] + b \cdot x_2[n]$, đầu ra sẽ là $a \cdot y_1[n] + b \cdot y_2[n]$.
    - _Tính bất biến theo thời gian (Đáp án C):_ Nếu tín hiệu đầu vào bị trễ đi $k$ mẫu ($x[n-k]$), thì tín hiệu đầu ra cũng bị trễ đi đúng $k$ mẫu ($y[n-k]$), mà không làm thay đổi hình dáng tín hiệu.
- **Liên hệ thực tiễn:** Tại sao LTI quan trọng? Vì nhờ nó, ta mới có thể dùng phép chập (Convolution): $y[n] = \sum_{k=-\infty}^{\infty} x[k]h[n-k]$. Trong ASR, ta coi bộ máy phát âm của con người trong một khung ngắn 20ms là một hệ thống LTI, cho phép ta lọc bỏ các tạp âm dễ dàng.

**2. Biến đổi Z (Z-Transform) - "Chiếc kính lúp" miền tần số (Câu 110)**

- **Công thức Bắt buộc:** $$X(z) = \sum_{n=-\infty}^{\infty} x[n] z^{-n}$$ _(Trong đó: $x[n]$ là chuỗi tín hiệu thời gian rời rạc, $z$ là một số phức $z = r \cdot e^{j\omega}$ đại diện cho mặt phẳng phức)._
- **Ý nghĩa cốt lõi (Đáp án B):** Mục đích chính yếu nhất của Biến đổi Z là **Phân tích miền tần số (Frequency-domain analysis)** của các tín hiệu và hệ thống rời rạc. Khi ta thay $z = e^{j\omega}$ (tức là xét trên vòng tròn đơn vị $r=1$), Biến đổi Z sẽ trở thành DTFT.
- **Lỗi sai phổ biến:** Sinh viên thường nghĩ Z-transform chỉ là một công cụ giải toán. Thực tế, các kỹ sư dùng nó để tìm các **Điểm cực (Poles)** và **Điểm không (Zeros)** của hệ thống LPC, từ đó biết hệ thống có bị "hú/rít" (mất ổn định) hay không dựa vào Vùng hội tụ (ROC).


### BÀI GIẢNG 1: NỀN TẢNG XỬ LÝ TÍN HIỆU SỐ (DSP) & MIỀN TẦN SỐ

_(Bao trùm các câu: 16, 18, 19, 20)_

Trong ASR, máy tính bị "điếc" với sóng âm thời gian thực. Chúng ta phải chuyển sóng âm đó sang miền tần số để máy tính nhìn thấy "màu sắc" của âm thanh.

**1. Biến đổi Fourier rời rạc theo thời gian (DTFT - Câu 16)**

- **Bản chất:** DTFT dùng để phân tích thành phần tần số (frequency content) của một tín hiệu rời rạc. Nó chuyển tín hiệu từ trục thời gian $n$ sang trục tần số liên tục $\omega$.
- **Công thức Bắt buộc:** $$X(e^{j\omega}) = \sum_{n=-\infty}^{\infty} x[n] e^{-j\omega n}$$ _(Trong đó: $x[n]$ là mẫu tín hiệu thứ $n$, $\omega$ là tần số góc. $e^{-j\omega n}$ là các hàm sin/cos cơ sở để dò xem tín hiệu có chứa tần số $\omega$ đó không)._


**2. Biến đổi Z (Z-Transform) và Miền Hội Tụ (ROC - Câu 18, 20)**

- **Bản chất:** Nếu DTFT chỉ phân tích phổ, thì Z-transform là "vũ khí tối thượng" để phân tích **toàn bộ hệ thống** (độ ổn định, bộ lọc) trong miền tần số (Frequency-domain analysis).
- **Công thức Bắt buộc:** $$X(z) = \sum_{n=-\infty}^{\infty} x[n] z^{-n}$$ _(Với $z$ là một số phức $z = r \cdot e^{j\omega}$. Thực chất DTFT chỉ là trường hợp đặc biệt của Z-transform khi vòng tròn có bán kính $r=1$)._
- **Hiểu trực quan về ROC (Region of Convergence):** ROC là tập hợp các điểm trên mặt phẳng Z mà tại đó chuỗi tổng $X(z)$ không bị nổ tung (converges - hội tụ). **Liên hệ thực tế:** Bạn đã bao giờ đưa micro lại gần loa và nghe tiếng rít chói tai chưa? Đó là khi hệ thống âm thanh mất ổn định, các nghiệm của hệ thống đã rơi ra khỏi "vùng an toàn" ROC!

**3. Đáp ứng tần số của hệ thống (Câu 19)**

- Làm sao để biết một bộ lọc kỹ thuật số (ví dụ: bộ cắt âm trầm) hoạt động thế nào? Ta chỉ cần đưa một xung lực (impulse) vào hệ thống, lấy kết quả đầu ra (impulse response $h[n]$), và **áp dụng biến đổi Fourier lên $h[n]$** này. Máy tính sẽ vẽ ra chính xác biểu đồ tần số bị cắt hay được giữ lại.


**1. Bộ lọc kỹ thuật số (Digital Filters - Câu 4, 14)**

- Có hai loại bộ lọc số chính: FIR (hữu hạn) và IIR (vô hạn). Đặc trưng cốt lõi của **IIR là nó có vòng phản hồi (feedback loop)**, giúp nó tạo ra các bộ lọc phức tạp chỉ với rất ít tham số tính toán.


_(Bao trùm các câu: 30, 32, 34, 36)_

Để xử lý tiếng nói, việc đầu tiên là phải đưa sóng âm vật lý (analog) vào thế giới số (digital).

**1. Lấy mẫu và Định lý Nyquist (Câu 30, 34)**

- **Bản chất (Câu 34):** Quá trình chuyển đổi tín hiệu từ dạng liên tục (Analog) sang dạng số (Digital) gọi là **Sampling (Lấy mẫu)**. Về mặt toán học, ta lấy tín hiệu liên tục $x_a(t)$ và cắt nó tại các chu kỳ $T$ đều đặn: $$x[n] = x_a(nT)$$
- **Tốc độ Nyquist (Câu 30):** Máy tính không thể lấy mẫu bừa bãi. Theo định lý Nyquist-Shannon, tốc độ lấy mẫu tối thiểu ($F_s$) phải thỏa mãn: $$F_s \geq 2 \cdot F_{max}$$ Trong đó $F_{max}$ là tần số cao nhất có trong tín hiệu.
- **Giải thích trực quan & Lỗi sai:** Nếu bạn lấy mẫu chậm hơn tốc độ Nyquist, hiện tượng **Aliasing (Chồng phổ)** sẽ xảy ra. Bạn đã bao giờ xem phim thấy bánh xe ngựa quay ngược dù xe đang chạy tới chưa? Đó chính là Aliasing trong hình ảnh (do camera chụp khung hình chậm hơn tốc độ quay của bánh xe). Trong âm thanh, Aliasing làm các tần số cao bị "gập" ngược lại thành tần số thấp, tạo ra tiếng ồn cực kỳ chói tai. Do đó, đáp án đúng của câu 30 là _Tốc độ tối thiểu để tránh Aliasing_.

**1. Tính tuần hoàn của DTFT (Câu 56)**

- **Công thức DTFT:** $$X(e^{j\omega}) = \sum_{n=-\infty}^{\infty} x[n] e^{-j\omega n}$$
- _Tại sao nó tuần hoàn với chu kỳ $2\pi$?_ Rất dễ chứng minh. Nếu bạn cộng thêm $2\pi$ vào tần số $\omega$, ta có $e^{-j(\omega + 2\pi)n} = e^{-j\omega n} \cdot e^{-j2\pi n}$. Vì $n$ là số nguyên, $e^{-j2\pi n}$ luôn bằng $1$. Do đó phổ bị lặp lại sau mỗi khoảng $2\pi$.

**2. Aliasing - Hiện tượng chồng phổ (Câu 57)**

- Theo định lý Nyquist, bạn phải lấy mẫu (sampling) với tần số $F_s \ge 2F_{max}$. Nếu lấy mẫu quá chậm (under-sampling), các thành phần tần số cao sẽ "gập" (overlap/fold) ngược trở lại và đè lên các tần số thấp, làm hỏng hoàn toàn âm thanh. Giống như khi bạn quay video một chiếc xe chạy quá nhanh, bánh xe trông như đang quay ngược lại vậy!

**4. Bộ lọc FIR (Câu 55)**

- Trong bộ lọc số, **FIR** viết tắt của **Finite Impulse Response (Đáp ứng xung hữu hạn)**. Nghĩa là nếu bạn đưa một xung lực vào, tín hiệu đầu ra của nó sẽ dập tắt về 0 sau một số lượng mẫu hữu hạn. Cực kỳ ổn định và không bao giờ bị cộng hưởng lặp vô tận (khác với IIR).


