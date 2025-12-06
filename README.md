# docker-flask-app
## Overview
A simple Flask application containerized with Docker for easy deployment and reproducibility.

## Prerequisites
- Docker installed on your system
- Python 3.8
- Flask

## Quick Start

### 1. Build the Docker Image
```bash
docker build -t docker-flask-app .
```

### 2. Run the Container
```bash
docker run -p 5000:5000 docker-flask-app
```

### 3. Access the Application
Open your browser and navigate to `http://localhost:5000`

## Dockerfile
```dockerfile
FROM python:3.8
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python", "app.py"]
```

## Useful Docker Commands
```bash
# View running containers
docker ps

# Stop a container
docker stop <container_id>

# Remove a container
docker rm <container_id>

# View logs
docker logs <container_id>
```

## Project Structure
```
docker-flask-app/
├── app.py
├── requirements.txt
└── Dockerfile
```