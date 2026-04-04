---
tags:
  - machine-learning
  - preprocessing
status: "⬜ chưa học"
created: 2025-01-01
---

# Missing Values & Outliers

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Data Preprocessing Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Missing Values

### Phân loại
| Loại | Ý nghĩa | Cách xử lý |
|------|---------|------------|
| MCAR | Missing hoàn toàn ngẫu nhiên | Drop rows / Simple imputation |
| MAR | Missing phụ thuộc vào data khác | Model-based imputation |
| MNAR | Missing phụ thuộc vào chính giá trị đó | Domain knowledge |

### Các kỹ thuật xử lý
- **Drop**: Xóa row/column (dùng khi missing < 5%)
- **Simple imputation**: Mean/Median/Mode
- **KNN imputation**: Dùng K điểm lân cận để điền
- **Iterative imputation**: Dự đoán bằng model (MICE)

```python
from sklearn.impute import SimpleImputer, KNNImputer

# Simple
imputer = SimpleImputer(strategy='median')

# KNN
imputer = KNNImputer(n_neighbors=5)
```

---

## Outliers

### Phát hiện
- **IQR method**: outlier nếu < Q1 - 1.5*IQR hoặc > Q3 + 1.5*IQR
- **Z-score**: outlier nếu |z| > 3
- **Isolation Forest**: unsupervised, tốt cho high-dim data

### Xử lý
- **Drop**: Xóa outlier
- **Cap (Winsorize)**: Giới hạn ở percentile nhất định
- **Transform**: Log transform để giảm ảnh hưởng

```python
# IQR
Q1 = df['col'].quantile(0.25)
Q3 = df['col'].quantile(0.75)
IQR = Q3 - Q1
df_clean = df[~((df['col'] < Q1 - 1.5*IQR) | (df['col'] > Q3 + 1.5*IQR))]
```

---

## Related
- [[Feature Scaling]]
- [[Feature Engineering Overview]]
- [[Data Preprocessing Overview]]
