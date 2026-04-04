---
tags:
  - machine-learning
  - mlops
status: "⬜ chưa học"
created: 2025-01-01
---

# Weights & Biases (W&B)

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[MLOps Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## So sánh với MLflow

| | MLflow | W&B |
|-|--------|-----|
| Setup | Self-hosted hoặc managed | Cloud-based |
| Visualization | Cơ bản | Rất đẹp, interactive |
| Phổ biến trong | Industry | Research, Academia |
| Giá | Free (self-host) | Free tier |

---

## Code cơ bản

```python
import wandb

wandb.init(project="ml-project", name="run-001")

wandb.config = {"lr": 0.001, "epochs": 10}

for epoch in range(10):
    # train...
    wandb.log({"loss": loss, "accuracy": acc, "epoch": epoch})

wandb.finish()
```

---

## Related
- [[MLflow]]
- [[MLOps Overview]]
