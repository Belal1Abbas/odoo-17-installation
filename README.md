## 📖 Overview
This project demonstrates a full, practical implementation of an end-to-end DevOps lifecycle. It starts with pulling code from GitHub, then building a Docker image, deploying it to a Kubernetes cluster managed with Kubeadm, configuring servers with Ansible, creating a CI/CD pipeline with Jenkins, and finally deploying the application using ArgoCD with GitOps workflows.

The pipeline ensures a production-ready, scalable, and self-healing infrastructure similar to what is used in enterprise environments.

<img width="1408" height="435" alt="Gemini_Generated_Image_nwzemcnwzemcnwze" src="https://github.com/user-attachments/assets/38fc35a5-c211-4b04-a280-f14328a936d5" />



## 🔥 Key Capabilities
### 🔗 GitHub – Source Code

Step:
The application code was pulled from a Git repository to prepare for the DevOps pipeline.
Goal:
Provide a source-ready version of the application.
Prepare the code for containerization and Kubernetes deployment.
Start the DevOps lifecycle with Git as the single source of truth.

### 📦Containerization with Docker 🐳

Step:
A Dockerfile was created to build the application image.
Goal:
Make the application portable and environment-independent.
Ensure consistent, immutable deployments across different environments.
Prepare the Docker image for Kubernetes deployment.

### ☸️Container Orchestration with Kubernetes☸️

Steps:
Set up a Kubeadm-based Kubernetes cluster (master + worker nodes on separate VMs).
Created the iVolve namespace for the application.
Configured Deployment and Service resources for high availability.
Goal:
Run the application in a production-like orchestration environment.
Provide self-healing, load-balancing, and scalability.
Isolate resources in its own namespace.
Enable rolling updates, service discovery, and Kubernetes-native features.

### 🤖 Configuration Management with Ansible 🤖

Steps:
Created Ansible playbooks to automate server configuration, including:
Installing Docker , Installing Git, Installing Java,Installing Jenkins
Preparing the environment for CI/CD
Goal:
Automate server setup without manual intervention.
Easily reproduce the same environment across multiple servers.
Ensure Jenkins and other dependencies are ready for the pipeline.

### 🚀Continuous Integration with Jenkins🚀

Steps:
A Jenkins pipeline was configured via Jenkinsfile with the following stages:
Build Docker Image
Bonus: Scan Image using Trivy (vulnerability scanning)
Push Image into DockerHub
Delete Local Image
Update Kubernetes Manifests
Push Manifests to Git
Use Shared Library for reusable pipeline steps
(Optional) Launch Jenkins slaves on-demand
Goal:
Fully automate the build and deployment process.
Ensure that every code update results in a new image and deployment.
Maintain clear stage separation for easy monitoring and maintenance.

### ✅ Continuous Deployment with ArgoCD (GitOps)

Steps:
Installed ArgoCD in the Kubernetes cluster.
Created an Application resource to continuously monitor the Git repository.
Any updates in manifests are automatically synced and deployed to the cluster.
Goal:
Implement GitOps workflows, using Git as the single source of truth.
Enable automated, pull-based deployment without human intervention.
Provide a dashboard to monitor application status and sync state.
Ensure secure, stable, and reliable deployments.
## ⭐ Project Highlights


- ☸️ Kubeadm-based Kubernetes Cluster
- 📦 Dockerized Application Workflow
- 🤖 Automated Server Configuration via Ansible
- 🚀 Jenkins CI/CD Pipeline
- 🔗 GitOps Deployment using ArgoCD
- 🛡️ Namespace isolation & managed workloads
- 🔄 End-to-end production-ready workflow
- 🔍 Vulnerability scanning with Trivy
- ⬆️ Rolling updates & self-healing deployments
- 📊 Centralized monitoring and management
