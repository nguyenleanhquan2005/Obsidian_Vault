# Chương 3: Image Degradation, Restoration & Reconstruction

> **Môn:** Xử lý ảnh số | **Slides:** 32 | **Tags:** #image-processing #computer-vision #restoration

---

## 📋 Mục lục

- [[#3.1 – Mô hình phục hồi ảnh]]
- [[#3.2 – Mô hình nhiễu (Noise Models)]]
- [[#3.3 – Lọc không gian & Tần số]]
- [[#3.4 – Hàm suy giảm & Ước lượng PSF]]
- [[#3.5 – Wavelet Denoising]]
- [[#3.6 – Bộ lọc Wiener (MMSE)]]
- [[#3.7 – Lọc CLS (Constrained Least Squares)]]
- [[#3.9 – Tái tạo từ hình chiếu (CT Scan)]]
- [[#3.10 – Ảnh đa kênh (Multichannel)]]
- [[#3.11–3.12 – Phát hiện chuyển động & Phục hồi video]]
- [[#🔑 Công thức cốt lõi cần thuộc]]
- [[#🤖 Kết nối AI / Deep Learning]]
- [[#❓ Câu hỏi ôn tập]]

---

## 3.1 – Mô hình phục hồi ảnh
> *Slides 2–3*

### Ý tưởng cốt lõi
Khôi phục ảnh là quá trình **tìm lại ảnh gốc** $f$ từ ảnh bị hỏng $g$, sử dụng kiến thức biết trước (a priori) về hàm suy giảm $h$ và nhiễu $\eta$.

### Phương trình suy giảm

| Miền | Công thức |
|------|-----------|
| Không gian | $g(x,y) = (h \star f)(x,y) + \eta(x,y)$ |
| Tần số | $G(u,v) = H(u,v) \cdot F(u,v) + N(u,v)$ |

> 💡 Trong miền tần số, **phép tích chập → phép nhân**, giúp tính toán nhanh hơn.

### Sơ đồ khối

```
f(x,y) → [Degradation H] → (+) ← η(x,y)
                             ↓
                           g(x,y)
                             ↓
                    [Restoration Filter]
                             ↓
                           f̂(x,y)
```

- $f$ = ảnh gốc
- $g$ = ảnh bị suy giảm (input)
- $\hat{f}$ = ảnh xấp xỉ khôi phục (output)
- $h$ = hàm suy giảm (Point Spread Function)
- $\eta$ = nhiễu cộng thêm

---

## 3.2 – Mô hình nhiễu (Noise Models)
> *Slides 4–6*

### 6 loại nhiễu phổ biến

#### 1. Nhiễu Gaussian ⭐ (quan trọng nhất)
$$p(z) = \frac{1}{\sqrt{2\pi}\sigma} e^{-(z-\bar{z})^2 / 2\sigma^2}$$

- $\bar{z}$: giá trị trung bình nhiễu
- $\sigma$: độ lệch chuẩn ($\sigma$ càng lớn → biểu đồ càng bè rộng)
- **Nguồn gốc:** cảm biến ISO cao, chụp thiếu sáng
- **Đặc điểm:** phân phối đối xứng hình chuông

```python
noise = np.random.normal(loc=mean, scale=sigma, size=image.shape)
noisy_img = image + noise
```

#### 2. Nhiễu Rayleigh
$$p(z) = \frac{2(z-a)}{b} e^{-(z-a)^2/b}, \quad z \geq a$$

- **Đặc điểm:** phân phối **lệch** (không đối xứng), có ngưỡng dưới $a$
- **Nguồn gốc:** ảnh radar, siêu âm y tế
- $p(z) = 0$ khi $z < a$

#### 3. Nhiễu Erlang (Gamma)
$$p(z) = \frac{a^b z^{b-1}}{(b-1)!} e^{-az}, \quad z \geq 0$$

- **Nguồn gốc:** ảnh y tế chụp laser, X-Quang

#### 4. Nhiễu Exponential
- Trường hợp đặc biệt của Erlang khi $b=1$

#### 5. Nhiễu Uniform
$$p(z) = \frac{1}{b-a}, \quad a \leq z \leq b$$

- Xác suất phân phối đều trong khoảng $[a, b]$

#### 6. Nhiễu Salt-and-Pepper (Muối tiêu) ⭐
$$p(z) = \begin{cases} P_s & z = 2^k - 1 \text{ (salt - trắng)} \\ P_p & z = 0 \text{ (pepper - đen)} \end{cases}$$

- **Ảnh 8-bit:** muối = 255, tiêu = 0
- **Nguồn gốc:** lỗi cáp, mạch điện tử chập
- **Ví dụ:** $P_s = P_p = 0.1$ → 10% pixel bị lỗi mỗi loại

```python
# Tạo nhiễu muối tiêu
noisy = image.copy()
noisy[np.random.rand(*image.shape) < 0.05] = 255   # Muối
noisy[np.random.rand(*image.shape) < 0.05] = 0     # Tiêu
```

### So sánh tóm tắt

| Loại nhiễu | Đối xứng? | Ứng dụng điển hình | Nhận biết |
|---|---|---|---|
| Gaussian | ✅ Có | Camera, sensor | Hình chuông |
| Rayleigh | ❌ Lệch phải | Siêu âm, radar | Có ngưỡng dưới |
| Erlang | ❌ Lệch | X-Quang | Tham số $a, b$ |
| Uniform | ✅ Phẳng | Lượng tử hóa | Hằng số trên [a,b] |
| Salt-Pepper | N/A | Lỗi điện tử | Chỉ 2 giá trị cực |

---

## 3.3 – Lọc không gian & Tần số
> *Slides 7–12*

### A. Các bộ lọc Mean Filter

#### Arithmetic Mean (Trung bình cộng)
$$\hat{f}(x,y) = \frac{1}{mn} \sum_{(r,c) \in S_{xy}} g(r,c)$$

- Cửa sổ $m \times n$ trượt trên ảnh
- **Ưu:** đơn giản, nhanh
- **Nhược:** làm nhòe cạnh (edges)
- `cv2.blur(img, (3,3))`

#### Geometric Mean (Trung bình nhân)
$$\hat{f}(x,y) = \left[\prod_{(r,c) \in S_{xy}} g(r,c)\right]^{1/mn}$$

- **Ưu:** giữ cạnh tốt hơn Arithmetic
- ⚠️ **Nhược:** nếu **bất kỳ pixel nào = 0** → kết quả = 0 (thảm họa với nhiễu tiêu)

#### Harmonic Mean (Trung bình điều hòa)
$$\hat{f}(x,y) = \frac{mn}{\sum_{(r,c)} \frac{1}{g(r,c)}}$$

- ✅ Tốt với nhiễu Gaussian và nhiễu Muối
- ❌ Thất bại với nhiễu Tiêu (chia cho 0)

#### Contraharmonic Mean ⭐
$$\hat{f}(x,y) = \frac{\sum g(r,c)^{Q+1}}{\sum g(r,c)^Q}$$

| Giá trị Q | Tác dụng |
|---|---|
| $Q > 0$ | Diệt nhiễu **Tiêu** (pepper) |
| $Q < 0$ | Diệt nhiễu **Muối** (salt) |
| $Q = 0$ | = Arithmetic Mean |
| $Q = -1$ | = Harmonic Mean |

### B. Notch Filter (Lọc khía tần số)

**Khi nào dùng:** nhiễu có tính **chu kỳ** (sọc lặp lại, lưới, giao thoa hình sin)

**Nguyên lý:** Nhiễu tuần hoàn → xuất hiện thành các **đốm sáng** cô lập trên phổ Fourier → khoét bỏ đúng các điểm đó.

$$H_{NR}(u,v) = \prod_{k=1}^{Q} H_k(u,v) \cdot H_{-k}(u,v)$$

$$D_k(u,v) = \sqrt{(u - M/2 - u_k)^2 + (v - N/2 - v_k)^2}$$

**Tính đối xứng Fourier:** mỗi điểm nhiễu $(u_k, v_k)$ luôn có điểm song sinh $(-u_k, -v_k)$ → phải khoét cả 2.

```python
# Khoét lỗ tại vị trí nhiễu
spectrum[u_k, v_k] = 0
spectrum[-u_k, -v_k] = 0
F_restored = np.fft.ifft2(np.fft.ifftshift(spectrum))
```

**Quy trình:**
1. FFT2D → phổ Fourier
2. Xác định vị trí đốm sáng nhiễu
3. Nhân mask = 0 tại vị trí đó
4. Inverse FFT2D → ảnh khôi phục

---

## 3.4 – Hàm suy giảm & Ước lượng PSF
> *Slides 13–16*

### Tích chập liên tục (Continuous Convolution)
$$g(x,y) = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} f(\alpha,\beta) \cdot h(x-\alpha, y-\beta) \, d\alpha \, d\beta + \eta(x,y)$$

**Tính chất quan trọng: Position-invariant (Bất biến vị trí)**
- Hàm mờ $h$ không thay đổi theo vị trí trong ảnh
- Vật thể bị nhòe như nhau dù ở góc nào

### 3 Phương pháp ước lượng H

| Phương pháp | Cách làm | Ưu/Nhược |
|---|---|---|
| **Quan sát** | Tự vẽ lại vùng nét, chia G_s/F̂_s | Chủ quan, phụ thuộc người dùng |
| **Thực nghiệm** | Chụp impulse sáng, G/A | Khách quan, cần thiết bị chuẩn |
| **Mô hình toán** | Dùng công thức vật lý | Chính xác nhưng cần biết môi trường |

**Thực nghiệm (Impulse):**
$$\hat{H}(u,v) = \frac{G(u,v)}{A}$$

**Mô hình nhiễu khí quyển (Atmospheric turbulence):**
$$H_s(u,v) = e^{-k(u^2+v^2)^{5/6}}$$
- $k$ càng lớn → không khí bốc hơi mạnh → ảnh càng mờ

### Blind Deconvolution
- **Định nghĩa:** Không biết $H$, phải tự suy ngược từ ảnh bị hỏng
- **Cực kỳ khó** – bài toán ill-posed
- Tương đương Unsupervised Learning / Zero-shot

---

## 3.5 – Wavelet Denoising
> *Slides 17–18*

### Nguyên lý Discrete Wavelet Transform (DWT)

```
x(n) ──┬── [h₀ Low-pass]  ──↓2── LL (xấp xỉ thô)
       └── [h₁ High-pass] ──↓2── LH, HL, HH (chi tiết cạnh + nhiễu)
```

- ↓2 = Giảm mẫu (downsampling) → giảm kích thước xuống một nửa
- Cấu trúc cây nhiều tầng = phân giải đa cấp (multiresolution)

### 3 Bước Wavelet Denoising

```
Ảnh gốc g
    ↓
[1] DWT Decompose → Hệ số Wavelet W
    ↓
[2] Thresholding → W' (cắt bỏ nhiễu)
    ↓
[3] Inverse DWT → f̂ (ảnh khôi phục)
```

### Hai kiểu Thresholding

#### Hard Thresholding
$$w' = \begin{cases} w & |w| \geq T \\ 0 & |w| < T \end{cases}$$

- Giữ nguyên hoặc xóa hẳn → hàm bước nhảy (discontinuous)

#### Soft Thresholding ⭐
$$w' = \begin{cases} \text{sign}(w)(|w| - T) & |w| \geq T \\ 0 & |w| < T \end{cases}$$

- Gọt bớt $T$ từ giá trị lớn → hàm **trơn liên tục**
- Tạo **sparsity** (thưa thớt) tương tự L1/Lasso

| | Hard | Soft |
|---|---|---|
| Giá trị lớn hơn T | Giữ nguyên | Gọt bớt T |
| Tính liên tục | Không | Có |
| Tương đương AI | Step function | ReLU + L1 |

---

## 3.6 – Bộ lọc Wiener (MMSE)
> *Slides 19–21*

### Mục tiêu
Tìm $\hat{f}$ để **tối thiểu hóa Mean Square Error:**
$$e^2 = \mathbb{E}\{(f - \hat{f})^2\}$$

### Công thức Wiener Filter ⭐

$$\hat{F}(u,v) = \underbrace{\frac{1}{H(u,v)}}_{\text{Inverse filter}} \cdot \underbrace{\frac{|H(u,v)|^2}{|H(u,v)|^2 + S_\eta(u,v)/S_f(u,v)}}_{\text{Cục phanh an toàn}} \cdot G(u,v)$$

**Ký hiệu:**
- $S_\eta(u,v)$ = phổ năng lượng nhiễu
- $S_f(u,v)$ = phổ năng lượng ảnh gốc
- $S_\eta/S_f$ = Noise-to-Signal Ratio (NSR)

**Hai trường hợp biên:**

| Điều kiện | Cục phanh | Kết quả |
|---|---|---|
| $S_\eta = 0$ (không nhiễu) | = 1 | = Inverse filter $G/H$ |
| $S_\eta \to \infty$ (nhiễu lớn) | → 0 | Tắt hoàn toàn, tránh nổ tung |

### Đo lường hiệu năng

$$\text{SNR} = \frac{\sum_u \sum_v |F(u,v)|^2}{\sum_u \sum_v |N(u,v)|^2} \quad \uparrow \text{ càng cao càng tốt}$$

$$\text{MSE} = \frac{1}{MN} \sum_x \sum_y [f(x,y) - \hat{f}(x,y)]^2 \quad \downarrow \text{ càng nhỏ càng tốt}$$

```python
mse = np.mean((f - f_hat)**2)
psnr = 10 * np.log10(255**2 / mse)
```

### Yếu điểm của Wiener
⚠️ Cần biết $S_f$ (phổ năng lượng ảnh **gốc**) — nhưng ảnh gốc đang bị mất!

---

## 3.7 – Lọc CLS (Constrained Least Squares)
> *Slides 22–24*

### Động lực
Giải quyết yếu điểm của Wiener: **không cần biết ảnh gốc**, chỉ cần thông tin về nhiễu.

### Bài toán tối ưu

**Minimize:**
$$C = \sum_x \sum_y [\nabla^2 f(x,y)]^2 \quad \leftarrow \text{ép ảnh mượt tối đa}$$

**Subject to:**
$$\|g - H\hat{f}\|^2 = \|\eta\|^2 \quad \leftarrow \text{giữ trung thực với dữ liệu}$$

> $\nabla^2 f$ = Laplacian = đo độ **gập ghềnh** của ảnh. Minimize $C$ = bắt ảnh phải phẳng mịn.

### Lời giải miền tần số ⭐

$$\hat{F}(u,v) = \left[\frac{H^*(u,v)}{|H(u,v)|^2 + \gamma |P(u,v)|^2}\right] G(u,v)$$

**Ma trận Laplacian** $p$ (3×3):
$$p = \begin{bmatrix} 0 & -1 & 0 \\ -1 & 4 & -1 \\ 0 & -1 & 0 \end{bmatrix}$$

**Tham số $\gamma$:**

| $\gamma$ lớn | $\gamma$ nhỏ |
|---|---|
| Ảnh mượt mà, bằng phẳng | Ảnh sắc nét nhưng nhiều nhiễu |
| Oversmoothing | Underfitting |

### So sánh Wiener vs CLS

| Tiêu chí | Wiener | CLS |
|---|---|---|
| Cần $S_f$ | ✅ Có | ❌ Không |
| Điều chỉnh | Tự động (SNR) | Thủ công ($\gamma$) |
| Tối ưu hóa | MSE thống kê | Laplacian mượt |
| Tương đương AI | Bayesian Optimal | Tikhonov / L2 Reg |

---

## 3.9 – Tái tạo từ hình chiếu (CT Scan)
> *Slides 25–27*

### Bài toán
Từ các **1D profile** (bóng tia X) thu được từ nhiều góc → dựng lại **cấu trúc 2D/3D** bên trong.

### Nguyên lý Back-Projection

```
Góc 1:  /  vệt sáng 1
Góc 2:  |  vệt sáng 2   →  giao điểm = vật thể
Góc 3:  \  vệt sáng 3
...
Góc N:  32+ vệt đan nhau → vật thể hiện rõ
```

- 1 góc: vệt mờ dọc
- 2 góc: giao điểm sáng lên
- **32+ góc:** vật thể hiện ra rõ nét

### Ứng dụng CT Scan y tế
- Máy quay vòng quanh bệnh nhân, chụp từng **lát cắt mỏng** (slice)
- Ráp hàng ngàn lát → **mô hình 3D** bộ tạng
- CT = **Computed** Tomography (cần máy tính xử lý)

**Xử lý AI:**
- Ảnh 2D đơn: `Conv2D`
- Chuỗi lát cắt CT: `Conv3D` hoặc `ViT-3D`

---

## 3.10 – Ảnh đa kênh (Multichannel)
> *Slides 28–29*

### Các loại ảnh đa kênh
- Ảnh màu: **3 kênh** RGB
- Ảnh vệ tinh: **12+ dải** quang phổ
- Ảnh y tế: nhiều pha chụp (T1, T2, FLAIR...)

### Ý tưởng: Khai thác tương quan giữa các kênh
> Kênh Đỏ và kênh Xanh có **tương quan hình học** → mượn chi tiết kênh này bù vào kênh kia bị mất.

### Hai phương pháp

#### LMMSE (Linear Minimum MSE)
$$f_{LMMSE} = C_f H^T (H C_f H^T + C_\eta)^{-1} g$$

- Mở rộng Wiener sang đa kênh
- $C_f, C_\eta$: ma trận Hiệp phương sai (Covariance)

#### RWLS (Regularized Weighted Least Squares)
$$f_{RWLS} = (H^T C_\eta^{-1} H + \lambda Q^T Q)^{-1} H^T C_\eta^{-1} g$$

- Gắn thêm trọng số phạt $\lambda$
- $\lambda$ lớn → ép các kênh đồng bộ mượt hơn

**Nút thắt tính toán:** Nghịch đảo ma trận $(\cdot)^{-1}$ có độ phức tạp $O(N^2)$ → dùng optimizer bậc 1 (Adam/SGD) thay thế trong AI.

---

## 3.11–3.12 – Phát hiện chuyển động & Phục hồi video
> *Slides 30–32*

### Motion Detection (Phát hiện chuyển động)

**Phương pháp cơ bản:**
$$\text{difference}(x,y) = |f(x,y,t) - f(x,y,t-1)|$$

**Thách thức:**
- Thay đổi ánh sáng → báo động giả
- Cây cối rung → nhiễu động

### Temporal Motion Model

$$x(\tau) = x(t) + v_t(x) \cdot (\tau - t)$$

- $x(t)$: vị trí hiện tại
- $v_t$: vận tốc
- Nếu có gia tốc $a$: cần thêm tham số → $x(\tau) = x(t) + v\Delta t + \frac{1}{2}a(\Delta t)^2$

**Ứng dụng:** Nén video MPEG – chỉ lưu **vector vận tốc** thay vì toàn bộ frame.

### Pipeline Phục hồi Video

```
Video cũ bị hỏng
      ↓
[Flicker Correction]  ← sửa nhấp nháy đèn
      ↓
[Motion Estimation]   ← tìm vector chuyển động
      ↓
[Noise Reduction]     ← khử nhiễu không gian
      ↓
[Blotch Removal]      ← xóa đốm xước bẩn
      ↓
Video phục hồi ✅
```

**Tại sao phải tự động?** Video có hàng ngàn frame → không thể làm thủ công từng frame.

---

## 🔑 Công thức cốt lõi cần thuộc

| Tên | Công thức | Ghi chú |
|---|---|---|
| Mô hình suy giảm | $g = h \star f + \eta$ | Nền tảng cả chương |
| Miền tần số | $G = H \cdot F + N$ | Chập → nhân |
| Gaussian PDF | $p(z) = \frac{1}{\sqrt{2\pi}\sigma}e^{-(z-\bar{z})^2/2\sigma^2}$ | Nhiễu phổ biến nhất |
| Arithmetic Mean | $\hat{f} = \frac{1}{mn}\sum g$ | = AveragePooling |
| Contraharmonic | $\hat{f} = \frac{\sum g^{Q+1}}{\sum g^Q}$ | Q>0 diệt tiêu, Q<0 diệt muối |
| Wiener Filter | $\hat{F} = \frac{H^*}{|H|^2 + S_\eta/S_f} \cdot G$ | Tối ưu MSE |
| CLS Filter | $\hat{F} = \frac{H^*}{|H|^2 + \gamma|P|^2} \cdot G$ | Không cần ảnh gốc |
| MSE | $\frac{1}{MN}\sum(f-\hat{f})^2$ | ↓ nhỏ = tốt |
| SNR | $\frac{\sum\|F\|^2}{\sum\|N\|^2}$ | ↑ lớn = tốt |
| Atmospheric model | $H_s = e^{-k(u^2+v^2)^{5/6}}$ | $k$ lớn → mờ nhiều |
| Motion model | $x(\tau) = x(t) + v\Delta t$ | Cơ sở nén MPEG |

---

## 🤖 Kết nối AI / Deep Learning

| Khái niệm xử lý ảnh | Tương đương trong AI |
|---|---|
| Phương trình $g = h \star f$ | Forward pass của `nn.Conv2D` |
| Sơ đồ Degradation → Restoration | Kiến trúc **AutoEncoder** |
| Gaussian noise forward | **Diffusion Models** (Stable Diffusion) |
| Arithmetic Mean Filter | **AveragePooling2D** |
| Notch filter (khoét điểm = 0) | **Dropout** |
| Soft Thresholding Wavelet | **ReLU + L1 Lasso** |
| DWT ↓2 multiresolution | **U-Net Pooling / FPN** |
| Hàm MSE Loss Wiener | **MSE/L2 Loss** |
| Tham số $\gamma$ CLS | **λ regularization strength** |
| CLS Laplacian ràng buộc | **Tikhonov / L2 Weight Decay** |
| Back-projection Radon | **NeRF** (Neural Radiance Fields) |
| 3D CT reconstruction | **Conv3D / ViT-3D** |
| Motion vector prediction | **RNN / LSTM / Kalman Filter** |
| Video restoration pipeline | **GAN** (Generator + Discriminator) |
| Translation invariance | Triết lý thiết kế **CNN** (LeCun) |
| Blind deconvolution | **Unsupervised / Zero-shot Learning** |
| Mô hình vật lý $H_s$ | **Physics-Informed Neural Networks** |

---

## ❓ Câu hỏi ôn tập

### Mức độ cơ bản (Nhớ)

1. Sự khác biệt giữa **Restoration** và **Enhancement** là gì?
2. Trong nhiễu muối tiêu ảnh 8-bit, giá trị "muối" bằng bao nhiêu?
3. SNR càng cao thì chất lượng ảnh càng tốt hay tệ?
4. Chữ "C" trong CT Scan có nghĩa là gì?
5. Ký hiệu $\hat{f}$ trong toán học có ý nghĩa gì?

### Mức độ trung bình (Hiểu)

6. Tại sao Geometric Mean Filter lại thất bại hoàn toàn với nhiễu hạt tiêu?
7. Bộ lọc Notch cắt dải rộng hay khoét bỏ điểm tần số cụ thể?
8. Tại sao mỗi Notch filter phải đi theo cặp $(H_k, H_{-k})$?
9. Kỹ thuật phân ngưỡng nào (Soft hay Hard) làm giảm cả giá trị đặc trưng cốt lõi?
10. Bộ lọc Wiener thoái hóa thành bộ lọc nào khi $S_\eta = 0$?

### Mức độ cao (Vận dụng)

11. Nếu ảnh chỉ toàn nhiễu hạt tiêu, chọn $Q$ dương hay âm cho Contraharmonic?
12. Tham số $k$ trong mô hình khí quyển càng lớn → ảnh rõ hay mờ hơn?
13. Nếu tăng $\gamma$ quá lớn trong CLS → ảnh sắc nét hay bị mờ?
14. Khi số góc back-projection tăng từ 1 → 32 → vật thể hiện ra như thế nào?
15. Hệ thống camera bị nhòe nhiều ở rìa ảnh có tính "position-invariant" không?

### Đáp án tóm tắt

> 1. Restoration dùng toán học khách quan (có mô hình), Enhancement làm đẹp theo mắt người
> 2. 255 (giá trị max ảnh 8-bit)
> 3. Càng tốt (SNR ↑)
> 4. Computed (cần máy tính xử lý)
> 5. Ước lượng / giá trị xấp xỉ
> 6. Tích có 1 pixel = 0 → cả cửa sổ = 0
> 7. Khoét bỏ điểm cụ thể
> 8. Phổ Fourier có tính đối xứng tâm
> 9. Soft thresholding (gọt bớt T từ giá trị lớn)
> 10. Inverse filter (G/H)
> 11. Q dương (loại bỏ giá trị nhỏ - pepper)
> 12. Mờ hơn (k lớn → nhiễu động khí quyển mạnh)
> 13. Bị làm mờ (oversmoothing)
> 14. Hiện ra rõ dần, sắc nét hơn
> 15. Không (position-invariant yêu cầu nhòe đều khắp nơi)

---

*Đề cương được tổng hợp từ 32 slides · Chương 3 · Xử lý ảnh số*
