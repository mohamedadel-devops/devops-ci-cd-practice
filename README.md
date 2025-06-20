# DevOps CI/CD Practice Project

This project demonstrates a full CI/CD pipeline using **Docker**, **GitHub Actions**, and **AWS EC2**.  
A Python web app is containerized and automatically built, tested, and deployed to the cloud.

---

## 🚀 Project Overview

- **Language:** Python 3
- **Framework:** Flask
- **CI Tool:** GitHub Actions
- **Containerization:** Docker
- **Deployment Target:** AWS EC2 (Ubuntu 22.04)
- **Image Registry:** Docker Hub (`mohammedrs/ci-test-image`)

---

## 🔁 CI/CD Pipeline

Every push to the `main` branch triggers the following:

1. **Checkout code**
2. **Build Docker image**
3. **Login to Docker Hub**
4. **Push image to Docker Hub**
5. ✅ *(Optional step coming soon: Run tests before push)*

See [`.github/workflows/main.yml`](.github/workflows/main.yml)

---

## 📦 Docker Hub

The image is automatically built and available publicly here:  
👉 https://hub.docker.com/r/mohammedrs/ci-test-image

---

## 🌐 Deployment

Deployed to:  
**AWS EC2** – Public IP: [`http://34.219.157.83:5000`](http://34.219.157.83:5000)

---

## 🛠 How to Run Locally

```bash
# Clone the repo
git clone https://github.com/mohamedadel-devops/devops-ci-cd-practice.git
cd devops-ci-cd-practice

# Build the image
docker build -t local-image .

# Run it
docker run -p 5000:5000 local-image
📄 Files
Dockerfile — builds the app image

app.py — simple Flask app

requirements.txt — Python dependencies

.github/workflows/main.yml — GitHub Actions CI pipeline

✍️ Author
Mohamed Adel Asar
💼 LinkedIn
🌐 Portfolio
