# 🚀 Kubernetes Static Web App Deployment

## 📌 Overview
This project demonstrates an end-to-end DevOps workflow for containerizing and deploying a static web application. It covers the complete lifecycle from writing source code to deploying it on a Kubernetes cluster, showcasing practical experience with Docker, container registries, and Kubernetes orchestration.

## 🏗️ Architecture & Workflow
The deployment pipeline follows these steps:
1. **Source Code:** Developed a static `index.html` file.
2. **Version Control:** Pushed the source code to GitHub.
3. **Containerization:** Created a `Dockerfile` using an Nginx base image to serve the HTML file.
4. **Registry:** Built the Docker image and pushed it to Docker Hub.
5. **Orchestration:** Wrote Kubernetes manifests (`deployment.yaml` and `service.yaml`) to deploy and expose the application.
6. **Deployment:** Applied the manifests to a Kubernetes cluster to run the application.

## 🛠️ Technologies Used
* **Version Control:** Git, GitHub
* **Containerization:** Docker, Docker Hub
* **Web Server:** Nginx (via Docker base image)
* **Container Orchestration:** Kubernetes
* **CLI Tools:** `docker`, `kubectl`

## 📂 Repository Structure
```text
├── index.html            # The static website source code
├── Dockerfile            # Instructions to build the Docker image
├── k8s/                  # Kubernetes configuration files
│   ├── deployment.yaml   # K8s Deployment manifest
│   └── service.yaml      # K8s Service manifest
└── README.md             # Project documentation





