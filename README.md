# 🚀 FastAPI Docker Basics 🐳

<div align="center">

<img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" width="120" alt="FastAPI Logo">

# ⚡ FastAPI + Docker

### 🐍 Python API Development & 🐳 Containerization

Building and running a REST API using FastAPI, Uvicorn, and Docker.

<br>

<img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Uvicorn-000000?style=for-the-badge&logo=python&logoColor=white" alt="Uvicorn">

<br><br>

<img src="https://img.shields.io/badge/Beginner--Friendly-00C853?style=flat-square" alt="Beginner Friendly">
<img src="https://img.shields.io/badge/API-REST-orange?style=flat-square" alt="REST API">
<img src="https://img.shields.io/badge/Containerized-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Containerized">

</div>

---

## 📌 Project Overview

This project demonstrates how to build a simple REST API using **FastAPI** and run it inside a **Docker container**.

It is designed for beginners who want to understand Python API development, containerization, and the fundamentals of deploying applications in a consistent environment.

## 🎯 Objectives

- Learn the basics of FastAPI.
- Create and run a REST API.
- Understand the role of Uvicorn as an ASGI server.
- Build a Docker image for a Python application.
- Run the application inside a Docker container.
- Access API endpoints through a web browser.
- Explore interactive API documentation.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.12 | Programming language |
| FastAPI | Building REST APIs |
| Uvicorn | Running the API server |
| Docker | Containerizing the application |
| Ubuntu / WSL | Command-line environment |

## ✨ Features

- ⚡ Lightweight API built with FastAPI.
- 🐍 Python-based application.
- 🐳 Docker image and container workflow.
- 📚 Interactive API documentation.
- 🔗 REST API endpoint testing.
- 💻 Beginner-friendly command-line workflow.

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

> Note: This structure represents the recommended layout. Adjust it to match your actual project files.

## ⚙️ Prerequisites

Make sure you have the following installed:

- Python 3.12
- Docker
- Ubuntu / WSL or another terminal
- Git (optional)

Check the installations:

```bash
python3 --version
docker --version
```

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/atharva00771/fastapi-docker-basics.git
```

```bash
cd fastapi-docker-basics
```

### 2️⃣ Install Dependencies

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the API Locally

```bash
uvicorn app.main:app --reload
```

Open the following URLs in your browser:

- API root: http://127.0.0.1:8000/
- Interactive Swagger documentation: http://127.0.0.1:8000/docs
- Alternative API documentation: http://127.0.0.1:8000/redoc

Stop the server by pressing `Ctrl + C`.

## 🐳 Docker Setup

### 4️⃣ Build the Docker Image

Run this command from the project root, where the Dockerfile is located:

```bash
docker build -t fastapi-docker-basics .
```

### 5️⃣ Run the Docker Container

```bash
docker run -d --name fastapi-container -p 8000:8000 fastapi-docker-basics
```

### 6️⃣ Test the Containerized API

Open:

http://127.0.0.1:8000/docs

Your API should be accessible through the published port if the application is configured to listen on `0.0.0.0:8000` inside the container.

### 7️⃣ Useful Docker Commands

Check running containers:

```bash
docker ps
```

View container logs:

```bash
docker logs fastapi-container
```

Stop the container:

```bash
docker stop fastapi-container
```

Remove the container:

```bash
docker rm fastapi-container
```

Remove the image:

```bash
docker rmi fastapi-docker-basics
```

## 🔌 API Endpoints

The exact endpoints depend on your `app/main.py` implementation.

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/` | Root endpoint, if implemented |
| GET | `/docs` | Interactive Swagger UI |
| GET | `/redoc` | Alternative API documentation |
| GET | `/openapi.json` | OpenAPI schema |

The documentation endpoints are provided by FastAPI by default unless they have been disabled or customized.

## 🧠 Key Concepts Learned

- **FastAPI:** Framework for building APIs with Python.
- **REST API:** An interface that allows applications to communicate over HTTP.
- **Uvicorn:** ASGI server used to run the FastAPI application.
- **Docker Image:** Packaged application environment used to create containers.
- **Docker Container:** A running instance of a Docker image.
- **Port Mapping:** Connects a host port to a container port.
- **Containerization:** Packages an application and its dependencies for consistent execution.

## 🔮 Future Improvements

- [ ] Add CRUD operations.
- [ ] Integrate a database.
- [ ] Add request validation and error handling.
- [ ] Add environment variables.
- [ ] Add Docker Compose.
- [ ] Add automated API tests using Pytest.
- [ ] Deploy the containerized API to AWS.

## 👨‍💻 Author

**Atharva Avhad**

B.Tech Artificial Intelligence & Data Science Student | Aspiring Data Analyst | AWS Cloud Enthusiast

- GitHub: [@atharva00771](https://github.com/atharva00771)

---

<div align="center">

### ⭐ If you find this project useful, consider giving it a star!

**Learn • Build • Containerize • Deploy**

</div>
