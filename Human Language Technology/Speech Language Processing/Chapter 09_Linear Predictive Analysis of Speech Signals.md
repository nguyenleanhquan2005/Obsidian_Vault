---
tags:
  - speech-processing
  - LPC
  - linear-prediction
  - chapter-9
aliases:
  - Linear Predictive Analysis
  - LPA
  - LPC
date: 2026-03-24
status: complete
---

# Chapter 9 — Linear Predictive Analysis of Speech Signals

> [!abstract] Tóm tắt chương
> LPA (Linear Predictive Analysis) là một trong những kỹ thuật quan trọng nhất trong xử lý tiếng nói — mô hình hóa vocal tract như một bộ lọc all-pole, từ đó nén và phân tích tiếng nói hiệu quả. Chương này đi qua nguyên lý cơ bản, tính toán gain, diễn giải miền tần số, tín hiệu lỗi dự đoán, và mối liên hệ với mô hình ống âm học.

---

## Bản đồ nội dung

```
Linear Predictive Analysis of Speech Signals
├── 1. Nguyên lý cơ bản (Basic Principles)
│   ├── Tại sao dùng LPA?
│   ├── Công thức dự đoán tuyến tính
│   ├── All-pole model
│   └── Autocorrelation & Levinson-Durbin ★
├── 2. Tính toán Gain của mô hình
│   └── Ý nghĩa của Gain
├── 3. Diễn giải miền tần số
│   ├── Poles → Formants
│   └── LPC Spectrum
├── 4. Tín hiệu lỗi dự đoán (Prediction Error Signal)
│   └── Glottal excitation
└── 5. Liên hệ với Lossless Tube Models
    ├── Acoustic tube model
    └── LPA ↔ Reflection coefficients
```

---

## 1. Nguyên Lý Cơ Bản (Basic Principles)

### 1.1 Tại Sao Dùng LPA?

**Linear Predictive Analysis** được dùng rộng rãi trong speech processing vì:

- Cung cấp **biểu diễn compact** (compact representation) của đặc tính vocal tract
- Ứng dụng trong **speech synthesis, coding, và recognition**
- Mô hình hóa chính xác cách vocal tract hoạt động như một **bộ lọc cộng hưởng**

### 1.2 Công Thức Dự Đoán Tuyến Tính

**Ý tưởng cốt lõi:** Mẫu tiếng nói hiện tại có thể được **dự đoán** từ các mẫu trong quá khứ:

$$\hat{s}[n] = \sum_{k=1}^{p} a_k \cdot s[n-k]$$

- $\hat{s}[n]$: giá trị **dự đoán** của mẫu thứ $n$
- $a_k$: **hệ số dự đoán** (prediction coefficients) — cần tìm
- $p$: **bậc** của mô hình (thường là 10–16 cho tiếng nói)
- $s[n-k]$: các mẫu trong **quá khứ**

### 1.3 LPC — "Bắt Chước" Cổ Họng Con Người

> LPC coi **cổ họng con người như một ống lọc IIR**, còn thanh quản là nguồn phát âm. Gọi điện Zalo/Messenger tốn chỉ ~8–10 kbps mà vẫn nghe rõ — đó là nhờ LPC không truyền file WAV, mà chỉ truyền bộ hệ số mô phỏng cổ họng + pitch + gain!

### 1.4 All-Pole Model của Vocal Tract

LPA mô hình hóa vocal tract như một **bộ lọc all-pole** (chỉ có cực, không có zero):

$$H(z) = \frac{G}{1 - \sum_{k=1}^{p} a_k z^{-k}} = \frac{G}{A(z)}$$

```
Excitation (Kích thích)          Vocal Tract Filter
  ┌─────────────┐                  ┌─────────────┐
  │  Glottal    │   e[n]           │  All-pole   │   s[n]
  │  source     │ ──────────────→  │  filter     │ ──────→
  │  (buzz/hiss)│                  │  H(z)=G/A(z)│
  └─────────────┘                  └─────────────┘
```

> [!info] Tại sao all-pole?
> Vocal tract là một ống cộng hưởng → chủ yếu có **poles** (cộng hưởng = formants), ít zeros. All-pole model đơn giản nhưng đủ chính xác cho hầu hết tiếng nói.

### 1.4 Tìm Hệ Số: Autocorrelation & Levinson-Durbin

**Mục tiêu:** Tối thiểu hóa năng lượng lỗi dự đoán:

$$E = \sum_{n} \left(s[n] - \hat{s}[n]\right)^2 = \sum_{n} e[n]^2$$

**Giải pháp:** Lập phương trình **Yule-Walker** dùng hàm autocorrelation $R[k]$:

$$\sum_{k=1}^{p} a_k R[i-k] = R[i], \quad i = 1, 2, \ldots, p$$

**Levinson-Durbin Algorithm** giải hệ phương trình này một cách đệ quy — hiệu quả $O(p^2)$ thay vì $O(p^3)$ nếu dùng Gaussian elimination thông thường.

> [!tip] Tóm tắt LPA
> LPA là thiết yếu để mô hình hóa tiếng nói bằng cách dự đoán mẫu tương lai từ quá khứ. Levinson-Durbin tính hệ số dự đoán hiệu quả từ autocorrelation.

### 1.5 Điểm Cực (Poles) và Điểm Không (Zeros)

Khi giải Z-transform của hệ thống LPC:

| | Ý nghĩa vật lý | Ảnh hưởng |
|-|---------------|----------|
| **Poles (Điểm cực)** | Tần số cộng hưởng của khoang miệng → **Formants** | Khuếch đại dải âm đó |
| **Zeros (Điểm không)** | Rãnh khuyết tần số (Notches) | Xảy ra khi khoang mũi hấp thụ năng lượng |

> [!tip] Ứng dụng thực tiễn
> LPC được dùng rộng rãi nhất để **ước lượng Formant (Q80)**: vì nó vẽ đường bao phổ (spectral envelope) cực mượt qua phổ tiếng nói → xác định đỉnh = Formants.

### 1.6 Bậc của Mô Hình LPC (LPC Order $p$)

**Tăng $p$ → cải thiện độ chính xác** — nhiều hệ số $\alpha_k$ hơn → bám sát phổ thực tế hơn.

> [!warning] Overfitting khi $p$ quá lớn
> Nếu $p$ quá lớn (ví dụ $p=100$), mô hình sẽ **overfitting** — học luôn cả phổ nhiễu và cấu trúc sóng hài pitch, làm mất đường bao vocal tract envelope cần thiết.
>
> **Quy tắc thực tế:** $p \approx 2 \cdot F_s / 1000 + 2$ (ví dụ: $F_s = 8\text{ kHz}$ → $p = 18$)

---

## 2. Tính Toán Gain Của Mô Hình

### 2.1 Gain Là Gì?

**Gain** $G$ là hệ số khuếch đại của mô hình — đại diện cho **năng lượng của tín hiệu kích thích** (excitation):

$$G^2 = R[0] - \sum_{k=1}^{p} a_k R[k]$$

- $R[0]$: năng lượng toàn phần của tín hiệu
- $\sum a_k R[k]$: phần năng lượng được "giải thích" bởi mô hình dự đoán

### 2.2 Ý Nghĩa Vật Lý

| Gain lớn | Gain nhỏ |
|----------|----------|
| Mô hình dự đoán kém | Mô hình dự đoán tốt |
| Nhiều "bất ngờ" trong tín hiệu | Tín hiệu predictable |
| Âm hữu thanh với nhiều năng lượng | Tín hiệu đã được mô hình hóa tốt |

### 2.3 Các Bước Tính Gain

1. Tính autocorrelation $R[k]$ của tín hiệu tiếng nói
2. Giải Levinson-Durbin → thu được $a_k$
3. Tính $G^2 = R[0] - \sum_{k=1}^{p} a_k R[k]$
4. $G = \sqrt{G^2}$

### 2.3 Vai Trò Chi Tiết Của Gain $G$

**Công thức synthesis đầy đủ:**
$$s[n] = \sum_{k=1}^p \alpha_k s[n-k] + G \cdot u[n]$$

- Các hệ số $\alpha_k$ → tạo hình **bộ lọc Formant** (khẩu hình miệng)
- $u[n]$ → nguồn kích thích chuẩn hóa (xung hoặc nhiễu trắng)
- **$G$ → điều chỉnh biên độ** để năng lượng giọng tổng hợp = giọng gốc

> Không có $G$: loa phát tiếng quá nhỏ hoặc clipping (rè do quá tải).

### 2.4 Phương Pháp Bình Phương Tối Thiểu (Least Squares)

Để tìm bộ hệ số $\alpha_k$ tối ưu, ta tối thiểu hóa MSE:

$$E_{\hat{n}} = \sum_{m} e^2[m] = \sum_{m} \left( s[m] - \sum_{k=1}^{p} \alpha_k s[m-k] \right)^2$$

**Điều kiện tối ưu:** $\dfrac{\partial E_{\hat{n}}}{\partial \alpha_k} = 0$ với mọi $k$ → giải hệ phương trình tuyến tính → thu được $\alpha_k$ phản ánh chính xác cấu trúc vocal tract.

---

## 3. Diễn Giải Miền Tần Số

### 3.1 LPC Spectrum

Biến đổi $H(z)$ lên vòng tròn đơn vị ($z = e^{j\omega}$):

$$H(e^{j\omega}) = \frac{G}{1 - \sum_{k=1}^{p} a_k e^{-j\omega k}}$$

**LPC Spectrum** = $|H(e^{j\omega})|^2$ — là **envelope** (bao phổ) của phổ tiếng nói.

### 3.2 Poles → Formants

**Các cực (poles)** của $H(z)$ nằm gần vòng tròn đơn vị → tạo ra các đỉnh trong LPC spectrum → đây chính là **Formants**!

```
LPC Spectrum |H(ω)|²
     ↑
     │    F1        F2        F3
     │   /\        /\        /\
     │  /  \      /  \      /  \
     │ /    \    /    \    /    \
     └──────────────────────────→ ω
        (Tần số)
```

> [!example] Ứng dụng
> Siri và các hệ thống ASR trích xuất **Formants từ poles của LPC** để nhận dạng nguyên âm — đây là cơ chế phân biệt "Cat" vs "Cut".

### 3.3 Components of Frequency Domain Analysis

| Thành phần | Ý nghĩa |
|-----------|---------|
| **Poles gần vòng tròn đơn vị** | Cộng hưởng mạnh → Formant rõ |
| **Poles xa vòng tròn đơn vị** | Cộng hưởng yếu → Formant mờ |
| **Bậc p cao** | Mô hình chi tiết hơn, bắt được nhiều formant |
| **Bậc p thấp** | Mô hình mượt hơn, chỉ bắt formant chính |

**2. Cốt lõi của mô hình LPC** LPC coi cổ họng con người như một ống lọc bằng nhựa (IIR filter), còn thanh quản là nguồn phát âm.

- **Công thức Tổng quát LPC Bắt buộc:** $$s[n] = \sum_{k=1}^{p} \alpha_k s[n-k] + G u[n]$$ _(Ý nghĩa: Mẫu âm thanh hiện tại $s[n]$ có thể được **dự đoán tuyến tính** bằng tổng của $p$ mẫu trong quá khứ $s[n-k]$ nhân với hệ số $\alpha_k$. Còn $G u[n]$ là nguồn kích thích (excitation) từ thanh quản)._
- **Tham số Gain ($G$) (Câu 3):** Quyết định trực tiếp đến **biên độ (amplitude)** của tín hiệu trong miền thời gian. Giọng bạn nói to hay nhỏ được quyết định bởi tham số $G$ này.

**3. Điểm Cực (Poles) và Điểm Không (Zeros) (Câu 17)**

- **Trực quan vật lý:** Khi giải phương trình Z-transform của hệ thống LPC, ta có các Poles và Zeros.
    - **Poles (Điểm cực):** Đại diện cho các tần số cộng hưởng của khoang miệng (Formants). Nó làm khuếch đại một dải âm thanh.
    - **Zeros (Điểm không):** Đại diện cho các rãnh khuyết tần số (Notches), ví dụ khi luồng khí bị khoang mũi hấp thụ bớt năng lượng.



**4. Bậc của mô hình LPC (LPC Order $p$ - Câu 25)**

- **Tại sao đáp án đúng?** Việc tăng bậc $p$ (ví dụ từ 10 lên 12 hoặc 16) cung cấp cho phương trình nhiều hệ số $\alpha_k$ hơn, từ đó bám sát phổ âm thanh thực tế hơn, giúp **cải thiện độ chính xác của biểu diễn tín hiệu (Improved accuracy)**.
- **Lỗi sai phổ biến:** Sinh viên nghĩ rằng tăng $p$ lên vô hạn (ví dụ $p=100$) là tốt nhất. Không! Nếu $p$ quá lớn, mô hình sẽ bị "Overfitting" – nó học luôn cả phổ nhiễu hoặc cấu trúc sóng hài của pitch, làm mất đi hình dáng đường bao phổ (vocal tract envelope) cần thiết.

---

## 4. Tín Hiệu Lỗi Dự Đoán (Prediction Error Signal)

### 4.1 Định Nghĩa

**Prediction error** (hay **residual**) là phần tín hiệu mà mô hình **không dự đoán được**:

$$e[n] = s[n] - \hat{s}[n] = s[n] - \sum_{k=1}^{p} a_k s[n-k]$$

Trong miền Z: $E(z) = S(z) \cdot A(z)$, tức là $e[n]$ là đầu ra của **bộ lọc inverse** $A(z)$.

### 4.2 Ý Nghĩa Vật Lý

Prediction error signal $e[n]$ chính là **ước lượng của tín hiệu kích thích (excitation)** — tức là nguồn tạo ra tiếng nói tại glottis:

| Loại âm | Prediction Error |
|---------|----------------|
| **Voiced** | Chuỗi xung tuần hoàn (pitch pulses) — dây thanh rung |
| **Unvoiced** | Nhiễu trắng ngẫu nhiên (white noise) — luồng khí rít |

> [!info] Ứng dụng trong Speech Coding
> Trong **CELP (Code Excited Linear Prediction)** — chuẩn nén tiếng nói của điện thoại di động — người ta truyền đi bộ hệ số LPC + excitation thay vì toàn bộ tín hiệu → tiết kiệm băng thông gấp nhiều lần.

### 4.3 Key Concepts

- **Minimum prediction error** → mô hình khớp tốt nhất với vocal tract
- **Inverse filter** $A(z)$ "whitens" tín hiệu tiếng nói → $e[n]$ gần như white noise với voiced sounds
- Phân tích $e[n]$ → có thể trích xuất **pitch period**

---

## 5. Liên Hệ Với Lossless Tube Models

### 5.1 Acoustic Tube Model Là Gì?

**Acoustic tube model** biểu diễn vocal tract như một chuỗi các ống hình trụ:

```
Glottis                                    Lips
  │                                          │
  ▼                                          ▼
[Tube 1] [Tube 2] [Tube 3] ... [Tube M] → [Output]
  A1       A2       A3           AM

Mỗi ống có: Chiều dài, Đường kính, Boundary conditions
```

**"Lossless"** có nghĩa là giả định **không mất năng lượng** trong ống — sóng chỉ truyền và phản xạ.

### 5.2 Liên Hệ LPA ↔ Tube Model

| LPA | Acoustic Tube Model |
|-----|-------------------|
| Hệ số dự đoán $a_k$ | Hệ số phản xạ tại các nối ống |
| Poles của $H(z)$ | Tần số cộng hưởng của ống |
| Bậc $p$ của mô hình | Số lượng ống $M$ |
| LPC spectrum | Hàm truyền đạt của ống |

> **Cả LPA và tube model đều nhằm mục tiêu:** Xác định các **tần số cộng hưởng (formants)** của vocal tract.

### 5.3 Reflection Coefficients (PARCOR)

Từ Levinson-Durbin, ta thu được các **reflection coefficients** $k_m$ — tương ứng với hệ số phản xạ tại mỗi nối ống trong tube model.

$$|k_m| < 1 \quad \forall m \Leftrightarrow \text{Hệ thống ổn định (stable)}$$

> [!important] Điều kiện ổn định
> Nếu tất cả $|k_m| < 1$ → bộ lọc LPC ổn định → vocal tract model hợp lệ.

### 5.4 Tóm Tắt Mối Quan Hệ

> LPA và acoustic tube models cùng nhằm mô tả **spectral properties của tiếng nói** bằng cách xác định resonant frequencies. Các hệ số LPC có thể được diễn giải trực tiếp như **formants** trong tube model tương đương, cung cấp nền tảng vật lý cho speech analysis và synthesis.

---

## Tóm Tắt

```
Tiếng nói s[n]
        │
        ▼
Autocorrelation R[k]
        │
        ▼ Levinson-Durbin
Hệ số LPC: a_1, a_2, ..., a_p
        │
        ├──→ H(z) = G/A(z) → LPC Spectrum → Formants (F1, F2, F3)
        │
        ├──→ Gain G → Năng lượng excitation
        │
        └──→ e[n] = s[n]*A(z) → Prediction Error → Pitch / Excitation type
```

| Khái niệm | Ý nghĩa |
|-----------|---------|
| **LPC coefficients** | Mô tả hình dạng vocal tract |
| **Poles của H(z)** | Tương ứng với Formants |
| **Gain G** | Năng lượng tín hiệu kích thích |
| **Prediction Error e[n]** | Ước lượng glottal excitation |
| **Reflection coefficients** | Tương ứng với hệ số phản xạ ống âm |

---

## Liên Kết

- [[Chapter 7]] — Frequency-Domain Representations
- [[Chapter 9]] — Algorithms for Estimating Speech Parameters
- [[Chapter 3]] — Human Speech Production (Formants, Vocal Tract)
- [[Formants]]
- [[MFCCs]]
- [[LPC]]

---

*Chapter 9 · Linear Predictive Analysis of Speech Signals · Rabiner & Schafer · Tự học*


_(Bao trùm các câu: 26, 33, 38)_

LPC (Linear Predictive Coding) là nền tảng của hầu hết các codec nén giọng nói trên điện thoại (GSM) hoặc ứng dụng gọi điện (Skype, WhatsApp). Nó không nén file audio, nó "bắt chước" cổ họng con người!



**2. Tín hiệu Lỗi dự đoán (Prediction Error Signal - Câu 26)**

- **Công thức LPC cốt lõi:** LPC dự đoán mẫu âm thanh hiện tại dựa trên $p$ mẫu trong quá khứ: $$\tilde{s}[n] = \sum_{k=1}^p \alpha_k s[n-k]$$ Tín hiệu lỗi $e[n]$ chính là **Sự chênh lệch giữa tín hiệu dự đoán và tín hiệu thực tế (The difference between predicted and actual speech signals)**: $$e[n] = s[n] - \tilde{s}[n]$$
- **Bản chất Kỹ sư:** Tại sao kỹ sư lại thích tín hiệu Lỗi $e[n]$ này? Vì sau khi trừ đi phần dự đoán (chính là bộ lọc Formant), $e[n]$ sẽ trở thành một dải âm thanh "phẳng" (spectral flattening), loại bỏ hoàn toàn ảnh hưởng của khẩu hình miệng. Lúc này, $e[n]$ chính là **nguồn kích thích từ dây thanh đới**. Ta có thể dùng nó để tìm Pitch (độ cao giọng) cực kỳ chính xác!



**3. Vai trò của tham số Gain ($G$) trong LPC (Câu 33)**

- **Công thức Phục hồi (Synthesis):** $$s[n] = \sum_{k=1}^p \alpha_k s[n-k] + G \cdot u[n]$$
Bạn có bao giờ thắc mắc tại sao gọi điện thoại qua Zalo/Messenger tốn rất ít dung lượng mạng (khoảng 8-10 kbps) mà vẫn nghe rõ tiếng người bên kia không? Đó là nhờ kỹ thuật **LPC (Linear Predictive Coding)**.

**1. Tín hiệu Lỗi dự báo (Prediction Error Signal - Câu 51)**

- **Công thức cốt lõi:** Trong LPC, máy tính "dự đoán" mẫu âm thanh hiện tại $\tilde{s}[n]$ bằng cách lấy tổng có trọng số của $p$ mẫu trong quá khứ: $$\tilde{s}[n] = \sum_{k=1}^{p} \alpha_k s[n-k]$$
- Tín hiệu lỗi dự báo $e[n]$ (còn gọi là residual) chính là phần chênh lệch giữa thực tế và dự đoán: $$e[n] = s[n] - \tilde{s}[n]$$ _Tại sao câu 51 lại đúng?_ "By subtracting the model output from the original signal" chính xác là phép trừ toán học $s[n] - \tilde{s}[n]$. Về mặt vật lý, $e[n]$ này đã loại bỏ hoàn toàn ảnh hưởng của khẩu hình miệng (formant), nó chính là "nguồn kích thích" tinh khiết phát ra từ dây thanh đới!

**2. Phương pháp Bình phương Tối thiểu (Least Squares Method - Câu 41)**

- Làm sao để tìm ra bộ hệ số $\alpha_k$ tối ưu nhất? Các kỹ sư sử dụng **Phương pháp Bình phương Tối thiểu**.
- **Bản chất Toán học:** Ta muốn tổng bình phương tín hiệu lỗi (Mean-Squared Error) trong một khung $E_{\hat{n}}$ là nhỏ nhất: $$E_{\hat{n}} = \sum_{m} e^2[m] = \sum_{m} \left( s[m] - \sum_{k=1}^{p} \alpha_k s[m-k] \right)^2$$ Để $E_{\hat{n}}$ đạt cực tiểu, ta lấy đạo hàm theo từng hệ số $\alpha_k$ và cho bằng 0 ($\partial E_{\hat{n}}/\partial \alpha_k = 0$). Giải hệ phương trình tuyến tính này, ta sẽ được bộ hệ số $\alpha_k$ phản ánh chính xác cấu trúc ống phát âm của người nói.

**🇬🇧 1. The Core Purpose of LPC (Q73)**

- **Concept:** Linear Predictive Coding (LPC) assumes the human vocal tract is a plastic tube. The current speech sample can be **predicted based on past samples**.
- **Math:** $\tilde{s}[n] = \sum_{k=1}^{p} \alpha_k s[n-k]$.

**🇻🇳 1. Mục đích cốt lõi của LPC (Câu 73)**

- **Giải thích:** LPC mô phỏng ống phát âm của con người. Nó cho rằng mẫu âm thanh hiện tại hoàn toàn có thể được **dự đoán dựa trên các mẫu trong quá khứ (predict future speech samples based on past samples)** thông qua một phép tổng tuyến tính.

**🇬🇧 2. Formants and Prediction Error Filter (Q62, Q80, Q84)**

- **Concept:**
    - **Formants (Q62):** These are the **resonance frequencies of the vocal tract** (tần số cộng hưởng). They are what makes an "A" sound different from an "O".
    - **Estimating Formants (Q80):** Because LPC perfectly models the vocal tract envelope by drawing a smooth curve over the spectrum, **LPC is widely used to estimate formant frequencies**.
    - **Prediction Error Filter $A(z)$ (Q84):** The filter $A(z) = 1 - \sum \alpha_k z^{-k}$ is used to subtract the predicted speech from the actual speech. Its coefficients ($\alpha_k$) are optimized to minimize the energy of the prediction error signal $e[n]$.

**🇻🇳 2. Formant và Bộ lọc Lỗi Dự báo (Câu 62, 80, 84)**

- **Giải thích:** Formant chính là **các tần số cộng hưởng của ống phát âm (resonance frequency of the vocal tract)**. Để tìm ra Formant, kỹ sư AI thường dùng **mô hình LPC (Câu 80)** vì nó vẽ ra được đường bao phổ (spectral envelope) cực kỳ mượt.
- **Bản chất Bộ lọc Lỗi Dự báo (Câu 84):** Để tìm ra các hệ số $\alpha_k$ cho LPC, ta phải tạo ra một "Prediction Error Filter" (Bộ lọc lỗi dự báo). Hệ số của bộ lọc này được tính toán (derived) dựa trên việc cực tiểu hóa tín hiệu lỗi dự báo.

**2. Phương pháp Bình phương Tối thiểu (Least Squares Method - Câu 41)**

- Làm sao để tìm ra bộ hệ số $\alpha_k$ tối ưu nhất? Các kỹ sư sử dụng **Phương pháp Bình phương Tối thiểu**.
- **Bản chất Toán học:** Ta muốn tổng bình phương tín hiệu lỗi (Mean-Squared Error) trong một khung $E_{\hat{n}}$ là nhỏ nhất: $$E_{\hat{n}} = \sum_{m} e^2[m] = \sum_{m} \left( s[m] - \sum_{k=1}^{p} \alpha_k s[m-k] \right)^2$$ Để $E_{\hat{n}}$ đạt cực tiểu, ta lấy đạo hàm theo từng hệ số $\alpha_k$ và cho bằng 0 ($\partial E_{\hat{n}}/\partial \alpha_k = 0$). Giải hệ phương trình tuyến tính này, ta sẽ được bộ hệ số $\alpha_k$ phản ánh chính xác cấu trúc ống phát âm của người nói.

**1. Tính toán Tham số Gain (G) trong LPC (Câu 111)**

- **Công thức Tổng quát LPC Bắt buộc:** $$s[n] = \sum_{k=1}^{p} a_k s[n-k] + G \cdot u[n]$$ _(Ý nghĩa: Mẫu tiếng nói hiện tại $s[n]$ được dự đoán từ $p$ mẫu quá khứ, cộng thêm nguồn kích thích $u[n]$ được khuếch đại bởi Gain $G$)._
- **Tính $G$ như thế nào? (Đáp án B):** Để mô hình phát ra âm thanh có năng lượng bằng đúng giọng thật, tham số Gain $G$ thường được tính toán dựa trên **Hàm tự tương quan của tín hiệu tiếng nói (The autocorrelation of the speech signal)**.
    - _Công thức năng lượng lỗi (bằng $G^2$):_ $G^2 = R - \sum_{k=1}^{p} \alpha_k R[k]$ Trong đó $R[k]$ chính là các hệ số tự tương quan (autocorrelation). Việc giải phương trình Durbin-Levinson không chỉ cho ta bộ lọc $a_k$ mà còn trực tiếp cho ta tham số $G$ này!