# 🚀 DevOps Full Stack Deployment Project

This project demonstrates the end-to-end deployment of a Python web application using modern DevOps practices including containerization, reverse proxy, and CI/CD automation.

---

## 📌 Project Overview

This project includes:

- Python Web Application
- Gunicorn Application Server
- Nginx Reverse Proxy
- Docker Containerization
- Docker Compose Multi-Container Setup
- CI/CD Pipeline using GitHub Actions
- Production-ready deployment structure

---

## 🏗️ Architecture

User → Nginx → Gunicorn → Python App

---

## ⚙️ Prerequisites

Make sure the following tools are installed on your system:

- Git
- Docker
- Docker Compose
- Python 3.x
- Linux / macOS / Windows (WSL recommended)

---

## 📂 Project Setup (Local Development)

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/project-name.git
cd project-name
```

---

### 2️⃣ Create Virtual Environment

#### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Run Application Locally

```bash
python app.py
```

Application will be available at:

```
http://localhost:8000
```

---

## 🐳 Docker Setup

### 🔹 Build Docker Image

```bash
docker build -t my-python-app .
```

---

### 🔹 Run Docker Container

```bash
docker run -d -p 8000:8000 my-python-app
```

---

## 🐳 Docker Compose Setup

Start all services:

```bash
docker-compose up -d
```

Stop services:

```bash
docker-compose down
```

---

## 🌐 Production Setup (Nginx + Gunicorn)

### Install Nginx (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install nginx -y
```

---

### Run Gunicorn Server

```bash
gunicorn app:app --bind 0.0.0.0:8000
```

---

### Restart Nginx

```bash
sudo systemctl restart nginx
```

---

## 🔄 CI/CD Pipeline

This project uses **GitHub Actions** for Continuous Integration and Deployment.

### Pipeline Workflow

On every push:

- Build Docker Image
- Run Tests
- Deploy Application

Workflow file location:

```
.github/workflows/deploy.yml
```

---

## 🌍 Access Application

### Local

```
http://localhost:8000
```

### Cloud (Example: AWS EC2)

```
http://<EC2-Public-IP>
```

---

## 📁 Project Structure

```
project/
│
├── app/
├── Dockerfile
├── docker-compose.yml
├── nginx/
├── requirements.txt
├── app.py
└── README.md
```

---

## ✨ Features

- Fully Containerized Application
- Reverse Proxy with Nginx
- Production-ready Deployment
- Automated CI/CD Pipeline
- Scalable Architecture

---

## 🛠️ Troubleshooting

### Port Already in Use

Change port mapping:

```bash
docker run -p 8080:8000 my-python-app
```

---

### Docker Not Running

Start Docker service:

```bash
sudo systemctl start docker
```

---

### Permission Denied

Use sudo:

```bash
sudo docker-compose up -d
```

---

## 👨‍💻 Author

Developed as part of a DevOps learning project demonstrating real-world deployment practices.

---

## 📜 License

This project is for educational purposes.
