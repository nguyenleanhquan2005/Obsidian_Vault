---
tags:
  - machine-learning
  - mlops
status: "⬜ chưa học"
created: 2025-01-01
---

# MLflow

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[MLOps Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Code cơ bản

```python
import mlflow

with mlflow.start_run(run_name="xgboost-v1"):
    mlflow.log_param("n_estimators", 100)
    mlflow.log_param("max_depth", 5)
    
    model.fit(X_train, y_train)
    
    mlflow.log_metric("f1", f1_score(y_test, model.predict(X_test)))
    mlflow.log_metric("roc_auc", roc_auc_score(y_test, model.predict_proba(X_test)[:,1]))
    
    mlflow.sklearn.log_model(model, "model")

# Xem UI: mlflow ui (mở localhost:5000)
```

---

## Related
- [[Weights & Biases]]
- [[MLOps Overview]]
