---
tags:
  - speech-processing
  - DSP
  - frequency-domain
  - chapter-7
aliases:
  - Frequency Domain Representations
  - Biểu Diễn Miền Tần Số
date: 2026-03-24
status: complete
---

# Chapter 7 — Frequency-Domain Representations

> [!abstract] Tóm tắt chương
> Chương này đi sâu vào các công cụ phân tích miền tần số: từ DFT/FFT, STFT, phương pháp tổng hợp Overlap-Add, đến các cấu trúc filter bank phức tạp hơn — tất cả đều là nền tảng để xử lý tiếng nói thực tế.

---

## Bản đồ nội dung

```
Frequency-Domain Representations
├── 1. Discrete-Time Fourier Analysis (Phân tích Fourier rời rạc) [1]
│   ├── DTFT và DFT: Toán học chuyển đổi không gian [3, 4]
│   ├── Thuật toán tính nhanh (FFT - Fast Fourier Transform) [5]
│   └── Vai trò của Windowing (Cửa sổ) trong phân tích phổ [6]
│
├── 2. Short-Time Fourier Analysis (Phân tích STFT) [1]
│   ├── Công thức STFT Bắt buộc & Biến số thời gian - tần số [7]
│   ├── Heisenberg Trade-off (Sự đánh đổi Độ phân giải Thời gian - Tần số) 
│   ├── Spectrographic Displays (Biểu diễn Ảnh phổ): Wideband vs Narrowband [1, 8]
│   └── Hai góc nhìn: Lọc tuyến tính (Linear Filtering) vs Biến đổi Fourier [9, 10]
│
├── 3. Overlap Addition Method - OLA (Phương pháp Cộng chồng lấp) [1]
│   ├── Định nghĩa & Perfect Reconstruction (Điều kiện phục hồi hoàn hảo) [11, 12]
│   ├── Sự cần thiết của Cửa sổ Tổng hợp (Synthesis Window) [13, 14]
│   └── Kiến trúc OLA khi có chỉnh sửa trên STFT [13, 15]
│
├── 4. Time-Decimated Filter Banks (Băng lọc giảm mẫu theo thời gian) [1]
│   ├── Filter Bank Summation (FBS) (Phương pháp tổng hợp băng lọc) [16, 17]
│   ├── Kỹ thuật Downsampling (Giảm mẫu) & Interpolation (Nội suy) [18, 19]
│   └── Maximally Decimated Filter Bank (Băng lọc giảm mẫu tối đa) ★ [20]
│
├── 5. Two-Channel Filter Banks (Băng lọc hai kênh) [1]
│   ├── Quadrature Mirror Filter Banks (QMF) [21]
│   ├── Conjugate Quadrature Filters (CQF) [22]
│   └── Polyphase Structure (Cấu trúc đa pha) & Tree-structured (Cấu trúc cây) [23, 24]
│
└── 6. Modifications of the STFT (Các phép chỉnh sửa trên STFT) [1]
    ├── Chỉnh sửa biên độ và pha (Magnitude and Phase modifications) [25]
    └── Ứng dụng Phase Vocoder (Ví dụ: Time Expansion/Compression - Đổi tốc độ/cao độ) [26, 27]
```




---

## 1. Discrete-Time Fourier Analysis

### 1.1 Fourier Transform Cơ Bản

**Fourier Transform** chuyển đổi tín hiệu từ **time domain → frequency domain**, tiết lộ tần số nào có trong tín hiệu và với cường độ bao nhiêu.

> [!info] Tại sao cần phân tích tần số?
> Tiếng nói trong miền thời gian chỉ là sóng — khó phân tích. Trong miền tần số, ta thấy rõ **"màu sắc"** âm thanh: formants, harmonics, noise...

### 1.2 Discrete Fourier Transform (DFT)

DFT lấy mẫu DTFT trên miền tần số → có thể tính toán trên máy tính.

$$X[k] = \sum_{n=0}^{N-1} x[n] \cdot e^{-j2\pi kn/N}, \quad k = 0, 1, \ldots, N-1$$

**Các tính chất quan trọng của DFT:**

| Tính chất | Ý nghĩa |
|-----------|---------|
| **Linearity** | DFT của tổng = tổng DFT |
| **Periodicity** | DFT có chu kỳ $N$ |
| **Symmetry** | Với tín hiệu thực: $X[N-k] = X^*[k]$ |
| **Time shift** | Dịch chuyển thời gian → xoay pha trong miền tần số |
| **Convolution** | Tích chập thời gian ↔ nhân trong miền tần số |

### 1.3 Fast Fourier Transform (FFT)

**FFT** là thuật toán tính DFT **hiệu quả hơn rất nhiều**:

| | DFT | FFT |
|-|-----|-----|
| Độ phức tạp | $O(N^2)$ | $O(N \log N)$ |
| N=1024 | ~1M phép tính | ~10K phép tính |

> FFT = DFT, chỉ khác về **cách tính** — kết quả giống hệt nhau.

### 1.4 Windowing & Spectral Leakage

**Vấn đề:** Khi cắt một đoạn tín hiệu hữu hạn, cạnh sắc ở hai đầu gây ra **spectral leakage** — năng lượng "rò rỉ" sang các tần số lân cận.

**Giải pháp:** Áp dụng **window function** để làm mềm cạnh tín hiệu:

| Window | Spectral Leakage | Đặc điểm |
|--------|-----------------|----------|
| **Rectangular** | Cao — cạnh sắc | Đơn giản nhất |
| **Hamming** | Thấp hơn — cạnh mượt | Phổ biến nhất |
| **Hanning** | Tương tự Hamming | Tapering khác |
| **Blackman** | Thấp nhất | Tapering nhiều hơn |

**Quy trình phân tích thực tế:**
```
Load tín hiệu → Apply window → Compute FFT → Visualize spectrum
```

> [!tip] Thực hành Python
> ```python
> import numpy as np
> from scipy import signal
> import matplotlib.pyplot as plt
>
> # Apply Hamming window
> window = np.hamming(len(x))
> x_windowed = x * window
>
> # Compute FFT
> X = np.fft.fft(x_windowed)
> magnitude = np.abs(X)
> ```

### 1.5 Tóm Tắt DFT/FFT

- DFT là công cụ **mạnh nhất** để phân tích miền tần số của tín hiệu rời rạc
- FFT làm DFT **thực tế và nhanh** cho ứng dụng real-time
- Windowing giúp **giảm spectral leakage** — tăng độ chính xác phân tích
- DFT/FFT là nền tảng cho mọi tác vụ speech processing: analysis → synthesis

---

## 2. Short-Time Fourier Analysis (STFT)

### 2.1 Tại Sao Phải Phân Tích Khung Ngắn?

**Tiếng nói là tín hiệu không dừng (Non-stationary)** — lưỡi và môi di chuyển liên tục, phổ âm thanh thay đổi từng mili-giây. Nếu lấy Fourier của cả câu 5 giây → kết quả là **mớ hỗn độn vô dụng**.

**Giải pháp:** Cắt tín hiệu thành các đoạn rất ngắn (~**20–30 ms**). Trong khoảng thời gian này, bộ máy phát âm chưa kịp cử động → coi tín hiệu là "**tạm thời dừng**" → trích xuất đặc trưng an toàn.

### 2.2 Công Thức STFT

$$X_{\hat{n}}(e^{j\hat{\omega}}) = \sum_{m=-\infty}^{\infty} x[m] \cdot w[\hat{n}-m] \cdot e^{-j\hat{\omega}m}$$

- $w[\hat{n}-m]$: **window function** — cửa sổ trượt trên tín hiệu
- Kết quả: **time-frequency representation** — biết tần số nào xuất hiện **vào lúc nào**

> [!info] STFT vs FFT thông thường
> - **FFT** → cho biết âm thanh có những **tần số nào**
> - **STFT** → cho biết tần số đó xuất hiện **vào lúc nào**
> - **Ứng dụng:** Spectrogram — đầu vào của CNN để nhận dạng giọng nói

### 2.3 Window Functions

| Window | Spectral Leakage | Đặc điểm |
|--------|-----------------|----------|
| **Rectangular** | Cao — cạnh sắc | Đơn giản nhất |
| **Hamming** | Thấp hơn — cạnh mượt | Phổ biến nhất trong speech |
| **Hanning** | Tương tự Hamming | Tapering khác |
| **Blackman** | Thấp nhất | Tapering nhiều hơn |

### 2.4 Heisenberg Trade-off — Sự Đánh Đổi Khốc Liệt

> [!warning] Nguyên lý bất định Heisenberg trong DSP
> Không thể đồng thời có **time resolution cao** VÀ **frequency resolution cao**.

| Window | Time Resolution | Frequency Resolution | Phù hợp |
|--------|----------------|---------------------|---------|
| **Dài** | Thấp (nhòe thời gian) | Cao (thấy rõ pitch, formant) | Phân tích âm vị ổn định |
| **Ngắn** | Cao (bắt được /t/, /p/) | Thấp (phổ bị nhòe) | Phát hiện onset âm |

> [!example] Ví dụ thực tế
> - Cửa sổ dài → thấy rõ các sóng hài (pitch) nhưng bỏ lỡ âm bật nhanh như /t/, /p/
> - Cửa sổ ngắn → bắt chính xác thời điểm phát âm /t/, nhưng phổ tần số bị nhòe

### 2.5 Tham Số STFT và Sự Đánh Đổi

| Tham số | Ảnh hưởng |
|---------|-----------|
| **Window Size** | Lớn → frequency resolution ↑, time resolution ↓ |
| **Overlap** | Nhiều → time resolution ↑, tính toán ↑ |
| **FFT Points** | Nhiều → frequency bins dày hơn, chậm hơn |

### 2.6 Trích Xuất Đặc Trưng Từ Tín Hiệu Ngắn Hạn

#### Short-Time Energy (STE)

$$E_{\hat{n}} = \sum_{m} \left(x[m] \cdot w[\hat{n}-m]\right)^2$$

- **Ý nghĩa vật lý:** Đo **độ lớn / âm lượng (Loudness)** của tiếng nói trong một khung
- **Ứng dụng:** VAD (Voice Activity Detection) — Google Assistant dùng STE để biết khi nào bạn đang nói

| Loại âm | Năng lượng | Lý do |
|---------|-----------|-------|
| **Voiced** (/a/, /e/) | Cao | Dây thanh rung mạnh → áp suất khí lớn |
| **Unvoiced** (/s/, /f/) | Thấp | Chỉ là luồng khí rít qua kẽ răng |

> [!important] Phân loại Voiced / Unvoiced bằng STE
> Bắt buộc phải có **Threshold value (Ngưỡng)**. Nếu $E_{\hat{n}} > \text{Threshold}$ → Voiced. Ngược lại → Unvoiced.

#### Short-Time Magnitude

$$M_{\hat{n}} = \sum_{m=0}^{L-1} |x[\hat{n}+m] \cdot w[m]|$$

Dùng **trị tuyệt đối** thay vì bình phương → **ít nhạy cảm hơn** với các điểm dị biệt có biên độ quá lớn (outliers).

#### Zero-Crossing Rate (ZCR)

ZCR đo **tốc độ tín hiệu cắt qua trục hoành** (0 Volt):

| Loại âm | ZCR | Lý do |
|---------|-----|-------|
| **Unvoiced** (/s/, /sh/, /f/) | **Cao** | Nhiễu tần số cao → sóng dao động cực nhanh |
| **Voiced** (/a/, /o/ — nguyên âm) | **Thấp** | Dao động chậm, tần số thấp |

> [!tip] Ứng dụng kết hợp STE + ZCR
> Dùng **cả hai** để phân loại V/U chính xác hơn: Voiced = năng lượng cao + ZCR thấp; Unvoiced = năng lượng thấp + ZCR cao.

> [!tip] Thực hành Python
> ```python
> from scipy import signal
> f, t, Zxx = signal.stft(x, fs=sr, window='hamming',
>                          nperseg=512, noverlap=256)
> plt.pcolormesh(t, f, np.abs(Zxx))
> plt.title('Spectrogram')
> ```

---

## 3. Overlap-Add Method (OLA)

### 3.1 Định Nghĩa & Perfect Reconstruction

**Overlap-Add** là kỹ thuật **tái tạo tín hiệu** từ các đoạn ngắn đã qua xử lý trong miền tần số.

$$y[n] = \sum_{r} y_r[n]$$

> [!important] Ưu điểm lớn nhất của OLA
> Nếu không có chỉnh sửa nào, OLA đảm bảo **khôi phục tín hiệu hoàn hảo 100% (perfect reconstruction)** so với ban đầu.

**Tại sao cần Overlap?** Khi windowing cắt tín hiệu, hai đầu frame bị suy giảm. Overlap-Add đảm bảo mỗi phần của tín hiệu gốc được đóng góp đủ vào đầu ra — tránh hiện tượng **discontinuities (giật cụ cục)**.

> [!example] Ứng dụng thực tế
> **Auto-Tune:** Chỉnh sửa pitch trong miền STFT → ráp lại bằng OLA → âm thanh liên tục, không bị giật.

### 3.2 Quy Trình OLA (6 bước)

```
Tín hiệu đầu vào x[n]
        │
        ▼ Bước 1: Frame Division
Chia thành các overlapping frames
        │
        ▼ Bước 2: Windowing
Áp dụng window function w[n] cho mỗi frame
        │
        ▼ Bước 3: Apply STFT
Chuyển từng frame → miền tần số
        │
        ▼ Bước 4: Modify Each Frame
Thực hiện các chỉnh sửa (lọc nhiễu, pitch shift...)
        │
        ▼ Bước 5: Apply ISTFT
Chuyển từng frame đã chỉnh → miền thời gian
        │
        ▼ Bước 6: Overlap and Add
Chồng lên nhau và cộng lại → tín hiệu đầu ra y[n]
```

### 3.3 Ứng Dụng OLA

- **Noise removal** — lọc tiếng ồn
- **Pitch shifting / Auto-Tune** — thay đổi cao độ giọng
- **Time stretching** — thay đổi tốc độ mà không thay đổi pitch
- **Speech enhancement** — tăng cường chất lượng tiếng nói


**2. Phương pháp Overlap-Add (OLA) (Câu 39)**

- **Bản chất:** Sau khi đã cắt âm thanh thành từng khung (frames), nhân với cửa sổ $w[n]$, và dùng STFT để chỉnh sửa (ví dụ: khử nhiễu, tăng giảm pitch), làm sao để ghép chúng lại thành file Audio ban đầu?
- **Cách làm đúng:** Bạn không thể cứ thế xếp chúng nối đuôi nhau. Do hiệu ứng của hàm cửa sổ (tín hiệu bị bóp nhỏ ở 2 đầu), bạn bắt buộc phải xếp chúng chồng lấp lên nhau (Overlap) rồi **Cộng các phần chồng lấp lại (Summing the overlapped segments)**. $$y[n] = \sum_{r=-\infty}^{\infty} y_r[n]$$
- **Ứng dụng:** Các phần mềm chỉnh phô giọng hát (Auto-Tune) hoạt động chính xác dựa trên thuật toán TD-PSOLA (Pitch Synchronous Overlap-Add) này!

---

## 4. Time-Decimated Filter Banks

### 4.1 Filter Banks Là Gì?

**Filter bank** = tập hợp các **band-pass filters** phân tách tín hiệu thành nhiều **subbands**. Ta không phân tích toàn bộ dải tần 0–8000 Hz cùng lúc mà chia nhỏ ra (ví dụ: 0–1 kHz, 1–2 kHz...).

```
Tín hiệu đầu vào
        │
        ├──→ [Low-pass]    → Subband 1 (0 ~ 1kHz)
        ├──→ [Band-pass]   → Subband 2 (1 ~ 2kHz)
        ├──→ [Band-pass]   → Subband 3 (2 ~ 4kHz)
        └──→ [High-pass]   → Subband N (4 ~ 8kHz)
```

**Ứng dụng trong speech processing:**
- **Compression** (nén) — giữ dải tần quan trọng
- **Feature extraction** — trích xuất đặc trưng theo dải tần
- **Synthesis** — tổng hợp tiếng nói

### 4.2 Time-Decimation (Giảm Mẫu)

Sau khi lọc, ta **giảm tốc độ lấy mẫu (Downsampling / Decimation)**:

> Subband có băng thông hẹp → theo định lý Nyquist → không cần sample rate cao → giảm mẫu an toàn.

**Lợi ích:** Giảm thiểu đáng kể **khối lượng tính toán tổng thể (reduces overall computational load)**.

### 4.3 Maximally Decimated Filter Bank

> [!important] Định nghĩa
> Filter bank được gọi là **"Maximally Decimated"** (giảm mẫu tối đa) khi:
> $$\text{Số kênh lọc} = \text{Hệ số giảm mẫu (downsampling factor)}$$

> [!example] Liên hệ thực tế — MP3
> Đây là kỹ thuật **cốt lõi của chuẩn nén MP3**: chia âm thanh thành 32 subbands → giảm mẫu tối đa từng dải → chỉ giữ lại những gì tai người nghe được → file nhỏ hơn nhiều lần.

### 4.4 Digital Filters trong Hệ Thống

**Mục đích chính của bộ lọc số:** Loại bỏ nhiễu và cải thiện độ rõ nét của tiếng nói (remove noise and improve speech clarity).

> [!example] Anti-Aliasing Filter
> Bộ lọc Low-pass (Anti-aliasing) luôn được đặt **trước bộ A/D converter** để cắt bỏ mọi thành phần tần số vượt quá $F_{max}$ — ngăn chặn Aliasing trước khi lấy mẫu.

### 4.5 Thiết Kế Time-Decimated Filter Banks

1. Thiết kế **prototype low-pass filter** (windowing hoặc optimization)
2. **Modulate** prototype → tạo toàn bộ filter bank
3. Đảm bảo các filter có **passbands không (hoặc ít) chồng nhau**

---

## 5. Two-Channel Filter Banks

### 5.1 Cấu Trúc

Two-Channel Filter Bank chia tín hiệu thành **2 sub-bands**: low-frequency và high-frequency.

**Hai nhánh chính:**

```
                    ┌─────────────────────────────────────┐
                    │         ANALYSIS FILTER BANK         │
Input x[n] ──→ [H0: Low-pass]  →  ↓2  →  v0[n]  (low sub-band)
           └──→ [H1: High-pass] →  ↓2  →  v1[n]  (high sub-band)
                    └─────────────────────────────────────┘

                    ┌─────────────────────────────────────┐
                    │        SYNTHESIS FILTER BANK         │
v0[n] → ↑2 → [G0: Low-pass synthesis]  ──→ ┐
v1[n] → ↑2 → [G1: High-pass synthesis] ──→ ┘ → (+) → Output y[n]
                    └─────────────────────────────────────┘
```

### 5.2 Analysis Filter Bank

| Thành phần | Chức năng |
|-----------|-----------|
| **H0 (Low-pass)** | Tách thành phần tần số thấp |
| **H1 (High-pass)** | Tách thành phần tần số cao |
| **Downsampler ↓2** | Giữ mỗi mẫu thứ 2 → giảm data rate 50% |

### 5.3 Synthesis Filter Bank

| Thành phần | Chức năng |
|-----------|-----------|
| **Upsampler ↑2** | Chèn zeros giữa các mẫu → tăng sample rate |
| **G0 (Low-pass synthesis)** | Tái tạo thành phần tần số thấp |
| **G1 (High-pass synthesis)** | Tái tạo thành phần tần số cao |
| **Cộng (+)** | Ghép hai sub-band → tín hiệu đầu ra |

### 5.4 Điều Kiện Perfect Reconstruction

Để tái tạo hoàn hảo ($y[n] = x[n]$), các filter analysis và synthesis phải được thiết kế phối hợp chặt chẽ — thường dùng **Quadrature Mirror Filters (QMF)**.

### 5.5 Tóm Tắt Two-Channel Filter Banks

- Phân tách và tái tạo tín hiệu **hiệu quả**
- Cân bằng **computational efficiency** và **signal quality**
- Nền tảng của wavelet transforms và audio codecs (MP3, AAC)
- to analyze a signal in two frequency bands
- to compress the signal data
- to perform time-domain filtering
- to separate noise from the signal

---

## Tóm Tắt Toàn Chương

```
Tín hiệu rời rạc x[n]
        │
        ▼
DFT / FFT ──────────────────── Phân tích phổ toàn cục
        │
        ▼
STFT + Windowing ───────────── Phân tích time-frequency
        │
        ▼
Spectrogram ────────────────── Biểu diễn trực quan 2D
        │
        ▼
Xử lý trong miền tần số
        │
        ▼
Overlap-Add (OLA) ─────────── Tái tạo tín hiệu
        │
        ▼
Filter Banks ──────────────── Phân tách theo dải tần
(Time-Decimated / Two-Channel)
```

| Công cụ | Mục đích chính |
|---------|---------------|
| **DFT/FFT** | Phân tích phổ, thực tế hóa Fourier |
| **Windowing** | Giảm spectral leakage |
| **STFT** | Phân tích time-frequency (non-stationary) |
| **Spectrogram** | Trực quan hóa 2D |
| **OLA** | Tổng hợp từ short-time frames |
| **Filter Banks** | Phân tích theo dải tần, compression |

---

## Liên Kết

- [[Chapter 5]] — Short-Time Analysis of Speech
- [[Chapter 6]] — Time-Domain Methods for Speech Processing
- [[Chapter 8]] — The Cepstrum and Homomorphic Speech Processing
- [[STFT]]
- [[MFCCs]]
- [[Spectrogram]]
- [[FFT]]

---

*Chapter 7 · Frequency-Domain Representations · Rabiner & Schafer · Tự học*
**4. Phân tích STFT và Phương pháp OLA (Câu 43, 59)**

- **Công thức STFT:** $$X_{\hat{n}}(e^{j\hat{\omega}}) = \sum_{m=-\infty}^{\infty} x[m]w[\hat{n}-m]e^{-j\hat{\omega}m}$$
- **Sự đánh đổi khốc liệt (Câu 43):** Hàm cửa sổ $w[m]$ sinh ra một nghịch lý vật lý (nguyên lý bất định Heisenberg). Cửa sổ quá dài $\rightarrow$ độ phân giải tần số tốt nhưng nhòe thời gian. Cửa sổ quá ngắn $\rightarrow$ bắt dính thời gian nhưng phổ tần số bị nhòe. Do đó, thách thức vĩnh cửu của STFT là **Cân bằng độ phân giải thời gian và tần số**.
- **Overlap-Add (OLA) (Câu 59):** Khi bạn chỉnh sửa âm thanh (ví dụ như Auto-Tune) trên miền STFT, bạn chia tín hiệu thành các khung. Để ráp chúng lại thành Audio ban đầu mà không bị giật cụ cục (discontinuities), bạn phải xếp chúng gối lên nhau (overlap) và cộng lại (add): $$y[n] = \sum_{r} y_r[n]$$ _Ưu điểm lớn nhất của OLA_ chính là nếu không có chỉnh sửa gì, nó đảm bảo **khôi phục lại tín hiệu hoàn hảo (perfect reconstruction)** 100% so với ban đầu.

**🇬🇧 2. The Window Length Trade-off (Q63)**

- **Concept:** This is the Heisenberg Uncertainty Principle in DSP! If you increase the window length $L$, you capture more wave cycles (better frequency resolution), but you lose exact timing (worse time resolution).
    - **Rule:** As window length increases $\rightarrow$ **Time resolution decreases, but frequency resolution increases.**

**🇻🇳 2. Sự đánh đổi kích thước cửa sổ (Câu 63)**

- **Giải thích:** Đây chính là Nguyên lý Bất định Heisenberg trong âm thanh! Khi bạn tăng chiều dài cửa sổ (window length) lên, bạn gom được nhiều chu kỳ sóng hơn $\rightarrow$ **Độ phân giải tần số tăng (nhìn rõ các vạch Formant)**. Nhưng bù lại, bạn sẽ không biết chính xác âm thanh đó phát ra ở mili-giây nào $\rightarrow$ **Độ phân giải thời gian giảm**.
