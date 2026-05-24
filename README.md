# Docker Fundamentals - Holberton School

![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Holberton-School-red?style=for-the-badge)

## 📌 Overview

This repository contains my Docker projects, exercises, and hands-on activities completed as part of the Docker module in the Holberton School curriculum.

The objective of this module is to understand:

- Containerization concepts
- Docker architecture
- Image creation and management
- Docker containers lifecycle
- Networking and volumes
- Dockerfiles
- Docker Compose
- Development environment isolation
- Best practices in containerized applications

This repository serves as both:

- A learning archive
- A technical reference
- A portfolio of Docker fundamentals and DevOps practices

---

# 🐳 What is Docker?

Docker is a platform used to develop, ship, and run applications inside lightweight, portable containers.

Containers allow applications to run consistently across different environments by packaging:

- Application source code
- Runtime
- Dependencies
- Libraries
- System tools
- Configuration files

Unlike virtual machines, Docker containers share the host operating system kernel, making them:

- Faster
- More lightweight
- More portable
- Easier to deploy

---

# 📚 Learning Objectives

By completing this module, I learned how to:

## Core Concepts

- Understand containerization
- Differentiate containers vs virtual machines
- Understand Docker Engine architecture
- Work with Docker CLI commands

## Docker Images

- Pull images from Docker Hub
- Build custom Docker images
- Understand image layers
- Optimize Docker image size

## Containers

- Create and manage containers
- Run containers interactively and detached
- Execute commands inside containers
- Inspect running containers
- Remove unused resources

## Dockerfile

- Create Dockerfiles
- Use Docker instructions properly
- Optimize image builds
- Configure environments
- Automate application setup

## Volumes & Networking

- Persist data using volumes
- Configure bridge networks
- Connect multiple containers
- Expose application ports

## Docker Compose

- Define multi-container applications
- Manage services efficiently
- Simplify development environments

---

# 🛠 Technologies Used

| Technology     | Purpose                       |
| -------------- | ----------------------------- |
| Docker         | Containerization Platform     |
| Docker Compose | Multi-container Orchestration |
| Ubuntu/Linux   | Development Environment       |
| Bash           | Shell Scripting               |
| Git & GitHub   | Version Control               |

---

# 📂 Repository Structure

```bash
.
├── 0x00-docker_basics/
│   ├── Dockerfile
│   ├── README.md
│   └── scripts/
│
├── 0x01-docker_images/
│   ├── Dockerfile
│   ├── app/
│   └── README.md
│
├── 0x02-docker_compose/
│   ├── docker-compose.yml
│   ├── services/
│   └── README.md
│
└── README.md
```

---

# 🚀 Common Docker Commands

## Docker Version

```bash
docker --version
```

## Pull an Image

```bash
docker pull ubuntu
```

## List Images

```bash
docker images
```

## Run a Container

```bash
docker run ubuntu
```

## Run Interactive Container

```bash
docker run -it ubuntu bash
```

## Run Detached Container

```bash
docker run -d nginx
```

## List Running Containers

```bash
docker ps
```

## List All Containers

```bash
docker ps -a
```

## Stop Container

```bash
docker stop <container_id>
```

## Remove Container

```bash
docker rm <container_id>
```

## Remove Image

```bash
docker rmi <image_id>
```

---

# 🧱 Sample Dockerfile

```Dockerfile
FROM ubuntu:22.04

WORKDIR /app

COPY . .

RUN apt-get update && apt-get install -y python3

CMD ["python3", "app.py"]
```

---

# ⚙️ Build and Run

## Build Docker Image

```bash
docker build -t my-image .
```

## Run Built Image

```bash
docker run my-image
```

## Port Mapping

```bash
docker run -p 8080:80 nginx
```

---

# 🔄 Docker Compose Example

```yaml
version: '3'

services:
  web:
    build: .
    ports:
      - '5000:5000'

  database:
    image: mysql:8
    environment:
      MYSQL_ROOT_PASSWORD: root
```

## Run Compose

```bash
docker compose up
```

## Stop Compose

```bash
docker compose down
```

---

# 🧠 Key Concepts Learned

## Containers vs Virtual Machines

| Containers               | Virtual Machines      |
| ------------------------ | --------------------- |
| Lightweight              | Heavyweight           |
| Fast startup             | Slower startup        |
| Share host kernel        | Full OS required      |
| Smaller size             | Larger size           |
| Efficient resource usage | Higher resource usage |

---

# 🔥 Important Docker Concepts

## Image

A read-only template used to create containers.

## Container

A runnable instance of a Docker image.

## Dockerfile

A script containing instructions to build Docker images.

## Volume

Persistent storage mechanism for containers.

## Network

Allows containers to communicate with each other.

## Docker Hub

Cloud-based registry for Docker images.

---

# 🧪 Example Workflow

```bash
# Build image
docker build -t sample-app .

# Run container
docker run -p 3000:3000 sample-app

# Check running containers
docker ps

# Stop container
docker stop <container_id>
```

---

# 📈 Skills Developed

Through this module, I improved my skills in:

- Linux command line
- DevOps fundamentals
- Environment setup
- Application deployment
- Infrastructure basics
- Backend development workflows
- Debugging containerized applications
- Software portability

---

# 🎯 Real-World Relevance

Docker is widely used in:

- Cloud computing
- CI/CD pipelines
- Software deployment
- Microservices architecture
- Backend development
- DevOps engineering
- Kubernetes orchestration
- Scalable web applications

Learning Docker is an essential step toward modern software engineering and DevOps practices.

---

# 📖 Resources

## Official Documentation

- Docker Documentation
- Docker Hub
- Docker Compose Documentation

## Recommended Learning

- Linux fundamentals
- Networking basics
- DevOps principles
- CI/CD workflows
- Kubernetes fundamentals

---

# 👨‍💻 Author

**Patrick Macabulos**

Holberton School Student

Focused on:

- Full Stack Development
- Backend Engineering
- DevOps
- Cloud Technologies

---

# ⭐ Notes

This repository is part of my continuous learning journey in software engineering.

Each project demonstrates practical implementation of Docker concepts learned throughout the Holberton curriculum.

Future improvements may include:

- Kubernetes integration
- CI/CD pipelines
- Production-ready deployments
- Multi-stage Docker builds
- Advanced container orchestration

---

# 📜 License

This project is for educational purposes under the Holberton School curriculum.
