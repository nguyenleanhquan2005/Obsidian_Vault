# Đề Cương Chapter 2: Image and Video Processing
**Môn:** IMP302m  
**Trường:** FPT University

---

## Mục Lục

1. [2.1 Basic Linear Filtering](#21-basic-linear-filtering)
2. [2.2 Nonlinear Filtering](#22-nonlinear-filtering)
3. [2.3 Morphological Filtering](#23-morphological-filtering)
4. [2.4 Spatial Filters](#24-spatial-filters)
5. [2.5 Filtering in Frequency Domain](#25-filtering-in-frequency-domain)

---

## 2.1 Basic Linear Filtering with Application to Image Enhancement

### Khái niệm cơ bản
- **Linear system theory** là nền tảng của xử lý ảnh và video số
- Ứng dụng: contrast improvement, denoising, sharpening, target matching

### Hàm xung 2 chiều (2D Impulse Function)

$$\delta(m-p, n-q) = \begin{cases} 1 & \text{nếu } m=p \text{ và } n=q \\ 0 & \text{còn lại} \end{cases}$$

- Bất kỳ ảnh f nào cũng biểu diễn được qua hàm xung:

$$f(m,n) = \sum_{p=-\infty}^{\infty} \sum_{q=-\infty}^{\infty} f(p,q)\delta(m-p, n-q)$$

### Hệ thống tuyến tính (Linear System)

$$g(m,n) = \mathcal{L}[f(m,n)]$$

- Hệ thống **linear** khi thỏa **nguyên lý chồng chất (superposition)**:

$$a \cdot g_1(m,n) + b \cdot g_2(m,n) = \mathcal{L}[a \cdot f_1(m,n) + b \cdot f_2(m,n)]$$

### Linear Space-Invariant (LSI) & Tích chập

- Với hệ LSI, đầu ra là **tích chập (convolution)** giữa ảnh và hàm đáp ứng xung h:

$$g(m,n) = \sum_{p}\sum_{q} f(p,q) \cdot h(m-p, n-q) = f(m,n) * h(m,n)$$

- **h(m,n):** hàm đáp ứng xung (impulse response / filter kernel)

### Miền tần số (Frequency Domain)

- Tích chập trong miền không gian → **nhân** trong miền tần số:

$$G(U,V) = F(U,V) \cdot H(U,V)$$

### Ideal Low-Pass Filter

| Dạng | Công thức |
|------|-----------|
| Radial | $H(U,V) = 1$ nếu $\sqrt{U^2+V^2} \leq \Omega_c$, ngược lại = 0 |
| Rectangle | $H(U,V) = 1$ nếu $\|U\| \leq U_c$ và $\|V\| \leq V_c$, ngược lại = 0 |
| Spatial domain | $h(m,n) = U_c V_c \text{sinc}(2\pi U_c m) \cdot \text{sinc}(2\pi V_c m)$ |

> ⚠️ **Nhược điểm:** Gây hiện tượng **ringing** (dao động) tại biên ảnh

### Gaussian Filter

$$h(m,n) = \frac{1}{2\pi\sigma^2} \exp\left[-\frac{m^2+n^2}{2\sigma^2}\right]$$

- Đáp ứng tần số: $H(U,V) \approx e^{-2\pi^2\sigma^2(U^2+V^2)}$
- **σ càng lớn → làm mờ càng nhiều**
- Ưu điểm: Không gây ringing, chuyển tiếp mượt mà

---

## 2.2 Nonlinear Filtering for Image Analysis and Enhancement

### Tại sao dùng lọc phi tuyến?
- **Bảo toàn cạnh (edge preservation)** tốt hơn lọc tuyến tính
- Ít nhạy cảm với nhiễu
- Nhiễu (noise) xuất hiện tự nhiên trong quá trình thu ảnh (film-grain, nhiễu điện tử...)

### Median Smoother (Bộ làm mịn trung vị)

- Observation vector: $\mathbf{x}(n) = [x(n-N_L), \cdots, x(n+N_R)]^T$, với $N = N_L + N_R + 1$

$$y(n) = \begin{cases} x_{(\frac{N+1}{2})} & \text{nếu N lẻ} \\ \dfrac{x_{(\frac{N}{2})} + x_{(\frac{N}{2}+1)}}{2} & \text{còn lại} \end{cases}$$

> Sắp xếp các mẫu rồi lấy **giá trị ở giữa** — hiệu quả với nhiễu muối tiêu (salt-and-pepper)

### Weighted Median Smoother (Trung vị có trọng số)

**Các bước:**
1. Tính ngưỡng: $W_0 = \dfrac{1}{2}\displaystyle\sum_{i=1}^N W_i$
2. Sắp xếp các mẫu tăng dần
3. Cộng dồn trọng số từ mẫu **lớn nhất** đi xuống
4. Đầu ra = mẫu khi tổng trọng số $\geq W_0$

**Ví dụ:**

| | Giá trị |
|-|---------|
| Observation samples | 12, 6, 4, 1, 9 |
| Corresponding weights | 0.1, 0.1, 0.2, 0.2, 0.1 |
| Threshold $W_0$ | 0.35 |
| Sorted samples (tăng) | 1, 4, 6, 9, 12 |
| Partial weight sums | 0.7, **0.5**, 0.3, 0.2, 0.1 |
| **Output** | **4** |

### Weighted Median Filter (Trọng số có dấu âm)

**Các bước:**
1. Tính ngưỡng: $T_0 = \dfrac{1}{2}\displaystyle\sum_{i=1}^N |W_i|$
2. Sắp xếp mẫu **có dấu**: $\text{sgn}(W_i)X_i$
3. Cộng dồn **giá trị tuyệt đối** trọng số từ max xuống
4. Đầu ra = mẫu có dấu khi tổng $\geq T_0$

### Vector Weighted Median Filter (Ảnh màu)

- Mỗi pixel: $\mathbf{x}_i = [x_i^1, x_i^2, x_i^3]^T$ (3 kênh màu)
- Tìm β tối thiểu hóa:

$$\hat{\boldsymbol{\beta}} = \arg\min_{\boldsymbol{\beta}} \sum_{i=1}^N |W_i| \cdot ||\text{sgn}(W_i)\mathbf{x}_i - \boldsymbol{\beta}||$$

### Ứng dụng 1: Image Zooming

- **Mục đích:** Thêm pixel mới để tăng kích thước ảnh
- **Ứng dụng thực tế:** Web, DVD/Video, khoa học

**Weighted Medians in Interpolation:**
- Pixel mới = trung vị có trọng số của pixel lân cận
- Ưu điểm so với nội suy tuyến tính:
  - **Bảo toàn cạnh** sắc nét
  - **Giảm artifact** — không bị "blocky"

**Ví dụ phóng to 2x:**
```
Ảnh gốc 2×3 → Zero Interlace → 4×6 → Median Interpolation → 4×6 (đã nội suy)
```

### Ứng dụng 2: Image Sharpening

- Dùng weighted median filter mask:

$$W = \frac{1}{3}\begin{bmatrix} -1 & -1 & -1 \\ -1 & 8 & -1 \\ -1 & -1 & -1 \end{bmatrix}$$

- Kiến trúc: High-pass WM filter (×λ₁) và Pre-filtering → High-pass WM filter (×λ₂)
- **λ₁, λ₂:** tham số điều chỉnh độ sắc nét, thường chọn bằng nhau

---

## 2.3 Morphological Filtering for Image Enhancement and Feature Detection

### Mathematical Morphology là gì?
- Phương pháp **phi tuyến** dựa trên **lý thuyết tập hợp và lattice**
- Mô tả định lượng **cấu trúc hình học** của đối tượng trong ảnh
- Phép toán cơ bản: **union, intersection, complement**

### 4 Thuật toán cơ bản

#### Erosion (Xói mòn) — Thu nhỏ đối tượng
- **Input:** Binary image f(x,y) + Structuring Element (SE)
- **Điều kiện:** Nếu **TẤT CẢ** pixel dưới SE = 1 → g(x,y) = 1
- **Công dụng:** Loại bỏ nhiễu nhỏ, tách đối tượng dính nhau

#### Dilation (Giãn nở) — Mở rộng đối tượng
- **Input:** Binary image f(x,y) + Structuring Element (SE)
- **Điều kiện:** Nếu **BẤT KỲ** pixel nào dưới SE = 1 → g(x,y) = 1
- **Công dụng:** Lấp lỗ hổng nhỏ, nối các đối tượng gần nhau

#### Opening (Mở) — Erosion → Dilation
1. Erosion: f(x,y) + SE → f'(x,y)
2. Dilation: f'(x,y) + SE → g(x,y)
- **Công dụng:** Loại bỏ nhiễu nhỏ mà không thay đổi nhiều hình dạng chính

#### Closing (Đóng) — Dilation → Erosion
1. Dilation: f(x,y) + SE → f'(x,y)
2. Erosion: f'(x,y) + SE → g(x,y)
- **Công dụng:** Lấp đầy lỗ hổng và khoảng trống nhỏ trong đối tượng

### Tổng hợp 4 phép toán

| Phép | Chuỗi | Điều kiện | Công dụng |
|------|-------|-----------|-----------|
| Erosion | — | TẤT CẢ pixel = 1 | Thu nhỏ, loại nhiễu |
| Dilation | — | BẤT KỲ pixel = 1 | Mở rộng, nối đối tượng |
| Opening | E → D | — | Loại nhiễu nhỏ |
| Closing | D → E | — | Lấp lỗ hổng |

---

## 2.4 Spatial Filters

### Khái niệm
- Thay giá trị pixel bằng hàm của pixel đó và lân cận
- **Linear:** phép tính tuyến tính → **Linear spatial filter**
- **Phi tuyến:** → **Nonlinear spatial filter**

### Linear Spatial Filtering

$$g(x,y) = \sum_{s=-a}^{a} \sum_{t=-b}^{b} w(s,t) f(x+s, y+t)$$

- **Kernel w:** mảng 2D, kích thước = vùng lân cận, hệ số = loại lọc

### Spatial Correlation vs Convolution

$$\text{Correlation: } (w \star f) = \sum_{s,t} w(s,t)f(x+s, y+t)$$

$$\text{Convolution: } (w \star f) = \sum_{s,t} w(s,t)f(x-s, y-t)$$

- **Convolution = Correlation** khi kernel **đối xứng** qua tâm
- Convolution: xoay kernel 180° so với correlation

### Properties

| Tính chất | Convolution | Correlation |
|-----------|:-----------:|:-----------:|
| Giao hoán | ✓ f★g = g★f | ✗ |
| Kết hợp | ✓ | ✗ |
| Phân phối | ✓ | ✓ |

**Kích thước ảnh kết quả:**
$$S_v = m + M - 1 \quad ; \quad S_h = n + N - 1$$

**Lọc nhiều tầng Q (cùng kernel m×n):**
$$W_v = Q(m-1) + m \quad ; \quad W_h = Q(n-1) + n$$

---

### Smoothing Spatial Filters (Lowpass) — Làm mịn

#### Box Filter
$$W = \frac{1}{9}\begin{bmatrix}1&1&1\\1&1&1\\1&1&1\end{bmatrix}$$

- Lấy **trung bình** pixel trong cửa sổ
- Chia 1/9 để chuẩn hóa, tránh thay đổi độ sáng
- ⚠️ Nhược điểm: làm mờ cạnh

#### Lowpass Gaussian Filter
$$G(r) = Ke^{-\frac{r^2}{2\sigma^2}}$$

- Kernel 3×3: $\frac{1}{4.8976}\begin{bmatrix}0.3679&0.6065&0.3679\\0.6065&1.0000&0.6065\\0.3679&0.6065&0.3679\end{bmatrix}$
- σ càng lớn → làm mờ càng nhiều
- Mượt mà hơn Box filter

---

### Sharpening Spatial Filters (Highpass) — Làm sắc nét

#### Điều kiện đạo hàm trong ảnh số

| | Đạo hàm bậc 1 | Đạo hàm bậc 2 |
|--|:---:|:---:|
| Vùng cường độ không đổi | 0 | 0 |
| Bắt đầu bậc thang/dốc | ≠ 0 | ≠ 0 |
| Dọc theo dốc | ≠ 0 | **0** |
| Kết thúc bậc thang/dốc | ≠ 0 | **≠ 0** |

#### Laplacian

$$\nabla^2 f(x,y) = f(x+1,y) + f(x-1,y) + f(x,y+1) + f(x,y-1) - 4f(x,y)$$

4 biến thể kernel:

```
  0  1  0     1  1  1     0 -1  0    -1 -1 -1
  1 -4  1     1 -8  1    -1  4 -1    -1  8 -1
  0  1  0     1  1  1     0 -1  0    -1 -1 -1
```

#### Unsharp Masking & Highboost Filtering

**3 bước:**
1. Làm mờ ảnh gốc
2. Trừ ảnh mờ khỏi ảnh gốc → **mask**
3. Cộng mask vào ảnh gốc → ảnh sắc nét hơn

---

### Lowpass, Highpass, Bandreject, Bandpass

| Loại | Đặc điểm | Biểu diễn |
|------|----------|-----------|
| Lowpass | Giữ tần số thấp | $H_{LP}$ |
| Highpass | Giữ tần số cao | $H_{HP} = 1 - H_{LP}$ |
| Bandreject | Chặn một dải tần | $H_{LP1} + H_{HP2}$ |
| Bandpass | Giữ một dải tần | $1 - H_{BR}$ |

---

## 2.5 Filtering in the Frequency Domain

### 2D Discrete Fourier Transform (DFT)

$$F(u,v) = \sum_{x=0}^{M-1}\sum_{y=0}^{N-1} f(x,y) \, e^{-j2\pi\left(\frac{ux}{M}+\frac{vy}{N}\right)}$$

### 2D Inverse DFT (IDFT)

$$f(x,y) = \frac{1}{MN}\sum_{u=0}^{M-1}\sum_{v=0}^{N-1} F(u,v) \, e^{j2\pi\left(\frac{ux}{M}+\frac{vy}{N}\right)}$$

### Fourier Spectrum, Phase Angle, Power Spectrum

$$F(u,v) = R(u,v) + jI(u,v) = |F(u,v)|e^{j\Phi(u,v)}$$

| Đại lượng | Công thức |
|-----------|-----------|
| Fourier spectrum | $\|F(u,v)\| = [R^2(u,v) + I^2(u,v)]^{1/2}$ |
| Phase spectrum | $\Phi(u,v) = \arctan\left[\dfrac{I(u,v)}{R(u,v)}\right]$ |
| Power spectrum | $P(u,v) = \|F(u,v)\|^2 = R^2(u,v) + I^2(u,v)$ |

---

### 8 Bước Lọc Trong Miền Tần Số

| Bước | Mô tả |
|------|-------|
| 1 | Ảnh f(x,y) kích thước M×N → tính P = 2M, Q = 2N |
| 2 | Tạo ảnh đệm $f_p(x,y)$ kích thước P×Q (zero/mirror/replicate padding) |
| 3 | Nhân $f_p(x,y) \cdot (-1)^{x+y}$ để dịch DFT về trung tâm |
| 4 | Tính DFT → F(u,v) |
| 5 | Xây dựng H(u,v) kích thước P×Q, tâm tại (P/2, Q/2) |
| 6 | Nhân từng phần tử: G(u,v) = H(u,v) · F(u,v) |
| 7 | Tính IDFT: $g_p(x,y) = (\text{real}[\mathfrak{F}^{-1}\{G(u,v)\}])(-1)^{x+y}$ |
| 8 | Cắt góc trên trái M×N → ảnh kết quả g(x,y) |

---

### Image Smoothing — Lowpass Filters

Khoảng cách đến trung tâm:
$$D(u,v) = \left[(u-P/2)^2 + (v-Q/2)^2\right]^{1/2}$$

| Bộ lọc | Công thức |
|--------|-----------|
| Ideal LPF | $H = 1$ nếu $D \leq D_0$; $H = 0$ nếu $D > D_0$ |
| Gaussian LPF | $H(u,v) = e^{-D^2(u,v)/2D_0^2}$ |
| Butterworth LPF | $H(u,v) = \dfrac{1}{1+[D(u,v)/D_0]^{2n}}$ |

- **$D_0$:** tần số cắt (cutoff frequency)

---

### Image Sharpening — Highpass Filters

| Bộ lọc | Công thức |
|--------|-----------|
| Ideal HPF | $H_{HP} = 1 - H_{LP}$ |
| Gaussian HPF | $H_{HP}(u,v) = 1 - e^{-D^2(u,v)/2D_0^2}$ |
| Butterworth HPF | $H(u,v) = \dfrac{1}{1+[D_0/D(u,v)]^{2n}}$ |
| Laplacian | $H(u,v) = -4\pi^2(u^2+v^2)$ |

### Ứng dụng

- **Fingerprint (dấu vân tay nhòe):** Ảnh nhòe → Highpass filtering → Thresholding → Rõ nét
- **Moon image (ảnh mặt trăng mờ):** Ảnh mờ → Laplacian-based sharpening → Thấy rõ miệng núi lửa

---

## Tổng Kết

| Phần | Kỹ thuật chính | Ứng dụng |
|------|---------------|----------|
| 2.1 | Linear filtering, LSI, Convolution, Gaussian/LPF | Làm mờ, cải thiện tương phản |
| 2.2 | Median, Weighted Median, Vector WM | Khử nhiễu, zoom ảnh, làm sắc nét |
| 2.3 | Erosion, Dilation, Opening, Closing | Phân tích hình dạng, loại nhiễu hình thái |
| 2.4 | Box, Gaussian, Laplacian, Unsharp masking | Làm mịn, làm sắc nét (miền không gian) |
| 2.5 | DFT/IDFT, Ideal/Gaussian/Butterworth LP & HP | Lọc hiệu quả, phục hồi ảnh mờ |
