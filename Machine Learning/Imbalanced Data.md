---
tags:
  - machine-learning
  - preprocessing
  - classification
status: "⬜ chưa học"
created: 2025-01-01
---

# Imbalanced Data

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Data Preprocessing Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Vấn đề

Khi một class chiếm >80% data, model sẽ thiên vị (bias) về class đó.  
Ví dụ: fraud detection (0.1% fraud), disease detection (5% positive).

---

## Cách xử lý

### 1. Đổi metric đánh giá
Không dùng Accuracy → dùng **F1-score**, **ROC-AUC**, **Precision-Recall AUC**  
→ Xem [[Evaluation Metrics - Classification]]

### 2. Resampling
| Kỹ thuật | Ý tưởng |
|----------|---------|
| **Oversampling (SMOTE)** | Tạo synthetic samples cho minority class |
| **Undersampling** | Giảm samples của majority class |
| **Combined** | Vừa over vừa under |

```python
from imblearn.over_sampling import SMOTE
from imblearn.under_sampling import RandomUnderSampler

sm = SMOTE(random_state=42)
X_res, y_res = sm.fit_resample(X_train, y_train)
```

### 3. Class weights
```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression(class_weight='balanced')

# XGBoost
model = XGBClassifier(scale_pos_weight=neg_count/pos_count)
```

---

## Related
- [[Evaluation Metrics - Classification]]
- [[Data Preprocessing Overview]]
- [[Logistic Regression]]
