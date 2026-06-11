# Restaurant QR Menu System - DevOps Project

## Overview

A full-stack restaurant management and QR menu application deployed on Kubernetes with a complete DevOps pipeline.

The project demonstrates containerization, CI/CD, Kubernetes orchestration, monitoring, and cloud-native deployment practices.

---

## Tech Stack

### Frontend

* React.js
* Vite
* JavaScript

### Backend

* Node.js
* Express.js

### Database

* MongoDB

### DevOps & Infrastructure

* Docker
* Docker Compose
* GitHub Actions
* Docker Hub
* Kubernetes (Minikube)
* Ingress NGINX
* Helm
* Prometheus
* Grafana

---

## Features

### Customer Features

* Browse restaurant menu
* View categories
* View menu item details
* Place orders

### Admin Features

* Manage menu items
* Manage tables
* Manage orders
* Upload menu images

### DevOps Features

* Containerized frontend and backend
* CI pipeline using GitHub Actions
* Kubernetes deployment
* ConfigMaps and Secrets
* Ingress-based routing
* Monitoring using Prometheus and Grafana

---

## Project Architecture

GitHub
↓
GitHub Actions
↓
Docker Hub
↓
Kubernetes Cluster
│
├── Frontend (React)
├── Backend (Node.js)
├── MongoDB
│
├── ConfigMap
├── Secret
├── PVC
├── Ingress
│
└── Monitoring
├── Prometheus
├── Grafana
├── Alertmanager
└── Node Exporter

---

## CI/CD Workflow

1. Developer pushes code to GitHub.
2. GitHub Actions pipeline triggers automatically.
3. Docker images are built.
4. Images are pushed to Docker Hub.
5. Kubernetes deployments pull updated images.
6. Application is deployed and monitored.

---

## Kubernetes Components

### Deployments

* frontend
* backend
* mongodb

### Services

* frontend-service
* backend-service
* mongodb-service

### Configuration

* ConfigMap
* Secret

### Storage

* Persistent Volume Claim (PVC)

### Networking

* Ingress Controller

---

## Monitoring Stack

### Prometheus

Used for collecting:

* Pod metrics
* Node metrics
* Cluster metrics

### Grafana

Used for:

* CPU monitoring
* Memory monitoring
* Pod health monitoring
* Kubernetes dashboards

### Alertmanager

Used for alert management and notifications.

---

## Local Setup

### Clone Repository

```bash
git clone <repository-url>
cd restaurant-project
```

### Docker Compose

```bash
docker compose up --build
```

### Kubernetes Deployment

```bash
kubectl apply -f k8s/
```

### Verify Resources

```bash
kubectl get pods
kubectl get svc
kubectl get ingress
```

---

## Monitoring Setup

### Install Monitoring Stack

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm repo update

helm install monitoring prometheus-community/kube-prometheus-stack -n monitoring
```

### Access Grafana

```bash
kubectl port-forward -n monitoring svc/monitoring-grafana 3000:80
```

Open:

http://localhost:3000

---

## Screenshots

### Application

(Add screenshots)

### Kubernetes Resources

(Add screenshots)

### Grafana Dashboard

(Add screenshots)

### Prometheus Targets

(Add screenshots)

---

## Learning Outcomes

Through this project I learned:

* Docker containerization
* Kubernetes deployments and services
* Ingress routing
* Secrets and ConfigMaps
* CI/CD using GitHub Actions
* Docker Hub image management
* Monitoring using Prometheus and Grafana
* Troubleshooting Kubernetes workloads
* Production-style deployment workflows

---

## Future Improvements

* Automatic Kubernetes deployment from GitHub Actions
* GitOps using ArgoCD
* Helm chart for application deployment
* Alerting integrations
* Production cloud deployment (AWS/GCP/Azure)


![Project Screenshot](images\Screenshot 2026-06-12 000143.png)

![Project Screenshot](images\Screenshot 2026-06-12 000230.png)
