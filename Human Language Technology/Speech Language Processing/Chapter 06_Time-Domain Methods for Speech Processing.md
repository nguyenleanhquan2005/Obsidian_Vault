---
tags:
  - speech-processing
  - time-domain
  - filter-banks
  - chapter-6
aliases:
  - Time-Domain Methods
  - Phương Pháp Miền Thời Gian
date: 2026-03-24
status: complete
---

# Chapter 6 — Time-Domain Methods for Speech Processing

> [!abstract] Tóm tắt chương
> Chương này đi sâu vào các phương pháp xử lý tiếng nói trong miền thời gian: bộ lọc số, biên độ ngắn hạn, và đặc biệt là Filter Banks với kỹ thuật Decimation — nền tảng của MP3 và nhiều hệ thống nén âm thanh hiện đại.

---

## Bản đồ nội dung

```

Time-Domain Methods for Speech Processing
├── 1. Short-Time Analysis Framework
│   ├── Bản chất của Windowing (Framing)
│   └── Phân tích theo thời gian thực (Sample-by-sample vs Block processing)
├── 2. Năng lượng & Biên độ ngắn hạn (STE & STM)
│   ├── Công thức tính STE (Bình phương) và STM (Trị tuyệt đối)
│   ├── Khác biệt cốt lõi: Tính nhạy cảm với nhiễu outlier ★
│   └── Ứng dụng: Dò tìm điểm bắt đầu/kết thúc (Endpoint Detection)
├── 3. Tỷ lệ qua điểm không (Short-Time Zero-Crossing Rate - ZCR)
│   ├── Khái niệm & Công thức (Hàm signum)
│   ├── Bản chất vật lý: Âm vô thanh (ZCR cao) vs Âm hữu thanh (ZCR thấp) ★
│   └── Sự cần thiết của bộ lọc loại bỏ DC Offset
├── 4. Hàm tự tương quan ngắn hạn (STACF)
│   ├── Công thức & Tính chất (Dò chu kỳ Pitch)
│   ├── Vấn đề giảm biên độ (Tapering effect) ở độ trễ lớn
│   └── Modified STACF (Khắc phục nhược điểm của STACF)
└── 5. Hàm sai phân biên độ trung bình (AMDF)
    ├── Công thức tính (Không cần phép nhân) ★
    └── Ứng dụng dò Pitch cực nhanh cho hệ thống nhúng
```





## 1  Short-Time Analysis & Windowing (Khung Phân Tích Ngắn Hạn)


 Tiếng nói của con người thay đổi liên tục theo thời gian thực, nhưng bộ máy phát âm (môi, lưỡi, thanh đới) bị giới hạn bởi quán tính cơ học, nên nó không thể biến đổi quá nhanh. Tiếng nói biến thiên theo thời gian nhưng do giới hạn cơ học của bộ máy phát âm, tín hiệu có thể được xem là gần như tĩnh trong các khoảng ngắn (10–40 ms). Vì vậy, ta sử dụng kỹ thuật **windowing (framing)** để trích xuất từng đoạn tín hiệu cục bộ bằng cách nhân với hàm cửa sổ trượt.

$$
x_n[m] = x[m] \cdot w[n - m]
$$

Trong đó $w[n-m]$ là cửa sổ giúp cô lập tín hiệu quanh thời điểm $n$, đồng thời hoạt động như một bộ lọc thông thấp, giảm nhiễu và hiện tượng spectral leakage.

- **Framing (Phân khung - Hành động "cắt" dữ liệu):**
    - Tín hiệu tiếng nói thay đổi liên tục theo thời gian. Để máy tính có thể phân tích, ta phải chia (segment) chuỗi tín hiệu dài đó thành các đoạn ngắn hơn có độ dài cố định (thường từ 10ms đến 40ms), và các đoạn này có thể xếp chồng lên nhau (overlapping).
    - _Mục đích:_ Bắt (capture) được các đặc tính động theo thời gian của tín hiệu tại một thời điểm cục bộ. Các tham số chính của Framing là kích thước khung (frame size - N) và bước trượt (frameshift/hop size).
	- - **Overlapping frames (Khung chồng lấp):** Các khung tín hiệu được đặt đè lên nhau (ví dụ trượt 10ms cho một khung dài 40ms) để bắt kịp các động lực học theo thời gian của tín hiệu và tránh làm mất mát thông tin ở các ranh giới.
	- **Non-overlapping frames (Khung không chồng lấp):** Các khung được cắt nối tiếp nhau mà không có phần dữ liệu nào bị lặp lại giữa hai khung liền kề.


- **Windowing (Áp dụng hàm cửa sổ - Hành động "mài dũa" dữ liệu):**
    - Đây là thao tác toán học áp dụng lên từng khung (frame) _đã được cắt ra_ ở bước trên. Tín hiệu trong khung sẽ được nhân với một hàm cửa sổ (ví dụ: Hamming, Hanning) theo công thức xw​[n]=x[n]⋅w[n].
    - _Mục đích:_ Khi  "cắt" tín hiệu bằng Framing, tín hiệu sẽ bị đứt gãy đột ngột ở hai đầu mút của khung tạo ra sự gián đoạn. Windowing sinh ra để "vuốt nhọn" (taper) hoặc làm giảm dần biên độ của phần tín hiệu ở hai đầu mút này về 0, giúp giảm thiểu sự gián đoạn giữa các ranh giới khung (reduce discontinuities).

---

### 1.1 Công thức tổng quát (Short-time processing)

Mọi đặc trưng miền thời gian (Energy, ZCR, Autocorrelation,...) đều có dạng:

$$
Q_n = \sum_{m=-\infty}^{\infty} T(x[m]) \, \tilde{w}[n - m]
$$

- $Q_n$: đặc trưng tại thời điểm $n$  
- $T(x[m])$: phép biến đổi (ví dụ: $x^2$, $|x|$) (áp dụng lên mẫu tín hiệu (Ví dụ: với tính Năng lượng thì T(x)=x2, với tính Biên độ thì T(x)=∣x∣)) 
- $\tilde{w}[n-m]$: cửa sổ (lowpass filter) (làm mịn sự biến thiên của tín hiệu và tránh hiện tượng rò rỉ phổ (spectral leakage) ở hai đầu mút,.)

---

### 1.2 Các hàm cửa sổ phổ biến

**Rectangular window:**

$$
w_R[n] =
\begin{cases}
1, & 0 \le n \le L-1 \\
0, & \text{otherwise}
\end{cases}
$$

**Hamming window:**

$$
w_H[n] =
\begin{cases}
0.54 - 0.46 \cos\left(\frac{2\pi n}{L-1}\right), & 0 \le n \le L-1 \\
0, & \text{otherwise}
\end{cases}
$$

---

### 1.3 Block Processing & Overlap

Thay vì xử lý từng mẫu ($R=1$), ta dùng xử lý theo khối:

- Frame length: $L$ (ví dụ: 40 ms)  
- Step size: $R > 1$ (ví dụ: 10–15 ms)  

$$
\text{Overlap} = L - R
$$

- Overlap thường > 50% để không mất thông tin chuyển tiếp  
- Bản chất: giảm số lượng mẫu đầu ra (**downsampling**) → tối ưu tính toán  


### Tóm tắt trực quan

```
text
Signal:   ────────────────
Window:     [=====]
              [=====]
                 [=====]

L = frame length
R = step (shift)
Overlap = L - R
```

### 1.4 CÁC SƠ ĐỒ KHỐI VÀ BIỂU ĐỒ MINH HỌA (Diagrams)

Trong sách giáo trình, có 2 sơ đồ cực kỳ quan trọng để minh họa cho nguyên lý này:

**A. Sơ đồ khối nguyên lý phân tích ngắn hạn (Figure 6.5 - General representation)** Sơ đồ này (nằm ở trang 245 của sách) mô tả quá trình xử lý tín hiệu như một hệ thống Lọc tuyến tính:



![[Pasted image 20260325222808.png]]


1. Tín hiệu gốc x[n] đi qua một khối biến đổi phi tuyến/tuyến tính T(⋅).
2. Sau đó, tín hiệu tiếp tục đi qua một **Bộ lọc thông thấp (Lowpass Filter)** có đáp ứng xung chính là hàm cửa sổ w~[n].
3. Đầu ra thu được là dãy tham số $Q_n$​ thay đổi chậm theo thời gian.

**B. Sơ đồ minh họa Xử lý theo khối (Figure 6.4 - Frames and Windows in short-time processing)** Sơ đồ này trực quan hóa khái niệm **Block processing** và **Overlap**.

![[Pasted image 20260325222934.png]]

- **Hình ảnh thể hiện:** Một đồ thị sóng âm dài, bên dưới là các hình thang/hình chuông (cửa sổ) đặt chồng lên nhau (overlap) dọc theo trục thời gian.
- **Thông số thực tế minh họa:** Sơ đồ dùng một tín hiệu có tần số lấy mẫu Fs​=16,000 Hz. Cửa sổ có chiều dài L=641 mẫu (tương đương 40 msec). Thay vì trượt từng mẫu một (R=1), cửa sổ nhảy các bước dài R=240 mẫu (tương đương bước nhảy 15 msec).
- **Độ chồng lấp (Overlap):** Sơ đồ chỉ rõ các cửa sổ đè lên nhau một khoảng là L−R=641−240=401 mẫu (chồng lấp hơn 50%). Thao tác nhảy bước R>1 này chính là quá trình **giảm mẫu (downsampling)** dữ liệu đầu ra, giúp giảm tải khối lượng tính toán mà không làm mất thông tin biến thiên của thanh quản.


---

## 2. Biên Độ Ngắn Hạn (Short-Time Magnitude)

### 2.1 Công Thức

$$M_{\hat{n}} = \sum_{m=0}^{L-1} |x[\hat{n}+m] \cdot w[m]|$$

### 2.2 Tại Sao Dùng Trị Tuyệt Đối?

Thay vì bình phương (như STE), dùng **trị tuyệt đối** giúp hệ thống:
- **Ít nhạy cảm** hơn với các điểm dị biệt (outliers) có biên độ quá lớn
- Bình phương sẽ **khuếch đại quá mức** các giá trị bất thường, làm sai kết quả

$E[\hat{n}] = \sum_{m=0}^{L-1} (x[\hat{n}+m]w[m])^2$

| Phương pháp | Công thức | Nhạy với Outlier | Độ nhạy V/U |
|------------|-----------|-----------------|-------------|
| **STE** | $(x \cdot w)^2$ | Cao | Rất cao |
| **STM** | $\|x \cdot w\|$ | **Thấp** | Trung bình |

---

## 3. Filter Banks & Decimation

### 3.1 Vấn Đề: Phân Tích Toàn Dải Tần Tốn Tài Nguyên

Phân tích tần số độ phân giải cao trên toàn dải 0–8000 Hz cùng lúc đòi hỏi **quá nhiều tài nguyên CPU** — không thực tế cho hệ thống thời gian thực.

### 3.2 Giải Pháp: Filter Bank

Thay vì phân tích toàn bộ, **chia tín hiệu thành các subbands nhỏ hơn**:

```
Tín hiệu x[n]  (0 ~ 8000 Hz)
        │
        ├──→ [LPF: 0~1kHz]    → Subband 1
        ├──→ [BPF: 1~2kHz]    → Subband 2
        ├──→ [BPF: 2~4kHz]    → Subband 3
        └──→ [HPF: 4~8kHz]    → Subband 4
```

Mỗi subband có **băng thông hẹp hơn** → theo định lý Nyquist → **không cần sample rate cao** → có thể **giảm mẫu (Downsampling/Decimation)** an toàn.

### 3.3 Maximally Decimated Filter Bank

> [!important] Định nghĩa
> Filter bank được gọi là **"Maximally Decimated"** (Giảm mẫu tối đa) khi:
>
> $$\text{Số kênh lọc (M)} = \text{Hệ số giảm mẫu (N)}$$
>
> Tức là mỗi subband được giảm mẫu đúng bằng số lượng kênh.

**Ví dụ:** 4 kênh lọc → mỗi kênh giảm mẫu 4 lần → tổng số mẫu giữ nguyên.

> [!example] Kỹ thuật cốt lõi của MP3
> Chuẩn nén **MP3** dùng Maximally Decimated Filter Bank với **32 subbands**:
> 1. Chia âm thanh thành 32 dải tần
> 2. Giảm mẫu tối đa từng dải
> 3. Áp dụng Auditory Masking → xóa các dải không nghe thấy
> 4. Kết quả: file nhỏ hơn **10–12 lần** mà chất lượng nghe gần như không đổi

### 3.4 Lợi Ích Chính

> Decimation **giảm thiểu đáng kể khối lượng tính toán tổng thể** (reduces overall computational load).

---

## 4. Time-Decimated Filter Banks (Chi Tiết)

### 4.1 Cấu Trúc Đầy Đủ

```
Input x[n]
    │
    ├──→ [H0] → ↓M → v0[n]  (subband 0)
    ├──→ [H1] → ↓M → v1[n]  (subband 1)
    ├──→ [H2] → ↓M → v2[n]  (subband 2)
    │    ...
    └──→ [HM-1] → ↓M → vM-1[n]  (subband M-1)
```

Ký hiệu $\downarrow M$ = **giảm mẫu** (giữ 1 mẫu, bỏ M-1 mẫu).

### 4.2 Thiết Kế Filter Bank

**Quy trình thiết kế:**
1. Thiết kế **prototype low-pass filter** (dùng windowing hoặc tối ưu hóa)
2. **Modulate (điều chế)** prototype → tạo toàn bộ M bộ lọc bandpass
3. Đảm bảo các filter có **passbands không (hoặc ít) chồng nhau**
4. Chọn hệ số giảm mẫu M phù hợp

### 4.3 So Sánh với Two-Channel Filter Bank

| | **Time-Decimated (M kênh)** | **Two-Channel** |
|-|---------------------------|----------------|
| **Số kênh** | M kênh (M > 2) | 2 kênh |
| **Độ phân giải** | Cao hơn | Thấp hơn |
| **Phức tạp** | Cao hơn | Đơn giản hơn |
| **Ứng dụng** | MP3, speech coding | Wavelet 1 cấp |

---

## 5.Tỷ Lệ Qua Điểm Không Ngắn Hạn (Short-Time Zero-Crossing Rate - ZCR)

[!important] Định nghĩa Zero-Crossing Rate (ZCR) là thước đo đếm số lần tín hiệu âm thanh đổi dấu (từ âm sang dương hoặc ngược lại) trong một khung thời gian nhất định. Trong miền thời gian, đây là công cụ đơn giản nhưng sức mạnh cực lớn để ước lượng **tần số thô** của tín hiệu.

### 5.1 Zero-Crossing Rate (ZCR)

Công thức tính Zero-Crossing Rate (ZCR) cho một khung tín hiệu được định nghĩa như sau:

$$
Z_n = \frac{1}{2L} \sum_{m=n-L+1}^{n} \left| \operatorname{sgn}(x[m]) - \operatorname{sgn}(x[m-1]) \right|
$$

Trong đó hàm dấu được xác định bởi:

$$
\operatorname{sgn}(x) =
\begin{cases}
1, & x \ge 0 \\
-1, & x < 0
\end{cases}
$$

với $L$ là chiều dài của khung phân tích. Về bản chất vật lý, ZCR là một đặc trưng quan trọng để phân biệt giữa âm hữu thanh (voiced) và âm vô thanh (unvoiced). Đối với âm hữu thanh (như nguyên âm), do dây thanh đới rung nên năng lượng tập trung ở dải tần thấp, khiến tín hiệu dao động chậm và dẫn đến ZCR thấp. Ngược lại, âm vô thanh (như /s/, /f/, /sh/) được tạo ra bởi luồng khí nhiễu đi qua các khe hẹp, tạo ra tín hiệu có tần số cao và dao động nhanh, do đó ZCR cao. Thông thường, âm hữu thanh có năng lượng cao nhưng ZCR thấp, trong khi âm vô thanh có năng lượng thấp nhưng ZCR cao.


### 5.2 Bản Chất Vật Lý: Hữu Thanh (Voiced) vs. Vô Thanh (Unvoiced)

ZCR là "khắc tinh" của các âm vô thanh (như /s/, /f/, /sh/). Tại sao?

- **Âm Hữu thanh (Voiced - Vowels):** Do dây thanh đới rung, năng lượng tập trung ở tần số thấp (dưới 3kHz). Sóng dao động chậm → **ZCR THẤP**.
- **Âm Vô thanh (Unvoiced - Fricatives):** Do luồng khí rít qua kẽ răng tạo nhiễu ngẫu nhiên dải rộng. Năng lượng tập trung ở tần số rất cao. Sóng dao động cực nhanh → **ZCR CAO**.

| Đặc trưng                         | Âm Hữu Thanh (Voiced) | Âm Vô Thanh (Unvoiced) |
| --------------------------------- | --------------------- | ---------------------- |
| **Năng lượng (Energy/Magnitude)** | Cao                   | Thấp                   |
| **ZCR (Zero-Crossing)**           | **Thấp**              | **Cao**                |
| Tần số chủ đạo                    | Thấp (Low-frequency)  | Cao (High-frequency)   |

### 5.3 Ứng Dụng Thực Tiễn và Cạm Bẫy (Senior Note)

1. ZCR hiếm khi được dùng một mình vì nó dễ bị nhiễu. Kỹ sư luôn kết hợp **ZCR (Đo tần số thô) + Short-Time Energy (Đo năng lượng)** để tạo thành thuật toán **Endpoint Detection (Phát hiện điểm đầu/cuối của câu nói)**.
2. **Ứng dụng trong Endpoint Detection (VAD):** AI dùng ZCR kết hợp với Năng lượng (Energy) để tìm điểm bắt đầu và kết thúc của một câu nói (Speech-Background Discrimination). Nếu chỉ dùng Energy, máy sẽ cắt nhầm mất đuôi chữ "S" trong từ "Six" vì năng lượng chữ "S" rất nhỏ. Nhờ có ZCR vọt lên cao đột ngột, máy sẽ nhận ra: _"À, đây là âm vô thanh, người dùng vẫn đang nói!"_.
3. **Cạm bẫy "DC Offset" (Lỗi chí mạng của Junior):** Để tính ZCR chính xác, tín hiệu **BẮT BUỘC** phải đi qua bộ lọc High-pass (chống nhiễu tần số cực thấp hoặc DC offset do micro bị lệch dòng điện). Nếu tín hiệu bị lệch lên trên trục hoành (DC offset = 0.75), sóng âm không cắt qua trục 0 nữa, làm ZCR đếm sai hoàn toàn (giảm từ 124 xuống 82 lần cắt).

## 6. Short-Time Autocorrelation Function (STACF)

Hàm tự tương quan ngắn hạn (STACF) được sử dụng để đo tính tuần hoàn (periodicity) của tín hiệu tiếng nói.

**Công dụng chính:**  
- Dò chu kỳ Pitch ($N_p$) của tín hiệu tiếng nói  
- Phân biệt âm **hữu thanh (voiced)** và **vô thanh (unvoiced)**  
- Phân tích tính tuần hoàn của tín hiệu

### Công thức

$$
R_n[k] = \sum_{m=0}^{L-1-k} s_n[m] \, s_n[m+k]
$$

- $s_n[m]$: khung tín hiệu tại thời điểm $n$  
- $L$: độ dài khung  
- $k$: độ trễ (lag)

### Ý nghĩa vật lý

- **Âm hữu thanh (Voiced):** tín hiệu có tính chu kỳ → xuất hiện các đỉnh (peaks) tại $k = N_p, 2N_p, ...$  
- **Âm vô thanh (Unvoiced):** tín hiệu nhiễu → không có đỉnh rõ ràng  

### Vấn đề tapering (suy giảm biên độ)

Khi $k$ tăng:
$$
\text{số mẫu} = L - k
$$

→ số mẫu giảm → biên độ tương quan giảm → dễ sai lệch khi dò pitch.

### Modified STACF (khắc phục)

$$
\hat{R}_n[k] = \sum_{m=0}^{L-1} x[n+m] \, x[n+m+k]
$$

→ luôn sử dụng $L$ mẫu → loại bỏ tapering effect.

---

## 7. Average Magnitude Difference Function (AMDF)

AMDF là phiên bản tối ưu tính toán của STACF, thay phép nhân bằng phép trừ. Phù hợp hệ thống có tài nguyên hạn chế

### Công thức

$$
\gamma_n[k] = \sum_{m} \left| x[n+m] - x[n+m-k] \right|
$$

### Ý tưởng chính

- STACF → tìm **đỉnh (peaks)**  
- AMDF → tìm **đáy (valleys)**  

Nếu $k = N_p$:
$$
x[n+m] \approx x[n+m-k]
$$

→ hiệu ≈ 0 → $\gamma_n[k]$ nhỏ nhất

### Ưu điểm

- Không dùng phép nhân → nhanh hơn  
- Phù hợp hệ nhúng / vi điều khiển  
- Tính toán nhẹ nhưng vẫn hiệu quả trong dò pitch
- - Embedded systems (vi điều khiển, DSP)  
- Real-time speech processing  
- Mobile / thiết bị nhỏ

**3. Autocorrelation vs. AMDF trong dò Pitch (Câu 48, 53)**

- **Autocorrelation (STACF - Câu 53):** Hàm tự tương quan sử dụng phép NHÂN ($R[k] = \sum x[m]x[m+k]$). Nó dịch chuyển tín hiệu đi một độ trễ $k$, nhân và cộng lại. Mục đích chính là tìm ra các đỉnh lặp lại để **xác định tần số cơ bản (F0) của tín hiệu tuần hoàn**.
- **AMDF (Câu 48):** Hàm sai biệt biên độ trung bình sử dụng phép TRỪ ($\gamma[k] = \sum |x[m] - x[m-k]|$). Khi tín hiệu lặp lại một chu kỳ, hiệu số của chúng sẽ tiến về 0 (tạo ra một "Thung lũng" - Valley). _Mục đích của AMDF cũng là để ước lượng Pitch_.
- _Tại sao kỹ sư lại thích AMDF?_ Vì phép trừ (Subtraction) và lấy trị tuyệt đối chạy trên các chip vi điều khiển (DSP/IoT) nhanh hơn phép nhân (Multiplication) rất nhiều!

## 8. Liên Hệ Với Speech Processing Hiện Đại

| Kỹ thuật                   | Ứng dụng                        |
| -------------------------- | ------------------------------- |
| **Digital Filters**        | Noise reduction, Anti-aliasing  |
| **Filter Banks**           | MP3, AAC, speech compression    |
| **Maximally Decimated FB** | Giảm tải tính toán trong ASR    |
| **Short-Time Magnitude**   | Robust feature cho noisy speech |

---

## Tóm Tắt

```
Speech Signal
        │
        ▼
[Digital Filter]  → Loại bỏ nhiễu, Anti-aliasing
        │
        ▼
[Filter Bank]     → Phân rã thành subbands
        │
        ▼
[Decimation ↓M]   → Giảm computational load
        │
        ▼
Subbands → Feature extraction cho từng dải tần
```

---

## Liên Kết

- [[Chapter 5]] — Short-Time Analysis (STE, ZCR, Windowing)
- [[Chapter 7]] — Frequency-Domain Representations (STFT, OLA, Two-Channel FB)
- [[Chapter 2]] — DSP Fundamentals (Sampling, Nyquist, FIR/IIR)
- [[MP3 Compression]]
- [[VAD]]

---

*Chapter 6 · Time-Domain Methods for Speech Processing · Rabiner & Schafer · Tự học*

