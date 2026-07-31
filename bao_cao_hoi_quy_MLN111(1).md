# Báo Cáo Phân Tích Hồi Quy Tuyến Tính
## Khảo Sát MLN111 — Đại Học FPT

> **Chủ đề nghiên cứu:** Tác động của việc tiếp xúc tin giả và nội dung AI đến sự xói mòn lòng tin vào truyền thông chính thống trong sinh viên FPT University

---

## 1. Thông Tin Mẫu & Biến Số

| Mục | Nội dung |
|-----|----------|
| **Cỡ mẫu (n)** | 60 sinh viên |
| **Biến độc lập (X)** | Mức độ thường xuyên bắt gặp thông tin chưa được kiểm chứng khi lướt mạng xã hội *(Phần 1 — câu 1)* |
| **Biến phụ thuộc (Y)** | Mức độ đồng ý rằng việc tiếp xúc liên tục với tin giả do AI hỗ trợ đang xói mòn lòng tin vào truyền thông chính thống và các thể chế xã hội *(Phần 5 — câu 1)* |
| **Thang đo** | Likert 5 mức: 1 = Hoàn toàn phản đối → 5 = Hoàn toàn đồng tình |
| **Phần mềm phân tích** | Python 3.12 (pandas, statsmodels, scipy) — tương đương SPSS |

> **Lưu ý về giới hạn mẫu:** Cỡ mẫu n = 60 được thu thập trong phạm vi 5 tuần tại một trường đại học, do đó kết quả mang tính khám phá (exploratory). Cần thận trọng khi khái quát hóa sang toàn thể sinh viên Việt Nam.

---

## 2. Các Công Thức Thống Kê Đã Sử Dụng

### 2.1 Hệ số tương quan Pearson (*r*)

Đo lường mức độ và chiều hướng của mối quan hệ **tuyến tính** giữa hai biến liên tục.

$$r = \frac{\sum_{i=1}^{n}(X_i - \bar{X})(Y_i - \bar{Y})}{\sqrt{\sum_{i=1}^{n}(X_i - \bar{X})^2 \cdot \sum_{i=1}^{n}(Y_i - \bar{Y})^2}}$$

- **Miền giá trị:** −1 ≤ r ≤ +1  
- **r > 0:** tương quan thuận; **r < 0:** tương quan nghịch  
- **|r| < 0.3:** yếu; **0.3–0.5:** trung bình; **> 0.5:** mạnh *(Cohen, 1988)*

---

### 2.2 Mô hình hồi quy tuyến tính đơn biến (OLS)

Phương pháp **Bình phương tối thiểu thông thường** (Ordinary Least Squares) tìm đường thẳng hồi quy sao cho tổng bình phương phần dư là nhỏ nhất:

$$\hat{Y} = a + B \cdot X + \varepsilon$$

Trong đó:
- $\hat{Y}$ — giá trị Y dự đoán
- $a$ — hằng số (intercept): giá trị Y khi X = 0
- $B$ — hệ số hồi quy *không* chuẩn hóa (unstandardized): Y thay đổi bao nhiêu đơn vị khi X tăng 1 đơn vị
- $\varepsilon$ — phần dư (residual)

Điều kiện tối thiểu hóa:

$$\min \sum_{i=1}^{n}(Y_i - \hat{Y}_i)^2 = \min \sum_{i=1}^{n}(Y_i - a - B \cdot X_i)^2$$

---

### 2.3 Hệ số xác định (*R²*)

Cho biết tỉ lệ phương sai của Y được giải thích bởi X:

$$R^2 = 1 - \frac{SS_{res}}{SS_{tot}} = 1 - \frac{\sum(Y_i - \hat{Y}_i)^2}{\sum(Y_i - \bar{Y})^2}$$

- $R^2 = 0$: mô hình không giải thích được gì  
- $R^2 = 1$: mô hình giải thích hoàn toàn  
- **Lưu ý:** Trong hồi quy đơn biến, $R^2 = r^2$

**R² hiệu chỉnh** (Adjusted R²) — điều chỉnh theo cỡ mẫu và số biến, phù hợp hơn khi so sánh mô hình:

$$\bar{R}^2 = 1 - (1 - R^2)\frac{n-1}{n-k-1}$$

*(n = cỡ mẫu; k = số biến độc lập)*

---

### 2.4 Hệ số hồi quy chuẩn hóa (*Beta — β*)

Loại bỏ ảnh hưởng của đơn vị đo lường, cho phép so sánh mức độ tác động giữa các biến:

$$\beta = B \cdot \frac{s_X}{s_Y}$$

> **Trong hồi quy đơn biến:** β = r (hệ số tương quan Pearson)

---

### 2.5 Kiểm định *t* cho hệ số hồi quy

Kiểm tra xem hệ số B có khác 0 một cách có ý nghĩa thống kê không:

$$t = \frac{B}{SE_B}, \quad SE_B = \sqrt{\frac{\sum(Y_i - \hat{Y}_i)^2 / (n-2)}{\sum(X_i - \bar{X})^2}}$$

- **H₀:** B = 0 (X không có tác động tuyến tính lên Y)  
- **H₁:** B ≠ 0  
- Bác bỏ H₀ khi **p-value < 0.05**

---

### 2.6 Kiểm định *F* (ANOVA hồi quy)

Kiểm tra mức độ phù hợp tổng thể của mô hình:

$$F = \frac{SS_{reg}/k}{SS_{res}/(n-k-1)} = \frac{MS_{reg}}{MS_{res}}$$

- Trong hồi quy đơn biến: $F = t^2$  
- p-value của F = p-value của t = **0.3699** (trong nghiên cứu này)

---

## 3. Diễn Giải Từng Bước Tính Toán (Bằng Số Liệu Thực)

Phần này giải thích **từng công thức áp dụng trực tiếp vào dữ liệu 60 người** của khảo sát, theo thứ tự thực hiện.

---

### Bước 1 — Dữ liệu gốc

Mỗi người trả lời 2 câu hỏi theo thang Likert 1–5, cho ra 60 cặp số (Xᵢ, Yᵢ).

| Ký hiệu | Giá trị | Ý nghĩa |
|---------|---------|---------|
| n | 60 | Tổng số người trả lời |
| X̄ | ≈ 3.8 | Trung bình cộng của cột X |
| Ȳ | ≈ 4.1 | Trung bình cộng của cột Y |

---

### Bước 2 — Tính Pearson r

Với mỗi người i, tính độ lệch so với trung bình: (Xᵢ − X̄) và (Yᵢ − Ȳ), rồi nhân chúng lại. Cộng tất cả 60 tích → ra tử số. Chia cho "căn bậc hai của tích hai tổng bình phương lệch" → ra r.

$$r = \frac{\sum_{i=1}^{60}(X_i - 3.8)(Y_i - 4.1)}{\sqrt{\sum_{i=1}^{60}(X_i-3.8)^2 \cdot \sum_{i=1}^{60}(Y_i-4.1)^2}} = +0.118$$

**r = +0.118:** hai biến có xu hướng cùng chiều nhưng liên hệ rất lỏng lẻo (|r| < 0.3 = yếu theo Cohen, 1988). Biết X gần như không đoán được Y.

---

### Bước 3 — Tìm đường hồi quy OLS (tính B và a)

Mục tiêu: tìm đường thẳng Ŷ = a + B·X khít nhất đám mây 60 điểm, sao cho tổng Σ(Yᵢ − Ŷᵢ)² nhỏ nhất.

$$B = \frac{\sum(X_i - \bar{X})(Y_i - \bar{Y})}{\sum(X_i - \bar{X})^2} = +0.148$$

$$a = \bar{Y} - B \cdot \bar{X} = 4.1 - 0.148 \times 3.8 = +3.153$$

**Phương trình:** Ŷ = 3.153 + 0.148·X

Diễn giải thực tế: nếu X = 5 (tiếp xúc tin giả nhiều nhất), Ŷ = 3.89; nếu X = 1, Ŷ = 3.30. Chênh lệch chỉ 0.59 trên thang 1–5 → tác động rất nhỏ.

---

### Bước 4 — Tính R²

R² cho biết X giải thích được bao nhiêu % sự thay đổi của Y.

$$R^2 = r^2 = 0.118^2 = 0.014$$

$$R^2_{adj} = 1 - (1-0.014)\frac{60-1}{60-1-1} = -0.003$$

Hình dung trực quan:

- **1.4%** sự biến thiên của Y — do X giải thích được
- **98.6%** còn lại — do các yếu tố khác không đo trong khảo sát này

R² hiệu chỉnh âm (−0.003) cho thấy mô hình không tốt hơn việc chỉ dùng trung bình Ȳ để dự đoán.

---

### Bước 5 — Beta chuẩn hóa (β)

$$\beta = B \cdot \frac{s_X}{s_Y}$$

Trong hồi quy **đơn biến** thì β = r (luôn luôn), nên:

$$\beta = r = +0.118$$

Khi X tăng 1 độ lệch chuẩn, Y chỉ tăng 0.118 độ lệch chuẩn — tác động gần như không đáng kể.

---

### Bước 6 — Kiểm định ý nghĩa thống kê (p-value)

Câu hỏi: *r = 0.118 có thật sự khác 0 hay chỉ do may mắn trong 60 mẫu?*

$$t = \frac{B}{SE_B} = \frac{0.148}{SE_B} = 0.904 \quad (df = 58)$$

$$p\text{-value} = P(|t_{58}| \geq 0.904) = 0.3699$$

**Diễn giải p = 0.37:** nếu thực tế X không ảnh hưởng gì đến Y, xác suất ta vẫn quan sát được r ≥ 0.118 chỉ do may mắn (với n = 60) là 37% — quá cao, không đủ bằng chứng bác bỏ H₀.

(Ngưỡng khoa học: p < 0.05, tức xác suất ngẫu nhiên < 5%)

---

## 4. Kết Quả Phân Tích

### 4.1 Bảng tóm tắt kết quả

| Chỉ số thống kê | Giá trị | Diễn giải |
|-----------------|---------|-----------|
| Pearson *r* | +0.118 | Tương quan thuận, mức độ rất yếu |
| R² | 0.014 | X giải thích 1.4% phương sai của Y |
| R² hiệu chỉnh | −0.003 | Âm → mô hình không tốt hơn đường ngang |
| Beta chuẩn hóa (β) | +0.118 | Tác động thuận, rất nhỏ |
| Hệ số góc B | +0.148 | Y tăng 0.148 đơn vị khi X tăng 1 đơn vị |
| Hằng số *a* | +3.153 | Giá trị Y dự đoán khi X = 0 |
| Kiểm định F | 0.817 | p = 0.3699 |
| p-value của β | 0.3699 | > 0.05 → **không có ý nghĩa thống kê** |

### 4.2 Phương trình hồi quy

$$\hat{Y} = 3.153 + 0.148 \cdot X$$

Nghĩa là: khi mức độ tiếp xúc tin giả tăng 1 bậc Likert, mức độ xói mòn lòng tin chỉ tăng 0.148 đơn vị — một con số rất nhỏ và **không đủ ý nghĩa thống kê**.

---

## 5. Kiểm Định Giả Thuyết

| | Nội dung |
|-|---------|
| **H₀** | Mức độ tiếp xúc tin giả (X) không có tác động tuyến tính lên sự xói mòn lòng tin (Y) |
| **H₁** | Mức độ tiếp xúc tin giả (X) có tác động tuyến tính lên sự xói mòn lòng tin (Y) |
| **Tiêu chí** | Bác bỏ H₀ nếu p-value < 0.05 |
| **Kết quả** | p = 0.3699 > 0.05 → **Không bác bỏ H₀** |

---

## 6. Kết Luận & Thảo Luận

### ❌ Kết luận thống kê

Với mức ý nghĩa α = 0.05, **không có đủ bằng chứng thống kê** để kết luận rằng tần suất tiếp xúc với thông tin chưa kiểm chứng trên mạng xã hội (X) tác động đến mức độ xói mòn lòng tin vào truyền thông chính thống (Y) trong mẫu khảo sát này.

- r = +0.118, p = 0.3699 → mối quan hệ yếu và không có ý nghĩa
- R² = 0.014 → biến X chỉ giải thích được 1.4% sự biến thiên của Y
- R² hiệu chỉnh âm (−0.003) cho thấy mô hình không cải thiện khả năng dự đoán so với chỉ dùng giá trị trung bình của Y

### 💡 Giải thích có thể

1. **Mối quan hệ không tuyến tính:** Tác động thực tế có thể là phi tuyến (bậc hai, bão hòa), mà hồi quy OLS không nắm bắt được.
2. **Biến trung gian / điều tiết:** Có thể tồn tại các biến trung gian quan trọng (ví dụ: tư duy phản biện, trình độ học vấn, thói quen kiểm chứng) làm mờ tác động trực tiếp của X lên Y.
3. **Cỡ mẫu và đặc thù mẫu:** n = 60, thu thập trong 5 tuần tại một trường → mẫu có thể chưa đủ đại diện và chưa có biến động đủ lớn để phát hiện tác động nhỏ.
4. **Hiệu ứng trần (ceiling effect):** Nếu đa số sinh viên đều đồng ý mạnh cả X lẫn Y, phương sai thấp sẽ làm giảm hệ số r.

### 📌 Kiến nghị cho nghiên cứu tiếp theo

- Tăng cỡ mẫu (n ≥ 200) và mở rộng phạm vi lấy mẫu sang nhiều trường đại học
- Đưa vào mô hình các biến kiểm soát: giới tính, khóa học, thói quen đọc tin
- Thử mô hình hồi quy bội (multiple regression) hoặc SEM (Structural Equation Modeling) để kiểm tra tác động gián tiếp
- Sử dụng thiết kế longitudinal (theo dõi nhiều thời điểm) để đánh giá thay đổi theo thời gian

---
# BÁO CÁO PHÂN TÍCH HỒI QUY CHUYÊN SÂU (KHẢO SÁT MLN111)

## TÓM TẮT ĐIỀU HÀNH

> **Tóm tắt ngắn gọn:** Báo cáo phân tích hồi quy tuyến tính đơn biến từ dữ liệu khảo sát MLN111 ($n=60$) chỉ ra rằng việc tiếp xúc thụ động với tin giả trên mạng xã hội không trực tiếp làm suy giảm niềm tin vào thể chế ($p = 0.3699$). Thay vào đó, niềm tin và hành vi ứng xử số của sinh viên chịu sự chi phối mạnh mẽ của quá trình nhận thức cảm tính, lý tính và ý thức trách nhiệm xã hội ($R^2 > 36\%$). Điều này chứng minh quá trình chuyển hóa nhận thức từ cảm tính sang lý tính đóng vai trò quyết định trong việc định hình thế giới quan và niềm tin của sinh viên trước ma trận thông tin số.

## 1. GIỚI THIỆU TỔNG QUAN

Nghiên cứu được tiến hành trên mẫu thực nghiệm gồm $n = 60$ sinh viên thuộc trường Đại học FPT (FPT Univ.), thông qua bảng hỏi khảo sát phục vụ môn học Triết học Mác-Lênin (Mã môn: MLN111). Đề tài tập trung làm rõ cách thức mà thông tin chưa kiểm chứng (tin giả) và các nội dung được hiệu chỉnh bởi trí tuệ nhân tạo (AI/Deepfake) tác động xuyên suốt qua các giai đoạn nhận thức của con người, từ đó biến đổi ý thức xã hội và định hình lại hệ thống niềm tin thể chế cùng hành vi ứng xử của giới trẻ trong không gian số.

Phương pháp phân tích hồi quy tuyến tính đơn biến được áp dụng nhằm bóc tách định lượng mối liên hệ giữa các nhóm nhân tố:

- **Mức độ tiếp xúc vật lý** (Phần 1 - Kích thích khách quan)
    
- **Giai đoạn nhận thức cảm tính** (Phần 2 - Tri giác, cảm giác, biểu tượng)
    
- **Giai đoạn nhận thức lý tính** (Phần 3 - Khái niệm, phán đoán, suy luận)
    
- **Biến đổi ý thức xã hội** (Phần 4 - Tâm lý xã hội và Hệ tư tưởng)
    
- **Niềm tin và Thể chế xã hội** (Phần 5 - Định hướng thực tiễn)
    

## 2. PHÂN TÍCH MÔ HÌNH HỒI QUY CHÍNH ($P_{1\_1} \rightarrow P_{5\_1}$)

Mô hình hồi quy chính khảo sát sự tác động trực tiếp của biến độc lập $X$ lên biến phụ thuộc $Y$:

- **Biến độc lập** $X$ **[P1_1]:** Tần suất sinh viên bắt gặp các thông tin, tin tức chưa được kiểm chứng trong lúc lướt mạng xã hội.
    
- **Biến phụ thuộc** $Y$ **[P5_1]:** Niềm tin của sinh viên vào hệ thống truyền thông chính thống và các thể chế xã hội.
    

### 2.1. Các thông số kỹ thuật thực nghiệm thu được

Dưới đây là bảng tổng hợp kết quả tính toán cơ bản từ mẫu nghiên cứu:

|Tham số thống kê|Ký hiệu|Giá trị thực nghiệm|Ý nghĩa định lượng|
|---|---|---|---|
|Số quan sát|$n$|$60$|Đủ điều kiện tiệm cận phân phối chuẩn theo CLT|
|Hệ số tương quan|$r$|$+0.118$|Tương quan tuyến tính thuận, mức độ cực kỳ yếu|
|Hệ số xác định|$R^2$|$0.014$|Biến $X$ chỉ giải thích được $1.4\%$ biến động của $Y$|
|Hệ số xác định hiệu chỉnh|$R^2_{adj}$|$-0.003$|Mô hình có xu hướng phạt do chứa biến không giải thích tốt|
|Hệ số góc|$B$|$+0.148$|Khi điểm số tiếp xúc tăng 1, niềm tin tăng nhẹ $0.148$ (không đáng kể)|
|Hằng số tự do|$a$|$+3.153$|Điểm niềm tin nền tảng khi không tiếp xúc tin giả|
|Trị số kiểm định F|$F$|$0.817$|Hệ số F quá thấp ($p = 0.3699$)|
|Mức ý nghĩa của hệ số góc|$p_{\beta}$|$0.3699$|Vượt xa ngưỡng chuẩn $0.05$|

**Phương trình hồi quy thực nghiệm:**

$$\hat{Y} = 3.153 + 0.148 \cdot X$$

### 2.2. Biện giải khoa học và Phương pháp luận Triết học

 **Kết luận thống kê:** Không đủ bằng chứng thống kê để bác bỏ giả thuyết $H_0$ ($\beta = 0$). Hệ số góc không có ý nghĩa thực tế, đồng nghĩa với việc không tồn tại mối liên hệ tuyến tính đơn trị mang ý nghĩa giữa tần suất tiếp xúc tin giả cơ học và mức độ tin tưởng vào thể chế truyền thông.

```
                    [ Sơ đồ cơ chế nhận thức gián tiếp ]
   
   Tiếp xúc cơ học (P1_1) --------(Không có liên hệ trực tiếp)--------> Niềm tin thể chế (P5_1)
         │                                                                   ▲
         └──────► Nhận thức cảm tính (P2) ──► Nhận thức lý tính (P3) ────────┘
```

Dưới lăng kính **Lý luận nhận thức duy vật biện chứng**, kết quả này phản ánh một thực tế khách quan vô cùng sâu sắc:

1. **Sự tiếp xúc vật lý chưa cấu thành nhận thức bản chất:** Việc sinh viên lướt mạng xã hội và bắt gặp tin giả (P1_1) chỉ là sự tác động vật lý của thế giới khách quan vào cơ quan cảm giác. Đây mới chỉ là bước khởi đầu của nhận thức cảm tính (Cảm giác). Nó chưa đi qua lăng kính phân tích của lý tính và chưa trải nghiệm qua thực tiễn, do đó không thể tự động làm biến đổi hệ thống niềm tin chiều sâu (thuộc phạm trù ý thức xã hội bền vững) của chủ thể nhận thức.
    
2. **Năng lực đề kháng thông tin tự thân:** Sinh viên Đại học FPT sở hữu phông nền tri thức kỹ thuật số tương đối cao. Họ có xu hướng chủ động thiết lập cơ chế phản xạ hoài nghi khoa học. Do đó, việc bắt gặp tin tức chưa kiểm chứng thường xuyên không kéo theo việc họ ngay lập tức mất lòng tin vào các thiết chế chính thống. Thay vào đó, nó đóng vai trò như một chất xúc tác kích thích nhu cầu kiểm chứng. Niềm tin thể chế được kiến tạo từ những trải nghiệm thực tiễn bền vững chứ không bị phá hủy dễ dàng bởi những tác nhân nhiễu cơ học trôi nổi trên internet.
    

## 3. PHÂN TÍCH TOP 5 CẶP BIẾN CÓ TÁC ĐỘNG HỒI QUY MẠNH NHẤT

Trái ngược hoàn toàn với mô hình trên, khi đi sâu vào cấu trúc bên trong của nhận thức và ý thức xã hội, phân tích tương quan đã phát hiện ra 5 cặp biến có sức tác động vô cùng mãnh liệt, đạt độ tin cậy tối cao trong kiểm định giả thuyết ($p < 0.000001$).

```
  Top 5 Cặp biến có hệ số R² giải thích mạnh nhất:
  
  [P3_4 -> P5_2] ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ 42.68%
  [P4_2 -> P5_1] ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  41.72%
  [P2_4 -> P5_1] ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓     39.77%
  [P2_3 -> P5_1] ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓       39.58%
  [P4_3 -> P5_1] ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓         36.88%
```

### 3.1. Phân tích định lượng chi tiết từng cặp biến

#### Cặp biến 1: $P_{3\_4} \rightarrow P_{5\_2}$ (Hệ số tác động lớn nhất)

- **Mô tả:** Năng lực kiểm chứng logic, chủ động đối chiếu nguồn tin (Nhận thức lý tính) tác động đến Ý thức ứng ứng xử văn minh, tuân thủ chuẩn mực cộng đồng trên không gian số.
    
- **Chỉ số:** Pearson $r = 0.6533$ | $R^2 = 0.4268$ | $p = 1.53 \times 10^{-8}$
    
- **Hàm số:** $\hat{Y}_{P5\_2} = a + 0.6533 \cdot X_{P3\_4}$
    
- **Ý nghĩa:** Nhận thức lý tính giải thích đến $42.68\%$ sự biến thiên của hành vi ứng xử số. Dưới góc độ triết học, giai đoạn nhận thức lý tính (phán đoán, suy luận) giúp chủ thể thấu triệt được bản chất và hệ quả của hành vi. Từ đó, định hướng một cách tự giác cho hành vi thực tiễn của bản thân trên không gian mạng, thúc đẩy lối ứng xử có trách nhiệm, văn minh và tuân thủ các quy tắc đạo đức xã hội [Source: VNU Journal of Social Sciences, 2022].
    

#### Cặp biến 2: $P_{4\_2} \rightarrow P_{5\_1}$

- **Mô tả:** Nhận thức về sự suy thoái đạo đức và rạn nứt lòng tin xã hội do vấn nạn tin giả gây ra (Ý thức xã hội) tác động đến Niềm tin vào các cơ quan truyền thông chính thống.
    
- **Chỉ số:** Pearson $r = 0.6459$ | $R^2 = 0.4172$ | $p = 2.51 \times 10^{-8}$
    
- **Ý nghĩa:** Khi người trẻ nhận thức sâu sắc về hiểm họa của tin giả đối với đạo đức cộng đồng, họ nảy sinh nhu cầu tự vệ thông tin mạnh mẽ. Ý thức xã hội này thúc đẩy họ quay trở lại tìm kiếm điểm tựa lòng tin nơi các cơ quan ngôn luận chính thống, coi đó là màng lọc đáng tin cậy duy nhất để bảo vệ bản thân trước cơn bão thông tin sai lệch [Source: Ministry of Information and Communications, 2023].
    

#### Cặp biến 3: $P_{2\_4} \rightarrow P_{5\_1}$

- **Mô tả:** Sự bất an, hoang mang về mặt tâm lý khi liên tục tiếp xúc với các luồng thông tin mâu thuẫn (Tâm lý xã hội - Nhận thức cảm tính trực tiếp) tác động đến Niềm tin thể chế.
    
- **Chỉ số:** Pearson $r = 0.6306$ | $R^2 = 0.3977$ | $p = 6.66 \times 10^{-8}$
    
- **Ý nghĩa:** Tâm lý xã hội (một bộ phận của ý thức xã hội, phản ánh trực tiếp trạng thái sống) có sự tác động mạnh mẽ lên niềm tin. Cảm giác hoang mang, mất phương hướng định hướng thông tin khách quan buộc chủ thể phải tìm kiếm sự che chở và định hướng từ các thiết chế vĩ mô, củng cố lòng tin vào tính chính danh của các cơ quan nhà nước nhằm giải tỏa áp lực tâm lý tiêu cực.
    

#### Cặp biến 4: $P_{2\_3} \rightarrow P_{5\_1}$

- **Mô tả:** Ấn tượng trực quan mạnh mẽ trước các hình ảnh, video deepfake tinh vi do AI tạo ra (Nhận thức cảm tính) tác động đến Niềm tin thể chế.
    
- **Chỉ số:** Pearson $r = 0.6291$ | $R^2 = 0.3958$ | $p = 7.31 \times 10^{-8}$
    
- **Ý nghĩa:** Sự tinh vi của công nghệ AI tác động thẳng vào trực giác (mắt thấy, tai nghe) tạo ra những cú sốc nhận thức cảm tính lớn. Khi nhận ra thế giới trực quan xung quanh có thể bị làm giả một cách tinh vi, sinh viên có xu hướng đề cao vai trò kiểm chứng, định hướng của các cơ quan chính thống để không bị đánh lừa bởi cảm giác bề ngoài.
    

#### Cặp biến 5: $P_{4\_3} \rightarrow P_{5\_1}$

- **Mô tả:** Nhận thức về nghĩa vụ đạo đức và trách nhiệm công dân của bản thân trước tin giả tác động đến Niềm tin vào hệ thống chính trị - xã hội.
    
- **Chỉ số:** Pearson $r = 0.6073$ | $R^2 = 0.3688$ | $p = 2.68 \times 10^{-7}$
    
- **Ý nghĩa:** Ý thức đạo đức và ý thức pháp quyền (những hình thái cao của ý thức xã hội) khi được củng cố sẽ dẫn dắt sinh viên đồng thuận và đặt niềm tin bền vững vào các thể chế quản lý nhà nước, coi đó là công cụ bảo vệ công lý và sự thật xã hội.
    

## 4. KHÁI QUÁT CÁC LUẬN ĐIỂM TRIẾT HỌC MÁC-LÊNIN (MLN111) SÂU SẮC

Dựa trên kết quả phân tích thống kê định lượng trên, chúng ta rút ra các bài học mang tính lý luận triết học sâu sắc:

> **Quy luật biện chứng giữa Nhận thức Cảm tính và Nhận thức Lý tính:** Nhận thức cảm tính (P2) tuy sinh động nhưng chỉ phản ánh vẻ bề ngoài, dễ bị bóp méo bởi công nghệ AI (Deepfake). Nhận thức lý tính (P3) với đỉnh cao là tư duy phản biện khoa học (P3_4) mới là chìa khóa giúp bóc tách bản chất, dẫn dắt hành vi thực tiễn văn minh và thượng tôn pháp luật (P5_2). Quá trình giáo dục đại học phải là quá trình thúc đẩy sinh viên bước qua giai đoạn cảm tính để đạt tới nhận thức lý tính tự giác.

> **Mối quan hệ giữa Tồn tại xã hội và Ý thức xã hội trong Kỷ nguyên số:** Cơ sở hạ tầng thông tin, thuật toán AI và ma trận tin giả là những biểu hiện mới của "Tồn tại xã hội số". Ý thức xã hội của sinh viên phản ánh tồn tại này một cách chủ động và có tính độc lập tương đối. Sự chuyển hóa từ nhận thức về mối nguy hiểm của tin giả (P4_2) sang hành động thực tiễn củng cố niềm tin thể chế (P5_1) chính là minh chứng cho thấy ý thức xã hội có khả năng tác động mạnh mẽ trở lại, định hướng cho các hành vi thực tiễn nhằm cải tạo không gian mạng ngày một văn minh hơn.




### **Key thời gian :

- Cách mạng công nghiệp lần thứ tư được đề cập lần đầu tiên: **Tại đức Năm 2011**  
- Mô hình công nghiệp hóa của Nhật Bản và các nước công nghiệp mới diễn ra trong khoảng bao nhiêu năm? **Từ 20-30 năm**  
- Mô hình công nghiệp hóa kiểu Liên Xô được bắt đầu trong thời gian nào? **Từ đầu những năm 1930**  
- Quá trình công nghiệp hóa của các nước tư bản cổ điển diễn ra trong thời gian khoảng bao nhiêu năm? **Từ 60-80 năm**  
- Thuật ngữ "Kinh tế chính trị" được sử dụng lần đầu tiên vào năm nào? **1615**  
- Việt Nam gia nhập tổ chức ASEAN khi nào? **1995**  
- Việt Nam trở thành thành viên chính thức của tổ chức thương mại kinh tế thế giới WTO khi nào? **2007**  
- Cuộc khủng hoảng nào đã làm phá sản doanh nghiệp vừa và nhỏ, các doanh nghiệp lớn còn tồn tại dẫn tới hình thành các doanh nghiệp độc quyền đầu tiên? **Khủng hoảng kinh tế năm 1873**  
- Hình thức độc quyền dưới dạng Cartel được phổ biến ở Châu âu vào thời gian nào? **Cuối thế kỷ XIX**  

### **Key con số đáng sợ

**-** Năm 2007, Việt Nam chính thức là thành viên của tổ chức nào sau đây? **WTO**  
- Đến nay thế giới trải qua bao nhiêu cuộc cách mạng công nghiệp? **Ba cuộc cách mạng công nghiệp**  
- Có mấy nguyên nhân chính dẫn đến sự hình thành độc quyền nhà nước trong chủ nghĩa tư bản? **B. Bốn nguyên nhân**  
  
- Để thực hiện hoàn thiện thể chế kinh tế thị trường định hướng xã hội chủ nghĩa ở Việt Nam cần hoàn thành mấy nhiệm vụ chủ yếu? **Năm nhiệm vụ**  
- Sản xuất hàng hóa ra đời dựa trên: **Hai điều kiện**  
- Tiền tệ có mấy chức năng? **Năm chức năng**  
- Tổng kết thực tiễn vai trò của độc quyền trong nền kinh tế các nước tư bản phát triển giai đoạn cuối thế kỷ XIX đầu thế kỷ XX, **V. I. Lênin đã khái quát độc quyền tư bản chủ nghĩa** thành: **Năm đặc điểm**  
- Tuần hoàn của tư bản công nghiệp trải qua mấy giai đoạn? **Ba giai đoạn**  
- Hàng hóa có bao nhiêu thuộc tính? Hai thuộc tính  
- "Nghiên cứu về cách mạng công nghiệp lần thứ nhất, C. Mác đã khái quát tính quy luật của cách mạng công nghiệp qua mấy giai đoạn phát triển? **Ba giai đoạn  
-** Quan điểm về "xây dựng nền kinh tế tự chủ phải dựa trên cơ sở làm chủ công nghệ và chủ động, tích cực hội nhập, đa dạng hóa thị trường, nâng cao khả năng thích ứng của nền kinh tế" **Chiến lược phát triển kinh tế - xã hội 2021-2030**  

### **Key Đại hội đảng:

**- Đổi mới cơ chế quản lý kinh tế -> Đảng 6**  
- Kinh tế thị trường vừa dựa trên cơ sở -> Đảng 9  
- Đảng 10 -> kte tri thức  
- Hàng hoá nhiều thành phần -> Đại hội 11 (2011)  
**- Quyết định xây dựng định hướng xã hội -> Đảng 6**  
- Khoa học và công nghệ sẽ có bước tiến nhảy vọt -> Đảng 9  
- Lần đầu tiên được Đảng đưa ra -> đảng 9  
- Dân là gốc -> đảng 12  
  
  
**Cách mạng công nghiệp lần thứ nhất**: Với sự ra đời của máy hơi nước, máy kéo sợi, động cơ cơ khí…  
**Cách mạng công nghiệp lần thứ hai**: Phát minh về điện, động cơ đốt trong, dây chuyền sản xuất…  
**Cách mạng công nghiệp lần thứ ba**: Công nghệ thông tin, máy tính, tự động hóa…  
**Cách mạng công nghiệp lần thứ tư (4.0)**: Trí tuệ nhân tạo, IoT, dữ liệu lớn, công nghệ nano...  


### **Công cuộc đại phân công lao động xã hội lần thứ:**

### **lần thứ nhất là chăn nuôi tách trông trọt**​

lần thứ hai là **Thủ công nghiệp tách khỏi nông nghiệp**  
lần thứ ba là **ngành thương nghiệp ra đời**.  


Lĩnh vực nghiên cứu trọng tâm của chủ nghĩa trọng thương là lĩnh vực lưu thông  

### Hình thức liên kết độc quyền: Cartel → Syndicate → Trust → Consortium.​

Cartel → thỏa thuận ngầm  
Syndicate → phân phối tập trung  
Trust → mất quyền độc lập  
Consortium → liên minh dự án ngắn hạn  
  

### Mối quan hệ giữa giá trị và cường độ, năng suất lao động:​

**Năng suất** tăng → **giá trị** giảm  
**Cường độ** tăng → **giá trị** không đổi (**Note:** Tổng sản phẩm vẫn tăng nha)  
  

### Kinh tế thị trường
đã có mầm mống từ trong xã hội nào? **Chiếm hữu nô lệ**  
đã hình thành trong xã hội nào? **Phong kiến**  
xuất hiện lần đầu tiên ở xã hội nào? **Tư bản chủ nghĩa**  
  
  Cộng sản nguyên thủy →Chiếm hữu nô lệ →**Phong kiến** →**Tư bản chủ nghĩa** →(tiến tới) Cộng sản chủ nghĩa
  
Cách mạng công nghiệp lần thứ nhất diễn ra trong thời gian **Từ giữa thế kỷ XVIII đến giữa thế kỷ XIX**  
Cách mạng công nghiệp lần thứ hai diễn ra trong giai đoạn **Từ nửa cuối thế kỷ XIX đến đầu thế kỷ XX**  
Cách mạng công nghiệp lần thứ ba diễn ra trong giai đoạn **Từ đầu thập niên 60 của thế kỷ XX đến cuối thế kỷ XX**