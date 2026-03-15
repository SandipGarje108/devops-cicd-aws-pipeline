# DevOps CI/CD Pipeline with Docker and AWS

This project demonstrates a complete CI/CD pipeline that automatically builds and deploys a containerized application to AWS EC2.

## Architecture

Developer → GitHub → GitHub Actions → Docker Hub → AWS EC2

## Tech Stack

- Python (Flask)
- Docker
- GitHub Actions
- Docker Hub
- AWS EC2

## CI/CD Workflow

1. Developer pushes code to GitHub
2. GitHub Actions builds Docker image
3. Image is pushed to Docker Hub
4. GitHub Actions connects to EC2 via SSH
5. EC2 pulls new image and restarts container automatically

## Deployment

Application runs on AWS EC2:

http://<EC2_PUBLIC_IP>:5000

##Architecture Diagram

+-------------+
| Developer   |
+-------------+
       |
       v
+-------------+
|  GitHub     |
+-------------+
       |
       v
+-------------------+
| GitHub Actions CI |
+-------------------+
       |
       v
+-------------+
| Docker Hub  |
+-------------+
       |
       v
+-------------+
| AWS EC2     |
| Docker Run  |
+-------------+
       |
       v
+-------------+
| Flask App   |
+-------------+
