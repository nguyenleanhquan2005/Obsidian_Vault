---
tags:
  - machine-learning
  - supervised-learning
  - MOC
status: "📖 đang học"
created: 2025-01-01
---

# Supervised Learning — Overview

> **Quay về:** [[🗺️ MOC - Machine Learning]]

## Định nghĩa

Supervised Learning là một loại machine learning trong đó các thuật toán được huấn luyện trên **labeled datasets** (tập dữ liệu có nhãn).

Mục tiêu: học mối quan hệ giữa **đầu vào X** và **đầu ra Y** để dự đoán trên dữ liệu mới.

$$f: \mathbb{R}^d \to Y$$

---

## Hai nhóm bài toán chính

| Bài toán | Đầu ra Y | Ví dụ |
|----------|----------|-------|
| [[Regression - Overview\|Regression]] | Số thực liên tục | Dự đoán giá nhà |
| [[Classification - Overview\|Classification]] | Nhãn rời rạc $\{1, 2, ..., C\}$ | Phân loại email spam |

---

## Regression — Các thuật toán

- [[Linear Regression]]
- [[Regularization Algorithms]] *(Ridge, Lasso, ElasticNet)*
- [[Decision Tree]]
- [[Ordinary Least Squares Regression]]
- [[Stepwise Regression]]
- [[Time Series Forecasting]]
- Jackknife Regression
- MARS (Multivariate Adaptive Regression Splines)
- LOESS (Locally Estimated Scatterplot Smoothing)

## Classification — Các thuật toán

- [[Logistic Regression]]
- [[Naive Bayes Classifier]]
- [[Perceptron Algorithm]]
- [[Support Vector Machine]]
- [[K-Nearest Neighbors]]
- [[Decision Tree]]
- [[Ensemble Algorithms Overview]]

---

## Dataview — Tất cả note Supervised Learning

```dataview
TABLE status, tags
FROM "Machine Learning/Supervised"
SORT file.name ASC
```

---

## Workflow chung

```
Raw Data
  → [[Data Preprocessing Overview|Preprocessing]]
  → [[Feature Engineering Overview|Feature Engineering]]
  → Train / [[Cross Validation|Cross Validate]]
  → [[Evaluation Metrics - Classification|Evaluate]]
  → [[Hyperparameter Tuning|Tune]]
  → [[Scikit-learn Pipeline|Deploy Pipeline]]
```

---

## Related
- [[Unsupervised Learning Overview]]
- [[Semi-Supervised Learning]]
- [[Bias Variance Tradeoff]]
- [[Overfitting & Underfitting]]
