---
tags:
  - machine-learning
  - theory
status: "⬜ chưa học"
created: 2025-01-01
---

# Bias-Variance Tradeoff

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Công thức

$$\text{Error} = \text{Bias}^2 + \text{Variance} + \text{Noise}$$

| | Bias cao | Variance cao |
|-|----------|-------------|
| **Biểu hiện** | Underfitting | Overfitting |
| **Train error** | Cao | Thấp |
| **Val error** | Cao | Cao |
| **Giải pháp** | Model phức tạp hơn | Regularization, more data |

---

## Chẩn đoán bằng Learning Curve

```python
from sklearn.model_selection import learning_curve
import matplotlib.pyplot as plt

train_sizes, train_scores, val_scores = learning_curve(
    model, X, y, cv=5, scoring='neg_mean_squared_error'
)
# Plot train vs validation score theo số lượng training samples
```

---

## Related
- [[Overfitting & Underfitting]]
- [[Regularization Algorithms]]
- [[Cross Validation]]
- [[Bias Variance Tradeoff]]
