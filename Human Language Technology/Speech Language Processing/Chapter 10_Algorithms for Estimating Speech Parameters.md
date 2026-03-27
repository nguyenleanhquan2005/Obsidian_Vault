---
tags:
  - speech-processing
  - algorithms
  - formant-estimation
  - VAD
  - chapter-10
aliases:
  - Speech Parameter Estimation
  - Ước Lượng Tham Số Tiếng Nói
date: 2026-03-24
status: complete
---

# Chapter 10 — Algorithms for Estimating Speech Parameters

> [!abstract] Tóm tắt chương
> Chương này trình bày các thuật toán thực tế để ước lượng các tham số quan trọng của tiếng nói: làm mượt tín hiệu bằng Median Smoothing, phân biệt tiếng nói với nền nhiễu, phát hiện âm hữu thanh bằng Bayesian inference, và ước lượng Formant từ LPC.

---

## Bản đồ nội dung

```
Algorithms for Estimating Speech Parameters
├── 1. Median Smoothing
│   ├── Định nghĩa & ưu điểm
│   ├── So sánh với Mean Smoothing
│   └── Ứng dụng trong speech processing
├── 2. Speech-Background/Silence Discrimination
│   ├── Tại sao cần phân biệt?
│   ├── Features: Energy, ZCR, Spectral
│   └── Thresholding & Algorithm
├── 3. Bayesian Voiced Detection
│   ├── Tại sao dùng Bayes?
│   ├── Công thức & Prior knowledge
│   └── Decision rule
└── 4. Formant Estimation
    ├── Tại sao ước lượng Formant?
    ├── Phương pháp LPC-based ★
    └── Quy trình thực hành
```

---

## 1. Median Smoothing

### 1.1 Định Nghĩa

**Median smoothing** là kỹ thuật loại bỏ outliers và giảm nhiễu tín hiệu bằng cách **thay mỗi điểm bằng giá trị median** của các điểm lân cận:

$$y[n] = \text{median}\left(x[n-L], \ldots, x[n], \ldots, x[n+L]\right)$$

Với $2L+1$ là kích thước cửa sổ.

### 1.2 So Sánh: Median vs Mean Smoothing

| | **Mean Smoothing** | **Median Smoothing** |
|-|-------------------|---------------------|
| **Công thức** | Trung bình cộng | Giá trị ở giữa khi sắp xếp |
| **Nhạy với outlier** | **Cao** — bị kéo lệch mạnh | **Thấp** — outlier không ảnh hưởng |
| **Bảo toàn cạnh** | Kém — làm mờ transitions | **Tốt** — giữ nguyên sharp transitions |
| **Loại bỏ impulse noise** | Kém | **Rất tốt** |

> [!example] Ví dụ trực quan
> Dữ liệu: `[10, 11, 12, 100, 13, 14, 15]`
> - **Mean** của 3 điểm giữa: $(12 + 100 + 13)/3 = 41.7$ → bị kéo lệch bởi 100
> - **Median** của 3 điểm giữa: $\text{median}(12, 100, 13) = 13$ → loại bỏ hoàn toàn outlier

### 1.3 Ứng Dụng Trong Speech Processing

Median smoothing được dùng rộng rãi trong:
- **Formant estimation** — làm mượt đường formant theo thời gian
- **Pitch detection** — loại bỏ các giá trị pitch sai lẻ tẻ
- **Speech enhancement** — giảm impulse noise

> [!tip] Python implementation
> ```python
> from scipy.signal import medfilt
> smoothed = medfilt(signal, kernel_size=5)
> ```

### 1.4 Điểm Yếu Của Median Smoothing

> [!warning] Hai nhược điểm chết người
> - **Độ trễ (Delay):** Để tính median của 5 frames tương lai, hệ thống phải **chờ** 5 frames đó → gây delay lớn trong real-time (Auto-Tune live concert bị lag 50ms!)
> - **Over-smoothing:** Tạo "block-like artifacts" — đường pitch thành bậc thang góc cạnh, làm mất chi tiết mịn

**Giải pháp thực tế:** Không dùng Median đơn độc — kết hợp với **Linear Smoother** phía sau để làm tròn góc cạnh (Tukey's combination smoother).

**🇬🇧 1. The Dangers of Median Smoothing (Unnumbered Q, Q77)**

- **Concept:** Median smoothing is great for removing sudden spikes (outliers) in pitch tracking. But it has critical flaws.
    - **Delay (Q77):** To find the median of the next 5 frames, the system _must wait_ for those 5 frames to be spoken. This **introduces a significant delay in real-time processing**. (Imagine Auto-Tune lagging by 50ms during a live concert!).
    - **Over-smoothing (Unnumbered Q):** It creates "blocky" artifacts and can **blur important short features** (like a quick consonant). Thus, for the unnumbered question, challenges include computational load, varying levels, and over-smoothing $\rightarrow$ **All of the above (c)**.

**🇻🇳 1. Điểm yếu của Bộ lọc Trung vị (Câu không số, Câu 77)**

- **Giải thích:** Median Smoothing (lấy trung vị) dùng để lọc nhiễu đột biến cực tốt. NHƯNG: Để tính trung vị của 5 mẫu tương lai, máy tính phải "ngồi đợi" người dùng nói xong 5 mẫu đó $\rightarrow$ **Gây ra độ trễ cực lớn trong xử lý thời gian thực (introduces significant delay - Câu 77)**. Hơn nữa, nó dẽ làm mất các chi tiết mịn (over-smoothing). Do đó đáp án câu không số đầu tiên là **All of the above**.

**3. Thuật toán làm mượt Median (Câu 40)**

- **Bản chất:** Median Smoothing (lấy trung vị) dùng để loại bỏ các điểm nhiễu đột biến (outliers), ví dụ bộ dò Pitch bỗng nhiên nhảy vọt lên do lỗi thuật toán.
- **Thách thức (All of the above):** Nhược điểm chết người của bộ lọc Median là nó làm mất đi các chi tiết mịn, biến đồ thị thành các hình bậc thang góc cạnh ("block-like artifacts"). Do đó, kỹ sư không bao giờ dùng Median đứng một mình, mà luôn phải kết hợp với bộ lọc tuyến tính (Linear Smoother) ở phía sau để làm tròn các góc cạnh (gọi là Tukey's combination smoother).


**2. Bộ lọc Trung vị (Median Smoothing) (Câu 114)**

- **Bản chất:** Lọc trung vị là sắp xếp các giá trị trong một cửa sổ theo thứ tự từ bé đến lớn rồi lấy giá trị ở giữa.
- **Tại sao nó hiệu quả với Nhiễu xung (Impulse Noise - Đáp án A)?** Nhiễu xung là những điểm sai số nhảy vọt (outliers). Ví dụ: Thuật toán dò Pitch đang chạy mượt ở 120Hz, bỗng nhiên có một khung bị lỗi nhảy vọt lên 400Hz.
- **Lỗi sai phổ biến:** Nếu bạn dùng bộ lọc Trung bình (Linear/Mean filter), giá trị 400Hz khổng lồ này sẽ bị "cào bằng" và kéo toàn bộ đồ thị sai theo. Bộ lọc Trung vị thì khác, nó hoàn toàn phớt lờ và "vứt bỏ" con số 400Hz dị biệt đó, giữ cho đường contour pitch của giọng nói mượt mà hoàn hảo.

---

## 2. Speech-Background/Silence Discrimination

### 2.1 Tại Sao Cần Phân Biệt?

**Phân biệt tiếng nói với nền nhiễu/im lặng** là bước nền tảng trong hầu hết hệ thống xử lý tiếng nói:

| Ứng dụng | Tại sao cần |
|----------|------------|
| **Voice Activity Detection (VAD)** | Biết khi nào user đang nói |
| **Speech enhancement** | Chỉ xử lý vùng có tiếng nói |
| **Speaker diarization** | Tách "ai nói khi nào" |
| **ASR** | Giảm tải tính toán, tránh nhận dạng nhầm silence |
(VAD - Voice Activity Detection), hay còn gọi là **Speech-Background/Silence Discrimination** (Phân biệt tiếng nói và nhiễu nền/khoảng lặng). 

Mục tiêu của thuật toán la tìm ra chính xác điểm bắt đầu (Beginning - B) và điểm kết thúc (Ending - E) của một câu nói,  giúp các hệ thống nhận dạng (ASR) tránh thời gian xử lý các đoạn nhiễu nền vô ích

Việc tìm điểm B và E không đơn giản chỉ là thấy âm thanh to lên thì cắt. Trong thực tế, kỹ sư phải đối mặt với các "cạm bẫy" sau,:

- Các âm xát yếu (như /f/, /th/, /h/) hoặc âm tắc/bật yếu (như /p/, /t/, /k/) nằm ở đầu hoặc cuối câu.
- Các âm mũi hoặc nguyên âm bị kéo dài và nhỏ dần (trailing off) ở cuối câu.

Để giải quyết, người ta không thể chỉ dùng **Short-time Log Energy (Năng lượng)** vì nó sẽ bỏ sót các âm xát/âm bật yếu,. Do đó, bắt buộc phải kết hợp thêm **Short-time Zero-Crossing Rate (ZCR)** để "bắt" các âm có tần số cao nhưng năng lượng thấp này,.

2. Tiền xử lý và Khởi tạo Ngưỡng (Thresholding)

Thuật toán hoạt động dựa trên các quy tắc heuristic (kinh nghiệm thực tiễn) được thiết lập rất thông minh:

- **Tiền xử lý:** Tín hiệu được đưa về tần số lấy mẫu chuẩn (10 kHz), đi qua bộ lọc thông cao (Highpass filter) để loại bỏ nhiễu dòng điện (DC offset/hum), sau đó chia thành các khung 40ms và dịch mỗi bước 10ms,.
- **Đo lường nhiễu nền:** Hệ thống sẽ giả định **100ms đầu tiên (10 khung)** của file ghi âm là khoảng lặng (vì người dùng thường mất một lúc phản xạ mới bắt đầu nói). Nó đo giá trị trung bình và độ lệch chuẩn của Năng lượng (eavg​,esig​) và ZCR (zcavg​,zcsig​) trong đoạn này để lập hồ sơ nhiễu nền.
- **Lập Ngưỡng (Thresholds):**
    - **Ngưỡng ZCR (**IZCT**):** Được tính bằng công thức max(IF,zcavg​+3⋅zcsig​), trong đó IF=35 là ngưỡng mặc định. Ngưỡng này sẽ tự động nâng lên nếu môi trường quá ồn.
    - **Ngưỡng Năng lượng:** Gồm ngưỡng trên khá an toàn (ITU, thường từ -10 đến -20 dB) và ngưỡng dưới nhạy hơn (ITR) được tính bằng max(ITU−10,eavg​+3⋅esig​),.

3. Quy trình 5 bước tìm kiếm (The Search Algorithm)

Sau khi có các ngưỡng, hệ thống bắt đầu "càn quét" theo 5 bước-:

- **Bước 1 (Tìm B1 bằng Năng lượng):** Dò từ đầu file, tìm khung có năng lượng vượt ngưỡng dưới ITR, đồng thời phải đảm bảo các khung lân cận đâm thủng được ngưỡng trên ITU. Khi thỏa mãn, ta đánh dấu điểm bắt đầu tạm thời là B1​.
- **Bước 2 (Tìm E1 bằng Năng lượng):** Dò ngược từ cuối file trở lại, áp dụng logic tương tự để tìm điểm kết thúc tạm thời E1​.
- **Bước 3 (Tinh chỉnh B1 bằng ZCR):** Dò ngược ra ngoài 25 khung từ B1​. Nếu phát hiện có từ 4 khung trở lên có ZCR vượt ngưỡng IZCT, hệ thống hiểu rằng có âm xát/âm bật bị bỏ sót. Nó sẽ lùi điểm bắt đầu ra xa hơn thành B2​.
- **Bước 4 (Tinh chỉnh E1 bằng ZCR):** Tương tự, dò tiến thêm 25 khung từ E1​. Nếu ZCR vượt ngưỡng, nó mở rộng điểm kết thúc thành E2​.
- **Bước 5 (Kiểm tra chéo):** Kiểm tra lại vùng lân cận [B2​,E2​] xem có cần mở rộng thêm theo ngưỡng năng lượng ITR không.

4. Ví dụ thực tế chứng minh độ hiệu quả,

- **Chữ "One":** Năng lượng làm rất tốt việc tìm B1 và E1. Vì không có âm xát, ZCR rất thấp và không can thiệp. (Kết quả: B1​=B2​,E1​=E2​).
- **Chữ "Six" (/s/ /ih/ /k/ /s/):** ZCR nhận diện được âm /s/ cực kỳ rõ rệt ở cả hai đầu, giúp mở rộng cả điểm bắt đầu và kết thúc một cách chính xác.
- **Chữ "Eight":** Âm nhả khí /t/ ở cuối câu có năng lượng cực nhỏ. Thuật toán đã dùng ZCR để mở rộng thành công điểm kết thúc chứa trọn vẹn âm /t/ này.
### 2.2 Features Dùng Để Phân Biệt

| Feature | Speech | Silence/Background |
|---------|--------|-------------------|
| **Energy (STE)** | Cao | Thấp |
| **Zero-Crossing Rate** | Vừa phải | Rất thấp (silence) hoặc cao (noise) |
| **Spectral content** | Có cấu trúc (formants, harmonics) | Phẳng hoặc ngẫu nhiên |
| **Temporal duration** | Có pattern | Không có pattern |

### 2.3 Thuật Toán Phân Biệt

**Energy-based thresholding** là phương pháp phổ biến nhất:

```
Tín hiệu đầu vào
        │
        ▼ Tính STE theo từng frame
E[n] cho mỗi frame
        │
        ▼ So với Threshold
E[n] > Threshold ?
    ├── YES → SPEECH
    └── NO  → SILENCE / BACKGROUND
```

**Spectral characteristics:**
- Tiếng nói có **formants và harmonics** đặc trưng
- Background noise thường có phổ **phẳng** hoặc ngẫu nhiên

**Temporal patterns:**
- Tiếng nói có **onset/offset** rõ ràng, khoảng ngắt có cấu trúc
- Silence thuần có duration dài, đồng đều

> [!tip] Bài tập Python
> ```python
> def speech_detection(signal, threshold):
>     energy = np.convolve(signal**2, np.ones(frame_size)/frame_size)
>     return energy > threshold  # True = speech, False = silence
> ```

---

## 3. Bayesian Voiced Detection

### 3.1 Tại Sao Dùng Bayesian Approach?

Thay vì dùng **luật cứng** (`if energy > threshold → Voiced`), Bayesian approach dùng **xác suất**:

> [!warning] Vấn đề với luật cứng
> Threshold cố định không thích nghi được với:
> - Tiếng nói nhanh/chậm khác nhau
> - Môi trường ồn ào hay yên tĩnh
> - Giọng người khác nhau (trẻ em, người già)

### 3.2 Framework Bayesian

**Bayes' Rule** áp dụng cho voiced detection:

$$P(\text{Voiced} | \mathbf{x}) = \frac{P(\mathbf{x} | \text{Voiced}) \cdot P(\text{Voiced})}{P(\mathbf{x})}$$

- $P(\text{Voiced} | \mathbf{x})$: **Posterior** — xác suất là Voiced sau khi quan sát features
- $P(\mathbf{x} | \text{Voiced})$: **Likelihood** — xác suất quan sát features này nếu là Voiced
- $P(\text{Voiced})$: **Prior** — kiến thức tiên nghiệm về tỉ lệ Voiced

### 3.3 Prior Knowledge — Điểm Mạnh Của Bayes

> [!important] Lợi thế chính
> Bayesian approach cho phép AI **tích hợp prior knowledge**:
> - Tiếng nói thường hữu thanh ~60% thời gian
> - Sau một âm voiced, khả năng voiced tiếp theo cao hơn
> - Điều kiện phòng (ồn/yên) ảnh hưởng xác suất

### 3.4 Features Dùng Trong Bayesian Detection

| Feature | Mô tả | Liên quan đến |
|---------|-------|--------------|
| **Pitch (F0)** | Tần số cơ bản | Dây thanh rung → Voiced |
| **Energy** | Năng lượng frame | Voiced > Unvoiced |
| **Harmonics** | Cấu trúc sóng hài | Chỉ Voiced có harmonics |
| **Formants** | Tần số cộng hưởng | Rõ trong Voiced |
| **Spectral regularity** | Phổ đều hay ngẫu nhiên | Voiced đều hơn |

### 3.5 Decision Rule

$$\text{Decision} = \begin{cases} \text{Voiced} & \text{nếu } P(\text{Voiced}|\mathbf{x}) > P(\text{Unvoiced}|\mathbf{x}) \\ \text{Unvoiced} & \text{ngược lại} \end{cases}$$

Hoặc dùng **log-likelihood ratio**:

$$\log \frac{P(\mathbf{x}|\text{Voiced})}{P(\mathbf{x}|\text{Unvoiced})} + \log \frac{P(\text{Voiced})}{P(\text{Unvoiced})} \gtrless 0$$

> [!info] Ứng dụng thực tế
> Bayesian voiced detection được dùng trong:
> - **Speech synthesis** — biết đoạn nào cần pitch variation
> - **ASR** — tách voiced/unvoiced cho acoustic model
> - **Speaker diarization** — phân đoạn tiếng nói

---

## 4. Formant Estimation

### 4.1 Tại Sao Ước Lượng Formant?

**Formants** là các spectral peaks — tần số cộng hưởng của vocal tract — mang thông tin cực kỳ quan trọng:

| Ứng dụng | Vai trò của Formant |
|----------|-------------------|
| **Phonetic analysis** | Phân biệt nguyên âm (/a/ vs /i/ vs /u/) |
| **Speech synthesis** | Tạo giọng tự nhiên với đúng formant |
| **Speaker recognition** | Formant pattern đặc trưng cho từng người |
| **Clinical speech** | Chẩn đoán rối loạn phát âm |

### 4.2 Phương Pháp LPC-Based (Chính)

**Quy trình ước lượng formant:**

```
Tiếng nói s[n]
        │
        ▼ 1. Pre-emphasis (khuếch đại tần cao)
        │   s'[n] = s[n] - α·s[n-1]  (α ≈ 0.97)
        │
        ▼ 2. Windowing (Hamming window)
        │
        ▼ 3. LPC Analysis → hệ số a_k
        │   (Levinson-Durbin, bậc p = 2·F_s/1000 + 2)
        │
        ▼ 4. Tìm Roots (nghiệm) của A(z)
        │   Poles: z_k = r_k · e^{jθ_k}
        │
        ▼ 5. Chuyển sang tần số
        │   F_k = θ_k · F_s / (2π)
        │
        ▼ 6. Lọc Formants hợp lệ
            (r_k > 0.5, 90 Hz < F_k < F_s/2)
```

### 4.3 Nguyên Lý: Peaks = Formants

Các **poles gần vòng tròn đơn vị** trong LPC filter tương ứng với **formant peaks**:

| Pole | Formant |
|------|---------|
| $z_1 = r_1 e^{j\theta_1}$, $r_1 \approx 1$ | F1 — formant thứ nhất |
| $z_2 = r_2 e^{j\theta_2}$, $r_2 \approx 1$ | F2 — formant thứ hai |
| $z_3 = r_3 e^{j\theta_3}$, $r_3 \approx 1$ | F3 — formant thứ ba |

### 4.4 Formant Patterns Của Nguyên Âm Tiếng Anh

| Nguyên âm | F1 (Hz) | F2 (Hz) | Ví dụ |
|-----------|---------|---------|-------|
| /i/ (high front) | ~270 | ~2300 | "see" |
| /æ/ (low front) | ~660 | ~1700 | "cat" |
| /ʌ/ (mid central) | ~600 | ~1000 | "cut" |
| /ɑ/ (low back) | ~730 | ~1090 | "father" |
| /u/ (high back) | ~300 | ~870 | "boot" |

> [!example] Ứng dụng thực tế
> **Siri phân biệt "Cat" và "Cut":** F2 của /æ/ (~1700 Hz) >> F2 của /ʌ/ (~1000 Hz) → đây là cơ chế nhận dạng nguyên âm qua formant.

### 4.5 Bước Thực Hành (Python)

```python
import numpy as np
from scipy.signal import lfilter, hamming
from numpy.linalg import roots

def estimate_formants(signal, fs, order=None):
    if order is None:
        order = int(2 * fs / 1000) + 2  # ~2 poles per kHz

    # 1. Pre-emphasis
    pre_emph = lfilter([1, -0.97], [1], signal)

    # 2. Windowing
    windowed = pre_emph * hamming(len(pre_emph))

    # 3. LPC via autocorrelation + Levinson-Durbin
    # (dùng librosa.lpc hoặc tự implement)
    from librosa.core.audio import lpc
    a = lpc(windowed, order=order)

    # 4. Find poles
    poles = roots(a)

    # 5. Convert to Hz, filter valid formants
    angles = np.angle(poles[np.abs(poles) > 0.5])
    freqs = sorted(angles[angles > 0] * fs / (2 * np.pi))
    return freqs
```

---

## 5. Khử Nhiễu: Spectral Subtraction

**Spectral Subtraction** là phương pháp kinh điển lọc tiếng ồn nền (quạt, điều hòa):

```
Đoạn Silence → Ước lượng phổ nhiễu N(ω)
        │
        ▼
|S(ω)|² = |X(ω)|² - |N(ω)|²  (trừ phổ)
        │
        ▼
Tiếng nói sạch hơn
```

> [!warning] "Musical Noise"
> Phép trừ tạo ra các vùng phổ âm (negative spectrum). Khi dùng trị tuyệt đối bù lại → tạo ra **"Musical Noise"** (tiếng ríu rít như chim hót) đặc trưng của Zoom/Google Meet khi noise suppression hoạt động quá mạnh. Cần thêm thuật toán smoothing để giảm.

---

## 6. Ước Lượng Pitch: Autocorrelation vs AMDF

### 6.1 Autocorrelation (STACF)

$$R[k] = \sum_{m} x[m] \cdot x[m+k]$$

- Dùng phép **NHÂN** — dịch tín hiệu đi $k$, nhân và cộng lại
- Tìm **đỉnh lặp lại** → xác định **tần số cơ bản F0**

### 6.2 AMDF — Average Magnitude Difference Function

$$\gamma[k] = \sum_{m} |x[m] - x[m-k]|$$

- Dùng phép **TRỪ + trị tuyệt đối** — khi tín hiệu lặp đúng một chu kỳ, hiệu số → 0 → tạo **"Thung lũng" (Valley)**
- Cùng mục đích với Autocorrelation: **ước lượng Pitch**

| | Autocorrelation | AMDF |
|-|----------------|------|
| **Phép tính** | Nhân (multiplication) | Trừ + abs |
| **Nhận dạng** | Đỉnh (peaks) | Thung lũng (valleys) |
| **Tốc độ** | Chậm hơn | **Nhanh hơn** trên DSP/IoT chip |
| **Lý do** | Phép nhân tốn cycles | Phép trừ + abs rẻ hơn nhiều |

> [!tip] Kỹ sư thực tế chọn AMDF cho các chip vi điều khiển (IoT, embedded) vì phép trừ chạy nhanh hơn phép nhân đáng kể.

---

## Tóm Tắt

```
Tín hiệu tiếng nói thô
        │
        ▼
Median Smoothing        → Loại bỏ outliers, làm mượt features
        │
        ▼
Speech/Silence Discrim. → Tìm vùng có tiếng nói (VAD)
        │
        ▼
Bayesian Voiced Detect. → Phân biệt Voiced / Unvoiced
        │
        ▼
Formant Estimation      → Trích xuất F1, F2, F3 (LPC-based)
        │
        ▼
Speech Parameters: Formants · Pitch · Energy · V/U labels
```

| Thuật toán | Mục đích | Phương pháp |
|-----------|---------|------------|
| **Median Smoothing** | Loại nhiễu, giữ cạnh | median filter |
| **Speech/Silence Discrim.** | VAD, segmentation | Energy + ZCR threshold |
| **Bayesian Voiced Detection** | V/U classification | Prior + Likelihood → Posterior |
| **Formant Estimation** | Trích xuất F1, F2, F3 | LPC poles → frequencies |

---

## Liên Kết

- [[Chapter 8]] — Linear Predictive Analysis (LPC, Poles, Formants)
- [[Chapter 5]] — Short-Time Analysis (STE, ZCR)
- [[Chapter 4]] — Hearing & Auditory Models (Bayesian Voicing)
- [[Chapter 10]] — Text-to-Speech Synthesis
- [[Formants]]
- [[LPC]]
- [[VAD]]

---

*Chapter 10 · Algorithms for Estimating Speech Parameters · Rabiner & Schafer · Tự học*
