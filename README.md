# 🚀 Dockerized Web Application – Deployment & CI/CD

A simple Dockerized static web application deployed step-by-step with manual AWS EC2 deployment and then automated using a CI/CD pipeline with GitHub Actions & Docker Hub.

---

## 📌 Project Overview

This project is divided into two tasks:

🔹 Task-2: Manual Docker Deployment (AWS EC2)  
Deploy a Dockerized web app manually on an EC2 instance using NGINX.

🔹 Task-3: CI/CD Automation  
Automate Docker image build & push using GitHub Actions and Docker Hub.

---

## 🧩 Task-2 – Manual Deployment on AWS EC2

### 🔧 What was done:
- Launched an Ubuntu EC2 instance
- Installed Docker
- Created a Dockerfile using NGINX
- Built a custom Docker image
- Ran container with proper port mapping

### 🌐 Port Mapping
Host Port → Container Port  
8080 → 80

### ✅ Verification
- Application accessed via browser
- Tested using curl

### 🔗 Live URL (Task-2)
http://13.127.142.69

---

## 🔁 Task-3 – CI/CD using GitHub Actions & Docker Hub

### 🎯 Goal
Automatically build and push Docker image on every push to the main branch.

### 🛠 Tools Used
- GitHub Actions
- Docker Hub
- Docker

### 📂 Workflow File
.github/workflows/docker-ci.yml

### ⚙️ CI/CD Pipeline Steps
1. Checkout repository code  
2. Login to Docker Hub using secrets:
   - DOCKER_USERNAME
   - DOCKER_PASSWORD  
3. Build Docker image  
4. Push image to Docker Hub  

### 🐳 Docker Image
sohu09/dockerized-web-app:latest

---

## ▶️ Run the Dockerized Web Application Locally

Steps:
- docker login -u sohu09  
  (Use Docker Hub access token as password)
- docker pull sohu09/dockerized-web-app:latest
- docker run -d -p 80:80 sohu09/dockerized-web-app:latest

### 🌍 Open in Browser
http://localhost

---

## 📦 GitHub Repository

Source code, Dockerfile, and CI/CD workflow:  
https://github.com/sohu9/docker-task2

---

## 🎓 Academic Info

Cloud Computing & DevOps – Task-2 & Task-3  
Student: Momin Shoaib Akhter ✅  

---

✨ This project demonstrates Docker fundamentals, AWS EC2 deployment, and CI/CD automation using GitHub Actions.
