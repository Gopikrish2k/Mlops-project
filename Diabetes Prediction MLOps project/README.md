# Diabetes Prediction Model using FastAPI + Docker

Project work flow

- Model Training
- Building the Model locally
- API Deployment with FastAPI
- Dockerization
- Kubernetes Deployment

---

## Quick Start

### 1. Create Virtual Environment

```
python3 -m venv .mlops
.\.mlops\Scripts\activate
```

### 2. Install Dependencies

```
pip install -r requirements.txt
```

## Train the Model

```
python train.py
```

## Run the API Locally

```
uvicorn main:app --reload
```

### Sample Input for /predict

```
{
  "Pregnancies": 2,
  "Glucose": 130,
  "BloodPressure": 70,
  "BMI": 28.5,
  "Age": 45
}
```

## Dockerize the API

### Build the Docker Image

```
docker build -t diabetes-prediction-model .
```

### Run the Container

```
docker run -p 8000:8000 diabetes-prediction-model
```
### To view in web page 

```
http://localhost:8000/docs
```

