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


🚀 How to Run the Project
Prerequisites
Before you begin, ensure you have the following installed:

Docker

A running Kubernetes cluster (e.g., Minikube, kind, or Docker Desktop with K8s enabled)

kubectl command-line tool

Step 1: Clone the Repository
Bash
git clone [https://github.com/](https://github.com/)[Your-GitHub-Username]/[Your-Repository-Name].git
cd [Your-Repository-Name]
Step 2: Build and Push the Docker Image (Optional)
Note: The Kubernetes manifests are already configured to pull the image from Docker Hub. If you want to build it yourself, run:

Bash
docker build -t [Your-DockerHub-Username]/[Your-Image-Name]:latest .
docker push [Your-DockerHub-Username]/[Your-Image-Name]:latest
Step 3: Deploy to Kubernetes
Navigate to the k8s directory and apply the manifests:

Bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
Step 4: Verify the Deployment
Check if the pods and services are running correctly:

Bash
kubectl get pods
kubectl get svc
Step 5: Access the Application
If you are using Minikube, you can expose the service to access your website locally:

Bash
minikube service [Name-Of-Your-Service]
(Alternatively, use kubectl port-forward svc/[Name-Of-Your-Service] 8080:80 and visit http://localhost:8080 in your browser).

🧹 Cleanup
To remove the deployed resources from your cluster, run:

Bash
kubectl delete -f k8s/deployment.yaml
kubectl delete -f k8s/service.yaml
Author: Yogesh
[Link to your LinkedIn Profile] | [Link to your Portfolio/Other Repos]


**Next Step:**
Would you like me to review the actual code inside your `Dockerfile`, `deployment.
