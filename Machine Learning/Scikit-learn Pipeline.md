---
tags:
  - machine-learning
  - workflow
  - scikit-learn
status: "⬜ chưa học"
created: 2025-01-01
---

# Scikit-learn Pipeline

> **Quay về:** [[🗺️ MOC - Machine Learning]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Tại sao dùng Pipeline?

- Tránh **data leakage** (fit scaler trên toàn bộ data thay vì chỉ train)
- Code gọn, dễ maintain
- Tự động apply transform đúng thứ tự
- Tích hợp tốt với [[Cross Validation]] và [[Grid Search & Random Search]]

---

## Cấu trúc cơ bản

```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.impute import SimpleImputer
from sklearn.ensemble import RandomForestClassifier

pipe = Pipeline([
    ('imputer', SimpleImputer(strategy='median')),
    ('scaler', StandardScaler()),
    ('model', RandomForestClassifier())
])

pipe.fit(X_train, y_train)
pipe.score(X_test, y_test)
```

## Pipeline với ColumnTransformer (numeric + categorical)

```python
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import OneHotEncoder

numeric_features = ['age', 'income']
cat_features = ['gender', 'city']

preprocessor = ColumnTransformer([
    ('num', StandardScaler(), numeric_features),
    ('cat', OneHotEncoder(drop='first'), cat_features)
])

pipe = Pipeline([
    ('preprocessor', preprocessor),
    ('model', RandomForestClassifier())
])
```

---

## Related
- [[Cross Validation]]
- [[Feature Scaling]]
- [[Encoding Categorical Data]]
- [[Grid Search & Random Search]]
