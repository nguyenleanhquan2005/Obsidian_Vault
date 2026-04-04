---
tags:
  - machine-learning
  - deep-learning
  - MOC
status: "⬜ chưa học"
created: 2025-01-01
---

# Deep Learning — Overview

> **Quay về:** [[🗺️ MOC - Machine Learning]]

## Định nghĩa

Deep Learning là tập con của ML, sử dụng **Artificial Neural Networks** với nhiều hidden layers để học hierarchical representations từ data.

$$\text{AI} \supset \text{Machine Learning} \supset \text{Deep Learning}$$

---

## Kiến trúc theo bài toán

| Bài toán | Kiến trúc | Pretrained model phổ biến |
|----------|-----------|--------------------------|
| Ảnh, Video | [[CNN - Convolutional Neural Network]] | ResNet, EfficientNet, ViT |
| Text, NLP | [[Transformer & Attention Mechanism]] | BERT, GPT, RoBERTa |
| Sequential | [[RNN - LSTM - GRU]] | Time series, speech |
| Sinh data | [[GAN - Generative Adversarial Network]] | StyleGAN, DALL-E |

---

## Building blocks

- [[Neural Network Fundamentals]] — Neurons, layers, weights, biases
- [[Activation Functions]] — ReLU, Sigmoid, Softmax
- [[Loss Functions]] — CrossEntropy, MSE
- [[Optimizers]] — Adam, SGD, RMSProp
- [[Backpropagation]] — Cơ chế học của model

---

## Thực tế: Transfer Learning là chính

→ [[Transfer Learning & Fine-tuning]]

Không cần train từ đầu. Tiết kiệm 90% compute và data.

---

## Dataview

```dataview
TABLE status
FROM "Machine Learning/Deep Learning"
```
