---
tags:
  - machine-learning
  - evaluation
  - regression
status: "⬜ chưa học"
created: 2025-01-01
---

# Evaluation Metrics — Regression

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Các metric chính

| Metric | Công thức | Ý nghĩa |
|--------|-----------|---------|
| **MAE** | $\frac{1}{n}\sum\|y_i - \hat{y}_i\|$ | Trung bình sai số tuyệt đối — dễ hiểu |
| **RMSE** | $\sqrt{\frac{1}{n}\sum(y_i - \hat{y}_i)^2}$ | Phạt nặng outlier, cùng đơn vị với Y |
| **R²** | $1 - \frac{SS_{res}}{SS_{tot}}$ | Tỉ lệ variance được giải thích (0–1) |
| **MAPE** | $\frac{100}{n}\sum\frac{\|y_i-\hat{y}_i\|}{y_i}$ | Sai số theo %, dễ báo cáo |

---

## Code

```python
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
import numpy as np

mae = mean_absolute_error(y_test, y_pred)
rmse = np.sqrt(mean_squared_error(y_test, y_pred))
r2 = r2_score(y_test, y_pred)
```

---

## Related
- [[Evaluation Metrics - Classification]]
- [[Linear Regression]]
- [[Cross Validation]]
