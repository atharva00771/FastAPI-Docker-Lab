# 🚀 FastAPI Docker Basics 🐳

<div align="center">

<img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" width="120">

# ⚡ FastAPI + Docker

### 🐍 Python API Development & 🐳 Containerization

<br>

<img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
<img src="https://img.shields.io/badge/Uvicorn-000000?style=for-the-badge&logo=python&logoColor=white">

<br><br>

<img src="https://img.shields.io/badge/Beginner--Friendly-00C853?style=flat-square">
<img src="https://img.shields.io/badge/API-REST-orange?style=flat-square">
<img src="https://img.shields.io/badge/Containerized-2496ED?style=flat-square">

</div>

---

## 📌 About This Project

This project demonstrates how to create a simple **FastAPI application** and run it inside a **Docker container**.

It covers the basic workflow of:

* 🐍 Creating a FastAPI application
* 📦 Managing Python dependencies
* 🐳 Creating a Docker image
* 🚀 Running FastAPI inside a container
* 🔌 Exposing the application through a port
* ⚡ Running the API using Uvicorn

---

## 🛠️ Technologies Used

| Technology          | Purpose               |
| ------------------- | --------------------- |
| 🐍 Python 3.12      | Programming Language  |
| ⚡ FastAPI           | API Framework         |
| 🚀 Uvicorn          | ASGI Server           |
| 🐳 Docker           | Containerization      |
| 📄 requirements.txt | Dependency Management |

---

## 📂 Project Structure

```text
fastapi-docker-basics/
│
├── main.py
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## 🐍 FastAPI Application

The `main.py` file contains the basic FastAPI application.

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "FastAPI is running!"}
```

---

## 📦 requirements.txt

```text
fastapi
uvicorn
```

---

## 🐳 Dockerfile

```dockerfile
FROM python:3.12

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```
