---
tags:
  - machine-learning
  - evaluation
  - classification
status: "⬜ chưa học"
created: 2025-01-01
---

# Evaluation Metrics — Classification

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Confusion Matrix

|  | Predicted Positive | Predicted Negative |
|--|--------------------|--------------------|
| **Actual Positive** | TP | FN |
| **Actual Negative** | FP | TN |

---

## Các metric chính

| Metric | Công thức | Khi ưu tiên |
|--------|-----------|-------------|
| **Accuracy** | $\frac{TP+TN}{Total}$ | Balanced classes |
| **Precision** | $\frac{TP}{TP+FP}$ | FP tốn kém (spam filter) |
| **Recall** | $\frac{TP}{TP+FN}$ | FN nguy hiểm (disease detection) |
| **F1-score** | $2 \cdot \frac{Precision \cdot Recall}{Precision + Recall}$ | Imbalanced data |
| **ROC-AUC** | Area under ROC curve | So sánh model tổng thể |

---

## Code

```python
from sklearn.metrics import (
    classification_report, confusion_matrix,
    roc_auc_score, f1_score
)

print(classification_report(y_test, y_pred))
print("ROC-AUC:", roc_auc_score(y_test, y_prob))
```

---

## Related
- [[Evaluation Metrics - Regression]]
- [[Imbalanced Data]]
- [[Cross Validation]]
