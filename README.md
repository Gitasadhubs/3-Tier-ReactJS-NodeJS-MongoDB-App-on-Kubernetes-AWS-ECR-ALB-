
# #ThreeTierApp

## Overview


It’s a fully **containerized Three-Tier Web Application** with:

* **Frontend:** ReactJS
* **Backend:** NodeJS
* **Database:** MongoDB

The app is deployed on **AWS EKS** with **Docker containers stored in AWS ECR**, **Kubernetes Deployments & Services**, **Ingress routing**, and an **Application Load Balancer (ALB)**.

📌 **Connect with me:** [Asad Ashraf on LinkedIn](https://www.linkedin.com/in/asadkhan-dev)

---

## Architecture Diagram

![3-Tier App Architecture](A_UML-style_architecture_diagram_illustrates_a_thr.png)

**Diagram Legend:**

* Blue: AWS Layer (ALB & EKS)
* Yellow/Orange: Application Pods (Frontend & Backend)
* Green: Database Pod (MongoDB)
* Arrows: Traffic flow from Users → ALB → Ingress → Frontend/Backend → Database

---

## Repository Structure

```
repo/
│
├─ frontend/                 # ReactJS app
│   └─ Dockerfile
├─ backend/                  # NodeJS API
│   └─ Dockerfile
├─ mongodb/                  # MongoDB container
│   └─ Dockerfile
├─ k8s/                      # Kubernetes manifests
│   ├─ frontend-deployment.yaml
│   ├─ backend-deployment.yaml
│   ├─ mongo-deployment.yaml
│   ├─ ingress.yaml
│   └─ service.yaml
├─ A_UML-style_architecture_diagram_illustrates_a_thr.png  # Architecture diagram
└─ README.md
```

---

## Features

* **CI/CD Automation:** GitHub → Docker → AWS ECR → Kubernetes
* **Kubernetes Deployments:** Frontend, Backend, MongoDB
* **Ingress Routing:** Routes traffic from ALB to Frontend & Backend
* **Monitoring (Optional):** Prometheus & Grafana
* **GitOps (Optional):** ArgoCD integration

---

## Getting Started

1. **Clone repo:**

```bash
git clone <repo-url>
cd repo
```

2. **Build Docker images:**

```bash
docker build -t frontend ./frontend
docker build -t backend ./backend
docker build -t mongo ./mongodb
```

3. **Push to AWS ECR**

4. **Deploy Kubernetes manifests:**

```bash
kubectl create namespace workshop
kubectl apply -f k8s/
```

5. **Access app** via ALB URL

*(For full AWS EKS & Load Balancer setup, follow the detailed guide.)*

---

## Contribution

* Fork → Feature Branch → PR
* Add enhancements or fixes
* PRs merged = Eligible for rewards!

---

## Support

Open an issue in the repository for any help.

---

Happy Learning! 🚀
**— Asad Ashraf**
[LinkedIn](https://www.linkedin.com/in/asadkhan-dev)

---
