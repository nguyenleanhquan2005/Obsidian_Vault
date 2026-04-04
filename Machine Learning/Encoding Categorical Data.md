---
tags:
  - machine-learning
  - preprocessing
status: "⬜ chưa học"
created: 2025-01-01
---

# Encoding Categorical Data

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Data Preprocessing Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Các loại encoding

| Loại | Khi dùng | Ví dụ |
|------|----------|-------|
| **Label Encoding** | Ordinal (có thứ tự) | S < M < L < XL |
| **One-Hot Encoding** | Nominal (không có thứ tự) | màu sắc, quốc gia |
| **Ordinal Encoding** | Ordinal với số lượng lớn | rating 1-5 |
| **Target Encoding** | High cardinality, tree models | zip code, city |

```python
from sklearn.preprocessing import LabelEncoder, OrdinalEncoder
from sklearn.preprocessing import OneHotEncoder

# One-hot
ohe = OneHotEncoder(sparse=False, drop='first')  # drop='first' tránh dummy trap

# Target encoding (cần category_encoders)
import category_encoders as ce
enc = ce.TargetEncoder()
```

---

## Related
- [[Feature Scaling]]
- [[Feature Engineering Overview]]
- [[Data Preprocessing Overview]]
