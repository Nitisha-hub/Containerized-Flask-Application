# 🚀 Containerized Flask Application
        
## 📌 Overview
This project demonstrates how to containerize a Python Flask application using Docker and deploy it on AWS using Amazon ECR and Amazon ECS. The application is packaged into a Docker container, stored in Amazon Elastic Container Registry (ECR), and deployed as a scalable containerized service using Amazon ECS.

---

## 🎯 Purpose
To deploy and manage a Flask web application in containers using Docker and AWS container services.

---

## 🧰 AWS Services Used
- Amazon ECR (Elastic Container Registry)
- Amazon ECS (Elastic Container Service)
- Amazon EC2
- Docker
- Python Flask

---

# ⚙️ Architecture Workflow

```text
Flask Application
      │
      ▼
Docker Container
      │
      ▼
Amazon ECR Repository
      │
      ▼
Amazon ECS Cluster
      │
      ▼
Containerized Flask Application Running on AWS
```

---

# 📌 Project Overview
This project shows how to build, containerize, push, and deploy a Flask application using Docker and AWS container services. It demonstrates modern cloud-native deployment practices using containers.

---

# 🚀 Features
- Dockerized Flask Application
- Container Image Management using Amazon ECR
- Container Deployment using Amazon ECS
- Scalable Containerized Architecture
- Cloud-native Application Deployment

---

# 🔄 How It Works

1. Create Flask application  
2. Build Docker image  
3. Push Docker image to Amazon ECR  
4. Create ECS Cluster and Task Definition  
5. Deploy containerized application on Amazon ECS  
6. Access Flask application through ECS service  

---

# 🛠️ Step-by-Step Setup

## 1️⃣ Create Flask Application

Example:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Flask App Running on ECS"

if __name__ == '__main__':
    app.run(host='0.0.0.0')
```

---

## 2️⃣ Create Dockerfile

```dockerfile
FROM python:3.9

WORKDIR /app

COPY . /app

RUN pip install flask

CMD ["python", "app.py"]
```

---

## 3️⃣ Build Docker Image

```bash
docker build -t flask-app .
```

---

## 4️⃣ Create Amazon ECR Repository

```bash
aws ecr create-repository --repository-name flask-app
```

---

## 5️⃣ Push Docker Image to ECR

```bash
docker tag flask-app:latest <account-id>.dkr.ecr.<region>.amazonaws.com/flask-app

docker push <account-id>.dkr.ecr.<region>.amazonaws.com/flask-app
```

---

## 6️⃣ Create ECS Cluster
- Open Amazon ECS
- Create Cluster
- Select EC2 or Fargate launch type

---

## 7️⃣ Create Task Definition
- Add container details
- Use ECR image URI
- Configure CPU and memory

---

## 8️⃣ Deploy ECS Service
- Create ECS Service
- Attach Task Definition
- Run desired number of tasks

---

# 📸 Screenshots

## 🐳 Docker Container Build
(Add Docker build screenshot)

---

## 📦 Amazon ECR Repository
(Add ECR screenshot)

---

## ⚙️ ECS Cluster
(Add ECS cluster screenshot)

---

## 🚀 ECS Service Running
(Add ECS service screenshot)

---

## 🌐 Flask Application Output
(Add application output screenshot)

---

# 📂 Project Structure

```text
containerized-flask-application/
│── screenshots/
│   ├── docker_build.png
│   ├── ecr_repository.png
│   ├── ecs_cluster.png
│   ├── ecs_service.png
│   └── application_output.png
│
│── app.py
│── Dockerfile
│── requirements.txt
│── README.md
```

---

# 💡 Key Features
- Containerized Deployment
- Scalable Architecture
- Docker-based Packaging
- Cloud-native Deployment
- Simplified Application Management

---

# 🧠 Learning Outcomes
- Understanding Docker Containers
- Working with Amazon ECR
- Deploying Applications on Amazon ECS
- Container Orchestration Basics
- Cloud-native Application Deployment

---

# 🔮 Future Improvements
- Add Application Load Balancer
- Use ECS Fargate
- Add CI/CD Pipeline using GitHub Actions
- Implement Auto Scaling
- Add CloudWatch Monitoring

---

# 👩‍💻 Author
**Nitisha Mali**

GitHub: [Nitisha-hub](https://github.com/Nitisha-hub)
