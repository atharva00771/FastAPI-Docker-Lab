# 🚀 FastAPI Docker Basics 🐳

<div align="center">

<img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" width="130" alt="FastAPI Logo"/>

# ⚡ FastAPI + Docker

### 🐍 Python API Development | 🐳 Containerization | ☁️ Cloud Ready

**Build • Run • Containerize • Deploy**

A beginner-friendly project to build a REST API using FastAPI and run it inside a Docker container.

<br/>

<img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Uvicorn-4051B5?style=for-the-badge&logo=python&logoColor=white"/>

<br/><br/>

<img src="https://img.shields.io/badge/Project-Beginner%20Friendly-00C853?style=flat-square"/>
<img src="https://img.shields.io/badge/API-REST-orange?style=flat-square"/>
<img src="https://img.shields.io/badge/Platform-Ubuntu%20%7C%20WSL-E95420?style=flat-square&logo=ubuntu&logoColor=white"/>

<br/><br/>

<a href="https://github.com/atharva00771">
<img src="https://img.shields.io/badge/GitHub-Atharva%20Avhad-181717?style=for-the-badge&logo=github"/>
</a>

</div>

---

## 🌈 About The Project

**FastAPI Docker Basics** is a hands-on project that demonstrates how to create a REST API using Python and FastAPI and containerize it using Docker.

This project helps beginners understand API development, application dependencies, Docker images, containers, and port mapping through practical implementation.

## 🎯 Project Objectives

- 🐍 Build a REST API using Python and FastAPI.
- ⚡ Run the application using Uvicorn.
- 🐳 Create a Docker image.
- 📦 Run the API inside a Docker container.
- 🔗 Understand port mapping.
- 📚 Explore automatic API documentation.
- ☁️ Learn the basics of containerized applications.

## 🛠️ Tech Stack

| Technology | Purpose |
|:---:|---|
| 🐍 Python 3.12 | Application development |
| ⚡ FastAPI | REST API framework |
| 🚀 Uvicorn | ASGI application server |
| 🐳 Docker | Containerization |
| 🐧 Ubuntu / WSL | Development environment |
| 📖 Swagger UI | Interactive API testing |

## ✨ Key Features

- ⚡ Lightweight API development with FastAPI.
- 🐍 Python-based backend application.
- 🐳 Docker image creation and container execution.
- 📚 Interactive Swagger documentation.
- 🔗 HTTP endpoint testing.
- 💻 Beginner-friendly commands.
- ☁️ Foundation for future cloud deployment.

## 📂 Project Structure

```text
fastapi-docker-basics/
│
├── app/
│   └── main.py
│
├── requirements.txt
├── Dockerfile
├── .dockerignore
└── README.md
```

## ⚙️ Prerequisites

Before starting, install:

- Python 3.12
- Docker Desktop or Docker Engine
- Ubuntu / WSL or another terminal

Verify your installations:

```bash
python3 --version
docker --version
docker info
```

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/atharva00771/fastapi-docker-basics.git
cd fastapi-docker-basics
```

### 2️⃣ Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the API Locally

```bash
uvicorn app.main:app --reload
```

Open the API documentation:

🔗 **Swagger UI:** http://127.0.0.1:8000/docs

🔗 **ReDoc:** http://127.0.0.1:8000/redoc

Stop the server using `Ctrl + C`.

## 🐳 Docker Deployment

### 4
