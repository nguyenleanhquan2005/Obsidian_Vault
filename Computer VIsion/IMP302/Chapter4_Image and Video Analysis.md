# Đề Cương Chapter 4: Image and Video Analysis
**Môn:** IMP302m  
**Trường:** FPT University

---

## Mục Lục

1. [4.1 Image Transforms](#41-image-transforms)
2. [4.2 Discrete Hartley Transform (DHT)](#42-discrete-hartley-transform-dht)
3. [4.3 Discrete Cosine Transform (DCT)](#43-discrete-cosine-transform-dct)
4. [4.4 Walsh-Hadamard Transform (WHT)](#44-walsh-hadamard-transform-wht)
5. [4.5 Wavelet Transform](#45-wavelet-transform)
6. [4.6 Multiscale Image Decompositions and Wavelets](#46-multiscale-image-decompositions-and-wavelets)
7. [4.7 Machine Learning based Image and Video Analysis](#47-machine-learning-based-image-and-video-analysis)

---

## 4.1 Image Transforms

### Định nghĩa
- **Image transforms** phân tích hàm thành **tổng có trọng số** của các hàm cơ sở trực giao (orthogonal) hoặc biorthogonal
- Nghiên cứu dựa trên **đại số tuyến tính** và **giải tích hàm**
- Ảnh được xem như **vector trong không gian vector** của tất cả các ảnh

### Tính chất (Properties)

| Tính chất | Mô tả |
|-----------|-------|
| Hệ số khai triển | Transforms biểu diễn hệ số của khai triển tuyến tính |
| Bảo toàn thông tin & năng lượng | Tất cả transforms của một ảnh chứa cùng thông tin và tổng năng lượng |
| Khả nghịch (Reversible) | Transforms có thể đảo ngược; chỉ khác nhau về phân phối thông tin/năng lượng giữa các hệ số |

---

## 4.2 Discrete Hartley Transform (DHT)

### Công thức 2D DHT

$$F_{\text{DHT}}(u,v) = \sum_{x=0}^{N-1}\sum_{y=0}^{M-1} f(x,y)\,\text{cas}\!\left(\frac{2\pi}{N}ux + \frac{2\pi}{M}vy\right)$$

Trong đó:
$$\text{cas}(x) = \cos(x) + \sin(x)$$

### Tính chất (Properties)

| Tính chất | Mô tả |
|-----------|-------|
| Real-valued output | Kết quả thực (không phức), đơn giản hóa tính toán |
| Symmetry | $H(u,v) = H(-u,-v)$ |
| Energy conservation | Bảo toàn tổng năng lượng tín hiệu (giống DFT) |
| Reversible | Có thể khôi phục lại ảnh gốc từ transform |
| Ma trận biến đổi | Real, orthogonal, và symmetric |

### Implementation
- Ví dụ với **N = 4** (xem slide)

---

## 4.3 Discrete Cosine Transform (DCT)

### Công thức 2D DCT

$$F_{\text{DCT}}(u,v) = \alpha(u)\alpha(v)\sum_{x=0}^{N-1}\sum_{y=0}^{M-1} f(x,y)\cos\!\left[\frac{(2x+1)u\pi}{2N}\right]\cos\!\left[\frac{(2y+1)v\pi}{2M}\right]$$

**Hệ số chuẩn hóa (normalization factors):**
$$\alpha(k) = \begin{cases} \sqrt{\dfrac{1}{N}} & \text{nếu } k = 0 \\[6pt] \sqrt{\dfrac{2}{N}} & \text{nếu } k \neq 0 \end{cases}$$

### Đặc điểm quan trọng

- Dải tần số tương đương DFT và DHT, nhưng **độ phân giải tần số gấp đôi**
- **Giả định:** 2N-point periodicity và **even symmetry** (thay vì N-point như DFT)
- 2N-point periodicity + even symmetry → **giảm thiểu discontinuity** và high-frequency artifact
- → Đây là ưu điểm quan trọng của DCT trong **nén ảnh (image compression)**

### Implementation
- Ví dụ với **N = 4** (xem slide)

---

### Discrete Sine Transform (DST)

**Công thức 2D DST:**

$$F_{\text{DST}}(u,v) = \frac{2}{\sqrt{(N+1)(M+1)}} \sum_{x=0}^{N-1}\sum_{y=0}^{M-1} f(x,y) \sin\!\left[\frac{(x+1)(u+1)\pi}{N+1}\right]\cos\!\left[\frac{(y+1)(v+1)\pi}{M+1}\right]$$

### So sánh DCT vs DST

| Đặc điểm | DCT | DST |
|----------|-----|-----|
| Dải tần số | Tương đương DFT | Tương đương DFT |
| Độ phân giải tần số | Gấp đôi DFT | Gấp đôi DFT |
| Thành phần DC (u=0) | **Có** | **Không có** |
| Symmetry | Even symmetric | Odd symmetric |
| Giả định tuần hoàn | 2N-point | 2(N+1)-point |
| Giảm boundary discontinuity | **Có** ✓ | **Không** ✗ |

> **Lý do DST không có DC component:** Giả định hàm là 2(N+1)-point periodic và **odd symmetric** → giá trị trung bình bằng 0

---

## 4.4 Walsh-Hadamard Transform (WHT)

### Khái niệm
- Biến đổi **non-sinusoidal** — phân tách tín hiệu thành tổ hợp tuyến tính của **Walsh functions** (+1 và -1)
- Phân tích tín hiệu thành tập **orthogonal square waveforms**
- Là **giải pháp thay thế** cho các biến đổi Fourier-based

### Công thức 2D WHT

$$F_{\text{WHT}}(u,v) = \boldsymbol{H}_N \cdot f(x,y) \cdot \boldsymbol{H}_N^T$$

**Ma trận Hadamard** được xây dựng đệ quy:

$$\boldsymbol{H}_1 = [1] \qquad \boldsymbol{H}_2 = \begin{bmatrix}\boldsymbol{H}_1 & \boldsymbol{H}_1 \\ \boldsymbol{H}_1 & -\boldsymbol{H}_1\end{bmatrix} = \begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}$$

$$\boldsymbol{H}_{2n} = \begin{bmatrix}\boldsymbol{H}_n & \boldsymbol{H}_n \\ \boldsymbol{H}_n & -\boldsymbol{H}_n\end{bmatrix}$$

### Inverse 2D WHT

$$f(x,y) = \frac{1}{N^2}\boldsymbol{H}_N \cdot F_{\text{WHT}}(u,v) \cdot \boldsymbol{H}_N^T$$

> **Đặc biệt:** Inverse WHT **giống hệt** forward WHT (chỉ thêm hệ số $\frac{1}{N^2}$) → dễ cài đặt

### Tính chất (Properties)

| Tính chất | Mô tả |
|-----------|-------|
| Orthogonality | Các hàm cơ sở trực giao → bảo toàn thông tin và năng lượng |
| Binary operations | Chỉ dùng **cộng và trừ** → hiệu quả cho phần cứng số |
| Computational efficiency | FWHT có độ phức tạp $O(NM\log(NM))$ — tương đương FFT |
| Lossless | Không mất thông tin, hoàn toàn khả nghịch |

### Ứng dụng (Applications)

| Ứng dụng | Mô tả |
|---------|-------|
| Image Compression | Dồn năng lượng vào ít hệ số (tương tự DCT nhưng tính toán đơn giản hơn) |
| Pattern Recognition | Trích xuất đặc trưng từ tín hiệu nhị phân 2D |
| Digital Signal Processing | Xử lý tín hiệu 2D cần transform nhanh, ít phức tạp |

---

## 4.5 Wavelet Transform

### Giới thiệu
- Nền tảng của **multiresolution theory** — lý thuyết đa độ phân giải
- Hợp nhất các kỹ thuật từ nhiều lĩnh vực:
  - **Subband coding** (xử lý tín hiệu)
  - **Quadrature mirror filtering** (nhận dạng giọng nói)
  - **Pyramidal image processing**
- Biểu diễn và phân tích tín hiệu tại **nhiều độ phân giải khác nhau**

---

### Discrete Wavelet Transform (DWT)

#### Scaling Function (Hàm tỷ lệ) — "Father wavelet"

$$\varphi_{j,k}(t) = \sqrt{2^j}\,\varphi(2^j t - k)$$

- **j:** scale (dilation) — độ co giãn
- **k:** translation — dịch chuyển

**Tính chất trực giao với các dịch chuyển nguyên:**

$$\varphi(t) = \sum_{k \in \mathbf{Z}} h_\varphi(k)\varphi_{j,k}(t) = \sum_{k \in \mathbf{Z}} h_\varphi(k)\sqrt{2}\,\varphi(2t-k)$$

**Scaling function coefficients:**

$$h_\varphi(k) = \langle\varphi(t),\,\sqrt{2}\,\varphi(2t-k)\rangle = \int_{-\infty}^{\infty}\varphi^*(t)\sqrt{2}\,\varphi(2t-k)\,dt$$

---

#### Mother Wavelet Function (Hàm wavelet mẹ)

$$\psi_{j,k}(t) = \sqrt{2^j}\,\psi(2^j t - k)$$

- Wavelet space **nằm trong** scaling space
- **Wavelet function coefficients:**

$$\psi(t) = \sum_{k \in \mathbf{Z}} h_\psi(k)\sqrt{2}\,\varphi(2t-k)$$

**Quan hệ giữa wavelet và scaling coefficients:**

$$h_\psi(k) = (-1)^k h_\varphi(1-k)$$

---

#### Phân tích tín hiệu bằng DWT

$$f(t) = \sum_k c_{j_0}(k)\varphi_{j_0,k}(t) + \sum_{j=0}^{\infty}\sum_k d_j(k)\psi_{j,k}(t)$$

| Hệ số | Tên | Công thức | Ý nghĩa |
|-------|-----|-----------|---------|
| $c_{j_0}(k)$ | Approximation coefficients | $\langle f(t), \varphi_{j_0,k}(t)\rangle$ | Thành phần xấp xỉ (thô) |
| $d_j(k)$ | Detail coefficients | $\langle f(t), \psi_{j,k}(t)\rangle$ | Thành phần chi tiết |

---

### Continuous Wavelet Transform (CWT)

**Scaling function đơn vị:**
$$\varphi(x) = \begin{cases}1 & \text{nếu } 0 \leq x < 1 \\ 0 & \text{còn lại}\end{cases}$$

**Ví dụ khai triển wavelet series** cho hàm $y = x^2$ ($0 \leq x \leq 1$):
- Xấp xỉ qua các không gian $V_0, V_1, V_2$ (càng lên cao càng chi tiết)
- Chi tiết bổ sung qua $W_0, W_1$ (wavelet coefficients)

---

## 4.6 Multiscale Image Decompositions and Wavelets

### 2D Discrete Wavelet Transform

Trong 2D, cần **1 scaling function** và **3 wavelets hướng**:

**Scaling function:**
$$\varphi(x,y) = \varphi(x)\varphi(y)$$

**3 Directionally sensitive wavelets:**

| Wavelet | Công thức | Hướng nhạy cảm |
|---------|-----------|----------------|
| $\psi^H(x,y)$ | $\psi(x)\varphi(y)$ | Columns (thay đổi theo cột) |
| $\psi^V(x,y)$ | $\varphi(x)\psi(y)$ | Rows (thay đổi theo hàng) |
| $\psi^D(x,y)$ | $\psi(x)\psi(y)$ | Diagonals (thay đổi theo đường chéo) |

> Các wavelet này đo **biến đổi cường độ** theo các hướng khác nhau trong ảnh

---

### Fast Wavelet Transform (FWT) — Forward

**Sơ đồ phân tích:**

```
                    ★h_ψ(-m) → [2↓] → T_ψ^D(j,k,l)   (chi tiết đường chéo)
         ★h_ψ(-n) → [2↓] ──┤
                    ★h_φ(-m) → [2↓] → T_ψ^V(j,k,l)   (chi tiết dọc)
T_φ(j+1,k,l) ──┤   (Columns)
                    ★h_ψ(-m) → [2↓] → T_ψ^H(j,k,l)   (chi tiết ngang)
         ★h_φ(-n) → [2↓] ──┤
                    ★h_φ(-m) → [2↓] → T_φ(j,k,l)     (xấp xỉ)
                   (Columns)
```

**Kết quả:** Ảnh được chia thành 4 vùng (subband):

```
┌─────────────┬─────────────┐
│  T_φ(j,k,l) │ T_ψ^H(j,k,l)│  ← Approximation | Horizontal detail
├─────────────┼─────────────┤
│ T_ψ^V(j,k,l)│ T_ψ^D(j,k,l)│  ← Vertical detail | Diagonal detail
└─────────────┴─────────────┘
```

- **m, n:** biến của phép tích chập (convolution)
- **2↓:** downsampling (giảm mẫu) hệ số 2

---

### Inverse Fast Wavelet Transform (IFWT)

**Sơ đồ tổng hợp (ngược lại FWT):**
- Các bước **upsample** (2↑) thay vì downsample
- Kết hợp 4 subband lại thành ảnh gốc $T_\varphi(j+1,k,l)$

---

### Ví dụ 2D DWT

Với ảnh 8×8 và scaling function đơn vị $\varphi(x) = 1$ nếu $0 \leq x < 1$:

```
Input image (8×8):
[ 2  2  2  2  2  2  2  1]
[33 32 31 32 33 33 31 30]
[33 33 32 33 33 33 31 29]
[34 33 32 33 34 33 29 28]
[32 31 30 31 33 31 28 27]
[30 29 28 29 31 30 28 27]
[29 28 28 28 30 30 28 25]
[28 31 28 27 28 29 28 28]
```

→ Sau DWT: tách thành 4 subband (approximation + 3 detail)

---

## 4.7 Machine Learning based Image and Video Analysis

> *(Nội dung chi tiết theo slide/tài liệu bổ sung từ giảng viên)*

---

## So Sánh Tổng Hợp Các Transforms

| Transform | Hàm cơ sở | Đặc điểm nổi bật | Ứng dụng chính |
|-----------|-----------|-----------------|----------------|
| DHT | cas(x) = cos(x)+sin(x) | Real-valued, symmetric | Thay thế DFT với kết quả thực |
| DCT | cos | 2N-periodicity, even symmetry, gấp đôi freq. resolution | Nén ảnh (JPEG), video (MPEG) |
| DST | sin | Không có DC, odd symmetry | Ít dùng trong ảnh |
| WHT | +1/-1 (Walsh functions) | Chỉ cộng/trừ, lossless, O(NM·log(NM)) | Compression, Pattern recognition |
| DWT | φ (scaling) + ψ (wavelet) | Đa độ phân giải, bảo toàn vị trí-tần số | Nén ảnh (JPEG2000), denoising |

---

## Tổng Kết

| Phần | Nội dung chính |
|------|---------------|
| 4.1 | Khái niệm image transforms: orthogonal basis, reversible, energy conservation |
| 4.2 | DHT: cas function, real-valued, symmetric, energy conservation |
| 4.3 | DCT: 2N-periodicity + even symmetry → ít artifact → nén ảnh; DST: odd symmetric, no DC |
| 4.4 | WHT: Walsh functions (+1/-1), chỉ dùng cộng/trừ, FWHT O(NMlog(NM)) |
| 4.5 | Wavelet: scaling function φ + mother wavelet ψ, approximation & detail coefficients |
| 4.6 | 2D DWT: 3 wavelets hướng (H, V, D), FWT/IFWT, phân tích đa độ phân giải |
| 4.7 | Machine learning cho Image & Video analysis |
