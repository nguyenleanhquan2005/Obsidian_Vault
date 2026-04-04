---
tags:
  - machine-learning
  - preprocessing
  - MOC
status: "⬜ chưa học"
created: 2025-01-01
---

# Data Preprocessing — Overview

> **Quay về:** [[🗺️ MOC - Machine Learning]]

> ⚡ **Đây là bước quan trọng nhất trong thực tế — chiếm 70-80% thời gian làm việc**

---

## Các bước preprocessing theo thứ tự

1. **Thu thập & hiểu data** — EDA (Exploratory Data Analysis)
2. [[Missing Values & Outliers]] — Xử lý dữ liệu thiếu và ngoại lệ
3. [[Feature Scaling]] — Chuẩn hóa scale
4. [[Encoding Categorical Data]] — Mã hóa biến phân loại
5. [[Imbalanced Data]] — Xử lý mất cân bằng nhãn
6. [[Feature Engineering Overview]] — Tạo feature mới
7. [[Feature Selection]] — Chọn feature quan trọng
8. [[Train Val Test Split]] — Chia tập dữ liệu

---

## Checklist trước khi train model

- [ ] Kiểm tra missing values
- [ ] Kiểm tra kiểu dữ liệu từng cột
- [ ] Visualize distribution của từng feature
- [ ] Kiểm tra class balance (classification)
- [ ] Scale features nếu dùng distance-based model
- [ ] Encode categorical features
- [ ] Bọc tất cả trong [[Scikit-learn Pipeline]]

---

## Dataview — Tất cả note Preprocessing

```dataview
TABLE status
FROM "Machine Learning"
WHERE contains(tags, "preprocessing")
```

---

## Related
- [[Scikit-learn Pipeline]]
- [[Feature Engineering Overview]]
- [[Cross Validation]]
