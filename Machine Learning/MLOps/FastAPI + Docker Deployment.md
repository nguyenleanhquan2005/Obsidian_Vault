---
tags:
  - machine-learning
  - mlops
  - deployment
status: "⬜ chưa học"
created: 2025-01-01
---

# FastAPI + Docker Deployment

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[MLOps Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Workflow

```
Train model → joblib.dump() → FastAPI endpoint → Dockerfile → docker build → deploy
```

---

## FastAPI (main.py)

```python
from fastapi import FastAPI
from pydantic import BaseModel
import joblib, numpy as np

app = FastAPI()
model = joblib.load("model.pkl")

class Request(BaseModel):
    features: list[float]

@app.post("/predict")
def predict(req: Request):
    X = np.array(req.features).reshape(1, -1)
    return {"prediction": int(model.predict(X)[0]),
            "probability": float(model.predict_proba(X)[0, 1])}
```

## Dockerfile

```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```

## Lệnh build & run

```bash
docker build -t ml-api .
docker run -p 8000:8000 ml-api
# Test: curl -X POST http://localhost:8000/predict -H "Content-Type: application/json" -d '{"features": [1.2, 3.4, 5.6]}'
```

---

## Related
- [[MLflow]]
- [[DVC - Data Version Control]]
- [[MLOps Overview]]
