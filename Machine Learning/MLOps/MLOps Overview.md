---
tags:
  - machine-learning
  - mlops
  - MOC
status: "⬜ chưa học"
created: 2025-01-01
---

# MLOps — Overview

> **Quay về:** [[🗺️ MOC - Machine Learning]]

> ⚡ MLOps = đưa model từ notebook ra production và duy trì nó theo thời gian

---

## Vòng đời một ML project

```
Data Collection
  → Preprocessing [[Data Preprocessing Overview]]
  → Feature Engineering [[Feature Engineering Overview]]  
  → Model Training + Cross Validation [[Cross Validation]]
  → Evaluation [[Evaluation Metrics - Classification]]
  → Experiment Tracking [[MLflow]]
  → Deployment [[FastAPI + Docker Deployment]]
  → Monitoring [[Model Monitoring & Data Drift]]
  → (phát hiện drift → lặp lại)
```

---

## Công cụ

| Nhóm | Tool | Note |
|------|------|------|
| Experiment Tracking | [[MLflow]], [[Weights & Biases]] | Log metrics, params, artifacts |
| Model Serving | [[FastAPI + Docker Deployment]] | REST API |
| Data Versioning | [[DVC - Data Version Control]] | Git cho data & model |
| Monitoring | [[Model Monitoring & Data Drift]] | Detect data drift |

---

## Dataview

```dataview
TABLE status
FROM "Machine Learning/MLOps"
```
