# 🚀 DevOps Project: Scalable Kubernetes-Based Application

## 📌 Overview

This project demonstrates a **production-ready DevOps pipeline** by deploying a containerized web application on Kubernetes with monitoring, autoscaling, and CI/CD integration.

It showcases real-world DevOps and SRE practices including containerization, orchestration, observability, and scalability.

---

## 🧱 Tech Stack

* **Backend:** Python (Flask)
* **Containerization:** Docker
* **Orchestration:** Kubernetes (Minikube)
* **CI/CD:** GitHub Actions
* **Monitoring:** Prometheus + Grafana
* **Autoscaling:** Kubernetes HPA

---

## ⚙️ Architecture

User → Kubernetes Service → Pods (Flask App)
          ↓
      Monitoring (Prometheus + Grafana)

---

## 🚀 Features

* ✅ Containerized application using Docker
* ✅ Deployed on Kubernetes cluster (Minikube)
* ✅ Multi-replica deployment for high availability
* ✅ Horizontal Pod Autoscaling (HPA)
* ✅ Health check endpoint (`/health`)
* ✅ Monitoring with Prometheus & Grafana
* ✅ CI/CD pipeline using GitHub Actions

---

## 📂 Project Structure

```
devops-project/
│── app.py
│── requirements.txt
│── Dockerfile
│── docker-compose.yml
│── deployment.yaml
│── service.yaml
│── .github/workflows/deploy.yml
```

---

## 🛠️ Setup Instructions

### 1. Clone Repository

```
git clone <your-repo-url>
cd devops-project
```

### 2. Run Locally

```
pip install -r requirements.txt
python app.py
```

---

### 3. Docker Setup

```
docker build -t devops-project .
docker run -p 5000:5000 devops-project
```

---

### 4. Kubernetes Deployment

Start Minikube:

```
minikube start
```

Load image:

```
minikube image load devops-project
```

Apply configs:

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Access app:

```
minikube service devops-service
```

---

### 5. Monitoring Setup

Install Helm and run:

```
helm install monitoring prometheus-community/kube-prometheus-stack
```

Access Grafana:

```
kubectl port-forward svc/monitoring-grafana 3000:80
```

---

### 6. Autoscaling

```
kubectl autoscale deployment devops-app --cpu-percent=50 --min=2 --max=5
```

---

## 📊 Key Learnings

* Built and deployed containerized applications
* Managed Kubernetes workloads and scaling
* Implemented monitoring and observability
* Designed CI/CD pipelines
* Applied SRE principles (health checks, scaling, reliability)

---

## 🔮 Future Improvements

* Add Docker Hub integration
* Implement Terraform for infrastructure provisioning
* Add alerting with Alertmanager
* Deploy on cloud (AWS EKS / GKE)

---

## 👨‍💻 Author

Your Name: Hari R G
GitHub: https://github.com/HARIGNANASEKARAN/devops-project

---

## ⭐ Acknowledgment

This project is built as part of hands-on DevOps and SRE learning to simulate real-world production systems.
