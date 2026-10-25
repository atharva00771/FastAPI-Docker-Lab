# 🚀 FastAPI Docker Basics 🐳

<div align="center">

<img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" width="120" alt="FastAPI Logo"/>

# ⚡ FastAPI + Docker

### 🐍 Python API Development & 🐳 Containerization

Build, run, and containerize a REST API using FastAPI, Uvicorn, and Docker.

<br/>

<img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
<img src="https://img.shields.io/badge/Uvicorn-4051B5?style=for-the-badge&logo=python&logoColor=white" alt="Uvicorn"/>

<br/><br/>

<img src="https://img.shields.io/badge/Beginner--Friendly-00C853?style=flat-square" alt="Beginner Friendly"/>
<img src="https://img.shields.io/badge/REST-API-orange?style=flat-square" alt="REST API"/>
<img src="https://img.shields.io/badge/Containerized-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Containerized"/>

</div>

---

## 📌 Project Overview

**FastAPI Docker Basics** is a beginner-friendly project that demonstrates how to build a REST API with Python and FastAPI and run it inside a Docker container.

The project introduces API development, application dependencies, Docker images, containers, and port mapping through a simple hands-on workflow.

## 🎯 Project Objectives

- Understand the fundamentals of FastAPI.
- Build and run a REST API using Python.
- Learn how Uvicorn runs an ASGI application.
- Create a Docker image for a Python application.
- Run the application inside a Docker container.
- Test API endpoints using a browser.
- Explore automatic API documentation.
- Understand the basics of application containerization.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.12 | Application development |
| FastAPI | REST API framework |
| Uvicorn | ASGI application server |
| Docker | Application containerization |
| Ubuntu / WSL | Command-line environment |
| Swagger UI | Interactive API testing |

## ✨ Features

- ⚡ Lightweight API built with FastAPI.
- 🐍 Python-based backend development.
- 🐳 Docker image creation and container execution.
- 📚 Interactive Swagger API documentation.
- 🔗 HTTP endpoint testing.
- 💻 Beginner-friendly command-line workflow.
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

*Note: The structure above is the recommended layout. Update it if your actual repository uses a different structure.*

## ⚙️ Prerequisites

Before getting started, make sure you have:

- Python 3.12
- Docker installed and running
- Ubuntu / WSL or another terminal
- Git (optional)

Verify your installations:

```bash
python3 --version
docker --version
docker info
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/atharva00771/fastapi-docker-basics.git
cd fastapi-docker-basics
```

### 2. Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

### 3. Run the API Locally

```bash
uvicorn app.main:app --reload
```

Open these URLs in your browser:

| URL | Purpose |
|---|---|
| http://127.0.0.1:8000/ | Root endpoint, if implemented |
| http://127.0.0.1:8000/docs | Interactive Swagger UI |
| http://127.0.0.1:8000/redoc | Alternative API documentation |
| http://127.0.0.1:8000/openapi.json | OpenAPI schema |

Stop the local server using `Ctrl + C`.

## 🐳 Docker Setup

### 4. Build the Docker Image

Run the command from the project root directory, where the `Dockerfile` is located.

```bash
docker build -t fastapi-docker-basics .
```

**What this does:** Builds a Docker image containing your application and its required dependencies.

### 5. Run the Docker Container

```bash
docker run -d --name fastapi-container -p 8000:8000 fastapi-docker-basics
```

**What this does:**

- `-d` runs the container in the background.
- `--name` assigns a name to the container.
- `-p 8000:8000` maps host port 8000 to container port 8000.
- The final argument specifies the Docker image.

**Important:** The FastAPI application must listen on `0.0.0.0:8000` inside the container. For example, your Docker startup command can use:

```bash
uvicorn app.main:app --host 0.0.0.0 --port 8000
```

### 6. Test the Containerized API

Open:

**http://127.0.0.1:8000/docs**

If the container starts successfully and the application is configured correctly, you can access the interactive API documentation.

### 7. Useful Docker Commands

Check running containers:

```bash
docker ps
```

View application logs:

```bash
docker logs fastapi-container
```

Follow logs continuously:

```bash
docker logs -f fastapi-container
```

Stop the container:

```bash
docker stop fastapi-container
```

Restart the container:

```bash
docker start fastapi-container
```

Remove the stopped container:

```bash
docker rm fastapi-container
```

Remove the Docker image:

```bash
docker rmi fastapi-docker-basics
```

*Note: Remove the container before removing its image. The image cannot be removed while a container is using it.*

## 🔌 API Endpoints

The available application endpoints depend on the routes defined in `app/main.py`.

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/` | Root endpoint, if implemented |
| GET | `/docs` | Interactive Swagger UI |
| GET | `/redoc` | Alternative API documentation |
| GET | `/openapi.json` | OpenAPI schema |

FastAPI provides the documentation endpoints automatically unless they are disabled or customized.

## 🧠 Key Concepts Learned

- **FastAPI:** A Python framework for building APIs.
- **REST API:** Enables applications to communicate over HTTP.
- **Uvicorn:** Runs the FastAPI application as an ASGI server.
- **Docker Image:** A packaged template used to create containers.
- **Docker Container:** An isolated environment running an application.
- **Port Mapping:** Connects a host port to a container port.
- **Containerization:** Packages an application and dependencies for consistent execution.
- **Swagger UI:** Allows users to explore and test API endpoints interactively.

## 🔮 Future Improvements

- [ ] Implement CRUD operations.
- [ ] Integrate a database such as MySQL or PostgreSQL.
- [ ] Add request validation and error handling.
- [ ] Use environment variables for configuration.
- [ ] Add Docker Compose.
- [ ] Write automated API tests using Pytest.
- [ ] Add a CI/CD workflow using GitHub Actions.
- [ ] Deploy the containerized API to AWS.

## 👨‍💻 Author

**Atharva Avhad**

B.Tech Artificial Intelligence & Data Science Student | Aspiring Data Analyst | AWS Cloud Enthusiast

- GitHub: [@atharva00771](https://github.com/atharva00771)
- Project Repository: [FastAPI Docker Basics](https://github.com/atharva00771/fastapi-docker-basics)

---

<div align="center">

### ⭐ Learn • Build • Containerize • Deploy

If you find this project useful, consider giving the repository a star!

</div>
