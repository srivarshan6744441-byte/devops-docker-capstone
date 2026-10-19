# DevOps Docker Capstone Project

## Project Overview
This project demonstrates website deployment and version management using Docker and NGINX.

## Technologies Used
- HTML
- CSS
- Docker
- NGINX Alpine
- Git and GitHub

## Project Structure
```text
devops-capstone/
├── Dockerfile
└── site/
    └── index.html
```

## Dockerfile
The Dockerfile uses the lightweight `nginx:alpine` image and copies the website files into the NGINX web root.

## Build Docker Images
```powershell
docker build -t website-demo:v1 .
docker build -t website-demo:v2 .
```

## Run Both Versions
```powershell
docker run -d --name website-v1 -p 8080:80 website-demo:v1
docker run -d --name website-v2 -p 8081:80 website-demo:v2
```

## Access the Websites
- Version 1: http://localhost:8080
- Version 2: http://localhost:8081

Both versions can run simultaneously using separate host ports.

## Verification Commands
```powershell
docker ps
docker images
docker history website-demo:v1
docker history website-demo:v2
```

## Result
Two versions of the website were built as Docker images and deployed simultaneously in separate containers using NGINX.

## Repository
https://github.com/srivarshan6744441-byte/devops-docker-capstone
