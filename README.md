# 🩺 didactic-broccoli

*(FastAPI · Docker · Kubernetes)*

> 🎥 Inspired by hands-on MLOps learning projects

**didactic-broccoli** is a **beginner-focused MLOps repository** designed to teach the **end-to-end lifecycle of a machine learning project** using a simple, real-world use case: **Diabetes Prediction**.

This project emphasizes **learning by doing**, making it ideal for students and newcomers exploring **MLOps, DevOps, and ML deployment**.

---

## 🎯 Project Objective

Build, serve, and deploy a machine learning model that predicts whether a person is diabetic based on basic health metrics—while following **production-style MLOps practices**.

---

## 📊 Problem Statement

Predict if a person is diabetic using the following features:

* Pregnancies
* Glucose
* Blood Pressure
* BMI
* Age

The model is trained using the **Pima Indians Diabetes Dataset** and a **Random Forest Classifier**.

---

## 🧠 What You’ll Learn

* ✅ Training a machine learning model
* ✅ Saving and loading trained models
* ✅ Building REST APIs with **FastAPI**
* ✅ Containerizing ML applications using **Docker**
* ✅ Deploying ML services on **Kubernetes**
* ✅ Understanding basic MLOps workflows

---

## 🗂️ Project Structure

```
didactic-broccoli/
│
├── train.py              # Model training script
├── main.py               # FastAPI application
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker configuration
├── k8s-deploy.yml        # Kubernetes deployment file
├── README.md             # Project documentation
└── .gitignore
```

---

## 🚀 Quick Start

### 1️⃣ Clone the Repository

```bash
git clone <your-repo-url>
cd didactic-broccoli
```

### 2️⃣ Create Virtual Environment

```bash
python3 -m venv .mlops
source .mlops/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🏋️ Train the Model

```bash
python train.py
```

This will train the Random Forest model and save it locally for inference.

---

## ⚡ Run the API Locally

```bash
uvicorn main:app --reload
```

Once running, access:

* API Docs: `http://127.0.0.1:8000/docs`

### Sample `/predict` Request

```json
{
  "Pregnancies": 2,
  "Glucose": 130,
  "BloodPressure": 70,
  "BMI": 28.5,
  "Age": 45
}
```

---

## 🐳 Dockerize the Application

### Build Docker Image

```bash
docker build -t diabetes-prediction-model .
```

### Run Docker Container

```bash
docker run -p 8000:8000 diabetes-prediction-model
```

---

## ☸ Deploy on Kubernetes

Make sure your Kubernetes cluster is running.

```bash
kubectl apply -f k8s-deploy.yml
```

Check deployment status:

```bash
kubectl get pods
kubectl get services
```

---

## 🎓 Who Is This For?

* Students learning **MLOps**
* Beginners in **FastAPI, Docker, or Kubernetes**
* Anyone wanting a **simple ML deployment example**
* Resume / portfolio projects for ML & DevOps roles

---

## 📌 Future Improvements

* Model versioning
* CI/CD pipeline
* Monitoring & logging
* Cloud deployment (AWS/GCP/Azure)

---

## 🙌 Credits

Inspired by community-driven MLOps learning projects.
Built for **learning, experimentation, and clarity**.

