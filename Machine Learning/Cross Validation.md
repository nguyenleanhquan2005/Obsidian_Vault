---
tags:
  - machine-learning
  - workflow
  - evaluation
status: "⬜ chưa học"
created: 2025-01-01
---

# Cross Validation

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Các loại

| Loại | Khi dùng |
|------|----------|
| **k-Fold** | Data đủ lớn, balanced |
| **Stratified k-Fold** | Classification với imbalanced data |
| **Leave-One-Out** | Dataset rất nhỏ |
| **Time Series Split** | Time series data (không shuffle!) |

```python
from sklearn.model_selection import cross_val_score, StratifiedKFold

cv = StratifiedKFold(n_splits=5, shuffle=True, random_state=42)
scores = cross_val_score(model, X, y, cv=cv, scoring='f1')
print(f"F1: {scores.mean():.3f} ± {scores.std():.3f}")
```

---

## Related
- [[Scikit-learn Pipeline]]
- [[Train Val Test Split]]
- [[Bias Variance Tradeoff]]
