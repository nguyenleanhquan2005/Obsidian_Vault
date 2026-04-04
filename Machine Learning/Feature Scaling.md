---
tags:
  - machine-learning
  - preprocessing
status: "⬜ chưa học"
created: 2025-01-01
---

# Feature Scaling

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Data Preprocessing Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Khi nào cần scaling?

**CẦN scaling:**
- [[K-Nearest Neighbors]] — distance-based
- [[Support Vector Machine]] — distance-based
- [[Neural Network Fundamentals]] — gradient descent nhạy cảm với scale
- Logistic Regression, Linear Regression khi dùng regularization

**KHÔNG cần scaling:**
- [[Decision Tree]], [[Random Forest]], [[XGBoost]], [[LightGBM]] — tree-based models

---

## Các kỹ thuật

| Tên | Công thức | Khi dùng |
|-----|-----------|----------|
| **Min-Max (Normalization)** | $x' = \frac{x - x_{min}}{x_{max} - x_{min}}$ | Khi cần range [0,1], không có outlier lớn |
| **Standard (Z-score)** | $x' = \frac{x - \mu}{\sigma}$ | Khi data phân phối chuẩn |
| **Robust Scaler** | Dùng median & IQR | Khi có outlier nhiều |

```python
from sklearn.preprocessing import StandardScaler, MinMaxScaler, RobustScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X_train)  # fit TRÊN train, transform cả train & test
```

> ⚠️ **CRITICAL**: Chỉ `fit` trên train set. Không fit trên test set để tránh data leakage.

---

## Related
- [[Missing Values & Outliers]]
- [[Encoding Categorical Data]]
- [[Scikit-learn Pipeline]]
- [[Data Preprocessing Overview]]
