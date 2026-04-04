---
tags:
  - machine-learning
  - deep-learning
status: "⬜ chưa học"
created: 2025-01-01
---

# Transfer Learning & Fine-tuning

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Deep Learning Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Chiến lược

| Chiến lược | Dataset | Approach |
|-----------|---------|----------|
| **Feature extraction** | Nhỏ, similar domain | Freeze toàn bộ, chỉ train classifier head |
| **Fine-tuning (vài layer)** | Trung bình | Unfreeze vài layer cuối |
| **Full fine-tuning** | Lớn, different domain | Unfreeze toàn bộ, lr nhỏ |

---

## Hugging Face (NLP)

```python
from transformers import AutoModelForSequenceClassification, Trainer, TrainingArguments

model = AutoModelForSequenceClassification.from_pretrained(
    "bert-base-uncased", num_labels=2
)

training_args = TrainingArguments(
    output_dir="./results",
    num_train_epochs=3,
    per_device_train_batch_size=16,
    learning_rate=2e-5,  # Nhỏ hơn nhiều so với train từ đầu
)

trainer = Trainer(model=model, args=training_args, train_dataset=train_data)
trainer.train()
```

---

## Related
- [[CNN - Convolutional Neural Network]]
- [[Transformer & Attention Mechanism]]
- [[Deep Learning Overview]]
