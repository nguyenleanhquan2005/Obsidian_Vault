# Báo Cáo Phân Tích Hồi Quy Tuyến Tính
## Khảo Sát MLN111 — Đại Học FPT

> **Chủ đề nghiên cứu:** Tác động của việc tiếp xúc tin giả và nội dung AI đến sự xói mòn lòng tin vào truyền thông chính thống trong sinh viên FPT University

---

## 1. Thông Tin Mẫu & Biến Số

| Mục                    | Nội dung                                                                                                                                                       |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cỡ mẫu (n)**         | 60 sinh viên                                                                                                                                                   |
| **Biến độc lập (X)**   | Mức độ thường xuyên bắt gặp thông tin chưa được kiểm chứng khi lướt mạng xã hội *(Phần 1 — câu 1)*                                                             |
| **Biến phụ thuộc (Y)** | Mức độ đồng ý rằng việc tiếp xúc liên tục với tin giả do AI hỗ trợ đang xói mòn lòng tin vào truyền thông chính thống và các thể chế xã hội *(Phần 5 — câu 1)* |
| **Thang đo**           | Likert 5 mức: 1 = Hoàn toàn phản đối → 5 = Hoàn toàn đồng tình                                                                                                 |
| **Phần mềm phân tích** | Python 3.12 (pandas, statsmodels, scipy) — tương đương SPSS                                                                                                    |


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

## 3. Kết Quả Phân Tích

### 3.1 Bảng tóm tắt kết quả

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

### 3.2 Phương trình hồi quy

$$\hat{Y} = 3.153 + 0.148 \cdot X$$

Nghĩa là: khi mức độ tiếp xúc tin giả tăng 1 bậc Likert, mức độ xói mòn lòng tin chỉ tăng 0.148 đơn vị — một con số rất nhỏ và **không đủ ý nghĩa thống kê**.

---

## 4. Kiểm Định Giả Thuyết

| | Nội dung |
|-|---------|
| **H₀** | Mức độ tiếp xúc tin giả (X) không có tác động tuyến tính lên sự xói mòn lòng tin (Y) |
| **H₁** | Mức độ tiếp xúc tin giả (X) có tác động tuyến tính lên sự xói mòn lòng tin (Y) |
| **Tiêu chí** | Bác bỏ H₀ nếu p-value < 0.05 |
| **Kết quả** | p = 0.3699 > 0.05 → **Không bác bỏ H₀** |

---

## 5. Kết Luận & Thảo Luận

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

## 6. Tài Liệu Tham Khảo (Phương pháp thống kê)

- Cohen, J. (1988). *Statistical Power Analysis for the Behavioral Sciences* (2nd ed.). Lawrence Erlbaum Associates.
- Field, A. (2018). *Discovering Statistics Using IBM SPSS Statistics* (5th ed.). SAGE Publications.
- Hair, J. F., et al. (2019). *Multivariate Data Analysis* (8th ed.). Cengage Learning.
- Seabold, S., & Perktold, J. (2010). Statsmodels: Econometric and statistical modeling with Python. *Proceedings of the 9th Python in Science Conference*.

---

*Báo cáo được tạo tự động từ dữ liệu khảo sát thực tế (n = 60) bằng Python 3.12 — statsmodels OLS, scipy.stats.pearsonr.*  
*Ngày phân tích: tháng 6 năm 2026*
