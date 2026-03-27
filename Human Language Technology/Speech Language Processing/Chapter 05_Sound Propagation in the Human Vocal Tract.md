---
tags:
  - speech-processing
  - vocal-tract
  - acoustics
  - chapter-5
aliases:
  - Sound Propagation Vocal Tract
  - Truyền Âm Trong Vocal Tract
date: 2026-03-24
status: complete
---

# Chapter 5 — Sound Propagation in the Human Vocal Tract

> [!abstract] Tóm tắt chương
> Chương này nghiên cứu cơ chế vật lý của việc âm thanh truyền qua vocal tract — từ mô hình ống âm học, lý thuyết sóng âm, đến cách vocal tract hoạt động như một bộ lọc tạo ra formants. Đây là nền tảng vật lý giải thích tại sao LPC hoạt động được.

---

## Bản đồ nội dung

```
Sound Propagation in the Human Vocal Tract
├── 1. Vocal Tract như một Acoustic Tube
│   ├── Cấu trúc giải phẫu
│   └── Mô hình ống hình trụ
├── 2. Lý Thuyết Sóng Âm trong Ống
│   ├── Wave equation
│   ├── Sóng tới và sóng phản xạ
│   └── Boundary conditions
├── 3. Tần Số Cộng Hưởng (Formants)
│   ├── Tại sao có formants?
│   └── Formants thay đổi theo khẩu hình
├── 4. Lossless Tube Model
│   ├── Chuỗi ống hình trụ
│   ├── Reflection coefficients
│   └── Liên hệ với LPC
└── 5. Radiation và Lip Effects
```

---

## 1. Vocal Tract Như Một Acoustic Tube

### 1.1 Cấu Trúc Giải Phẫu

**Vocal tract** là khoang khí từ glottis (thanh môn) đến môi, dài khoảng **17 cm** ở người trưởng thành nam. Nó bao gồm:

```
Glottis (Thanh môn)
    │  Nguồn kích thích (excitation)
    ▼
[Pharynx — Họng hầu]   ~7 cm
    │
    ▼
[Oral Cavity — Khoang miệng]  ~10 cm
    │  ← Lưỡi, Hàm, Môi điều chỉnh hình dạng
    ▼
[Lips — Môi]           → Đầu ra (radiation)
```

**Khoang mũi** cũng có thể kết nối vào qua velum → tạo ra nasal sounds (/m/, /n/, /ŋ/).

### 1.2 Mô Hình Ống Hình Trụ

Vocal tract được xấp xỉ bằng **chuỗi các ống hình trụ nối tiếp nhau**, mỗi ống có tiết diện khác nhau:

```
[A₁] [A₂] [A₃] [A₄] ... [Aₙ]
  ←── Độ dài mỗi đoạn: Δx ───→
```

- $A_k$: tiết diện (cross-sectional area) của đoạn thứ $k$
- Khi khẩu hình miệng thay đổi → các $A_k$ thay đổi → formants thay đổi

---

## 2. Lý Thuyết Sóng Âm Trong Ống

### 2.1 Wave Equation (Phương Trình Sóng)

Áp suất âm $p(x, t)$ trong ống đồng nhất thỏa mãn:

$$\frac{\partial^2 p}{\partial x^2} = \frac{1}{c^2} \frac{\partial^2 p}{\partial t^2}$$

với $c \approx 340$ m/s là tốc độ âm thanh trong không khí.

### 2.2 Sóng Tới và Sóng Phản Xạ

**Nghiệm tổng quát** là tổ hợp sóng tới (forward) và sóng phản xạ (backward):

$$p(x, t) = p^+(t - x/c) + p^-(t + x/c)$$

- $p^+$: sóng truyền **về phía môi** (từ glottis đến lips)
- $p^-$: sóng **phản xạ ngược lại** (từ lips về glottis)

### 2.3 Boundary Conditions

| Vị trí | Điều kiện | Ý nghĩa |
|--------|-----------|---------|
| **Glottis** (đóng) | Vận tốc = 0 | Đầu đóng — phản xạ hoàn toàn |
| **Lips** (mở) | Áp suất = 0 | Đầu mở — phản xạ với đổi dấu |
| **Nối ống** (diện tích thay đổi) | Liên tục áp suất & lưu lượng | Phản xạ một phần tại nối |

---

## 3. Tần Số Cộng Hưởng — Formants

### 3.1 Tại Sao Có Formants?

**Formants** xuất hiện do **cộng hưởng âm học** (acoustic resonance) của vocal tract:

Với ống đồng nhất dài $L$, **đầu đóng — đầu mở**:

$$F_n = \frac{(2n-1) \cdot c}{4L}, \quad n = 1, 2, 3, \ldots$$

Ví dụ: $L = 17$ cm, $c = 340$ m/s:
- $F_1 = 500$ Hz
- $F_2 = 1500$ Hz
- $F_3 = 2500$ Hz

> [!info] Tại sao formants là nền tảng của LPC?
> LPC mô hình hóa vocal tract như bộ lọc all-pole $H(z) = G/A(z)$. Các **poles** của $H(z)$ chính xác là các **formant frequencies** — đây là lý do LPC có thể ước lượng formants.

### 3.2 Formants Thay Đổi Theo Khẩu Hình

Khi lưỡi và môi thay đổi → tiết diện ống thay đổi → formants thay đổi:

| Nguyên âm | F1 (Hz) | F2 (Hz) | Khẩu hình |
|-----------|---------|---------|----------|
| /i/ ("see") | ~270 | ~2300 | Lưỡi cao, môi hẹp |
| /a/ ("father") | ~730 | ~1090 | Lưỡi thấp, miệng mở |
| /u/ ("boot") | ~300 | ~870 | Lưỡi cao-sau, môi tròn |

---

## 4. Lossless Tube Model

### 4.1 Chuỗi Ống Lossless

**Lossless Tube Model** xấp xỉ vocal tract bằng $M$ đoạn ống đồng nhất ghép nối:

```
Glottis                                    Lips
   │                                          │
[Tube 1]──[Tube 2]──[Tube 3]── ... ──[Tube M]──→
  A₁        A₂        A₃              Aₘ

"Lossless" = không mất năng lượng trong ống
             chỉ phản xạ tại các nối
```

### 4.2 Reflection Coefficients (Hệ Số Phản Xạ)

Tại mỗi nối giữa ống $m$ và $m+1$, có **hệ số phản xạ**:

$$k_m = \frac{A_m - A_{m+1}}{A_m + A_{m+1}}$$

- $k_m > 0$: tiết diện giảm → phản xạ thuận chiều
- $k_m < 0$: tiết diện tăng → phản xạ ngược chiều
- $|k_m| < 1$ với mọi $m$ → hệ thống **ổn định**

### 4.3 Liên Hệ Với LPC

| Lossless Tube Model | LPC |
|--------------------|-----|
| Reflection coefficients $k_m$ | PARCOR coefficients (từ Levinson-Durbin) |
| Tiết diện $A_m$ | Hàm diện tích vocal tract |
| Tần số cộng hưởng ống | Poles của $H(z)$ → Formants |
| $M$ đoạn ống | Bậc $p$ của LPC |

> [!important] Điều kiện ổn định
> $|k_m| < 1$ với mọi $m$ ↔ tất cả poles của LPC nằm trong vòng tròn đơn vị ↔ mô hình ổn định (stable).

---

## 5. Radiation và Lip Effects

### 5.1 Radiation Impedance

Tại môi, âm thanh "thoát ra" không gian mở → **radiation impedance** khác không. Hiệu ứng này:
- Tăng cường tần số cao (như bộ lọc high-pass)
- **Pre-emphasis filter** trong speech processing ($s'[n] = s[n] - \alpha s[n-1]$, $\alpha \approx 0.97$) mô phỏng và bù trừ hiệu ứng này

### 5.2 Nasal Coupling

Khi velum hạ xuống → khoang mũi kết nối:
- Tạo ra **zeros** (điểm không) trong transfer function
- Giải thích tại sao nasal sounds (/m/, /n/) có spectral "dips"
- Đây là lý do mô hình LPC đôi khi cần thêm zeros để mô tả chính xác nasal sounds

---

## Tóm Tắt

```
Vocal Tract
    │ Ống dài ~17cm, tiết diện thay đổi
    │
    ▼ Lossless Tube Model (M đoạn)
Reflection coefficients kₘ = (Aₘ - Aₘ₊₁)/(Aₘ + Aₘ₊₁)
    │
    ▼ ↔ LPC
PARCOR coefficients → All-pole filter H(z) = G/A(z)
    │
    ▼
Poles của H(z) = Formants (F₁, F₂, F₃)
    │
    ▼
Phân biệt các nguyên âm và phụ âm
```

| Khái niệm | Ý nghĩa vật lý | Tương đương trong LPC |
|-----------|---------------|----------------------|
| **Formants** | Tần số cộng hưởng của ống | Poles của H(z) |
| **Reflection coeff.** | Phản xạ tại nối ống | PARCOR coefficients |
| **Lossless** | Không mất năng lượng trong ống | Poles trong unit circle |
| **Pre-emphasis** | Bù radiation effect | Filter $1 - \alpha z^{-1}$ |

---

## Liên Kết

- [[Chapter 3]] — Fundamentals of Human Speech Production
- [[Chapter 4]] — Hearing, Auditory Models & Speech Perception
- [[Chapter 9]] — Linear Predictive Analysis (LPC, Poles, Reflection Coefficients)
- [[Chapter 6]] — Time-Domain Methods
- [[Formants]]
- [[LPC]]

---

*Chapter 5 · Sound Propagation in the Human Vocal Tract · Rabiner & Schafer · Tự học*
