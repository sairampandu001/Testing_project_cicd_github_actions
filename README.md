# 🚀 CI/CD Pipeline using GitHub Actions, Docker & AWS EC2

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline where a static web application is containerized using Docker and automatically deployed to an AWS EC2 instance using GitHub Actions.

---

## 🛠️ Tech Stack

* GitHub Actions (CI/CD)
* Docker
* AWS EC2
* Nginx
* Linux

---

## ⚙️ Workflow Explanation

### 1️⃣ Code Push

* Developer pushes code to GitHub (main branch)

### 2️⃣ CI Pipeline (GitHub Actions)

* Checkout code
* Login to Docker Hub
* Build Docker image
* Push image to Docker Hub

### 3️⃣ CD Pipeline (Deployment)

* SSH into EC2 instance
* Pull latest Docker image
* Stop old container
* Remove old container
* Run new container

---

## 📂 Project Structure

```
.
├── .github/workflows/cicd.yml
├── Dockerfile
├── index.html
```

---

## 🐳 Dockerfile

```Dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html
```

---

## ⚡ GitHub Actions Workflow

* Automated CI/CD using GitHub Actions
* Uses secrets for secure authentication:

  * DOCKER_USERNAME
  * DOCKER_PASSWORD
  * EC2_HOST
  * PRIVATE_KEY

---

## 🔐 Security Best Practices

* Secrets stored in GitHub Secrets
* No hardcoded credentials
* SSH key-based authentication used

---

## 🌐 Deployment Output

* Application is deployed on AWS EC2
* Accessible via public IP on port 80

---

## 🚧 Challenges Faced

* SSH connection timeout issue (fixed via Security Group)
* YAML syntax errors
* Docker authentication issues

---

## 🎯 Key Learnings

* End-to-end CI/CD pipeline setup
* Docker image lifecycle management
* GitHub Actions automation
* Real-world troubleshooting

---

## 👨‍💻 Author

Sairam Pandu

---

## ⭐ Conclusion

This project demonstrates real-world DevOps practices including automation, containerization, and cloud deployment.
