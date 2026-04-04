---
tags:
  - machine-learning
  - workflow
status: "⬜ chưa học"
created: 2025-01-01
---

# Train / Validation / Test Split

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Quy tắc

| Tập | Tỉ lệ thông thường | Mục đích |
|-----|--------------------|---------|
| **Train** | 60–80% | Huấn luyện model |
| **Validation** | 10–20% | Tune hyperparameters |
| **Test** | 10–20% | Đánh giá cuối — **chỉ dùng 1 lần** |

> ⚠️ **Test set phải được "khóa" cho đến khi train xong hoàn toàn. Không dùng test set để chọn model.**

```python
from sklearn.model_selection import train_test_split

X_temp, X_test, y_temp, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
X_train, X_val, y_train, y_val = train_test_split(X_temp, y_temp, test_size=0.25, random_state=42)
# Kết quả: 60% train, 20% val, 20% test
```

---

## Related
- [[Cross Validation]]
- [[Scikit-learn Pipeline]]
