# Dockerized Web Application – Deployment & CI/CD 🚀

## 📌 Overview
This project is a **Dockerized static web application** deployed in two phases:

- **Task‑2:** Manual Docker deployment on **AWS EC2** using NGINX.  
- **Task‑3:** CI/CD automation using **GitHub Actions** and **Docker Hub**.

---

## 🧩 Task‑2 – Manual Deployment (AWS EC2)

- Docker + NGINX setup on Ubuntu EC2.
- Custom image built from a Dockerfile.
- Port mapping configured (host `8080` → container `80`).
- Container verified via browser and `curl`.

**Live URL (Task‑2):** `http://13.127.142.69`

---

## 🔁 Task‑3 – CI/CD with GitHub Actions & Docker Hub

**Goal:** Automatically build and push a Docker image on every push to the `main` branch.

- Workflow file: `github/workflows/docker-ci.yml`
- Pipeline steps:
  - Checkout code
  - Login to Docker Hub (using `DOCKER_USERNAME` and `DOCKER_PASSWORD` secrets)
  - Build image: `sohu09/dockerized-web-app:latest`
  - Push image to Docker Hub

**Docker Hub Image:** `sohu09/dockerized-web-app:latest`

---

## ▶️ Run the Dockerized Web App

```bash
docker login -u sohu09              # use Docker Hub access token as password
docker pull sohu09/dockerized-web-app:latest
docker run -d -p 80:80 sohu09/dockerized-web-app:latest
Then open:

text
http://localhost
📦 Repository
Source code, Dockerfile, and CI workflow:

text
https://github.com/sohu9/docker-task2
Cloud Computing & DevOps – Task‑2 & Task‑3
Student: Momin Shoaib Akhter ✅
