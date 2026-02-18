# 🚀 DevOps Kubernetes Deployment Project

## 📌 Project Overview

This project demonstrates deploying a containerized Python Flask application to a Kubernetes cluster using Deployments, Services, and Namespaces.

The application is packaged using Docker and deployed with replica scaling inside Kubernetes.

---

## 🛠 Tech Stack

- Python (Flask)
- Docker
- Kubernetes
- Minikube
- kubectl

---

## 🏗 Architecture

Developer → Docker Build → DockerHub → Kubernetes Deployment → Service (NodePort) → Browser

- Docker image is built locally  
- Image is pushed to DockerHub  
- Kubernetes Deployment creates multiple replicas  
- Service exposes the application  

---

## 📂 Project Structure

.
├── app.py  
├── requirements.txt  
├── Dockerfile  
├── namespace.yaml  
├── deployment.yaml  
├── service.yaml  
└── README.md  

---

## 🐳 Step 1: Build & Push Docker Image

docker build -t <your-dockerhub-username>/devops-k8s-project .  
docker push <your-dockerhub-username>/devops-k8s-project  

---

## ☸ Step 2: Start Kubernetes (Minikube)

minikube start  

---

## 🚀 Step 3: Deploy to Kubernetes

kubectl apply -f namespace.yaml  
kubectl apply -f deployment.yaml  
kubectl apply -f service.yaml  

Check running pods:

kubectl get pods -n devops  

---

## 🌐 Access the Application

minikube service flask-service -n devops  

Open the generated URL in your browser.

---

## 📈 Features Implemented

- Containerized Flask Application  
- Kubernetes Namespace isolation  
- Deployment with multiple replicas  
- NodePort Service exposure  
- Basic health endpoint  
- Horizontal scaling capability  

---

## 🔄 Scaling the Application

kubectl scale deployment flask-app --replicas=4 -n devops  

---

## 🧠 Key Kubernetes Concepts Used

- Pods  
- Deployments  
- ReplicaSets  
- Services  
- Namespaces  

---

## 📌 Resume Description

Deployed a Dockerized Python application to Kubernetes using Deployments and Services with replica scaling and namespace isolation, demonstrating container orchestration fundamentals.

---
