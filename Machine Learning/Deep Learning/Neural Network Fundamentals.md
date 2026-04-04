---
tags:
  - machine-learning
  - deep-learning
status: "⬜ chưa học"
created: 2025-01-01
---

# Neural Network Fundamentals

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Deep Learning Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Kiến trúc cơ bản

```
Input Layer → Hidden Layer(s) → Output Layer
```

Mỗi neuron: $z = \sum w_i x_i + b$ → qua [[Activation Functions]]: $a = f(z)$

---

## Các thành phần

| Thành phần | Vai trò |
|-----------|---------|
| **Weights (W)** | Tham số học được từ data |
| **Biases (b)** | Offset |
| **Activation** | Thêm phi tuyến → [[Activation Functions]] |
| **Loss** | Đo sai số → [[Loss Functions]] |
| **Optimizer** | Cập nhật W, b → [[Optimizers]] |

---

## Code PyTorch cơ bản

```python
import torch.nn as nn

class MLP(nn.Module):
    def __init__(self, input_dim, hidden_dim, output_dim):
        super().__init__()
        self.net = nn.Sequential(
            nn.Linear(input_dim, hidden_dim),
            nn.ReLU(),
            nn.Dropout(0.3),
            nn.Linear(hidden_dim, output_dim)
        )
    def forward(self, x):
        return self.net(x)
```

---

## Related
- [[Activation Functions]]
- [[Backpropagation]]
- [[Loss Functions]]
- [[Optimizers]]
- [[Perceptron Algorithm]]
