# ACEest Fitness 🏋️‍♂️
A Flask-based fitness and gym management system demonstrating a complete DevOps CI/CD pipeline — including version control, testing, containerization, and automated deployment using Jenkins, Docker, and Kubernetes.

---

## 🚀 Project Overview
The **ACEest Fitness** web application provides a foundation for managing gym operations — including member registration, workout plans, attendance tracking, and trainer management.  
It follows a modular, version-controlled development approach integrating automation and modern DevOps practices.

---

## 🧩 Core Components
| Component | Description |
|------------|-------------|
| **Flask App** | Core Python web app (`ACEest_Fitness.py`) implementing backend routes and logic |
| **Versioning** | Incremental version files (e.g., `ACEest_Fitness-V1.1.py`, `V1.2.3.py`, etc.) following semantic versioning |
| **Unit Testing** | Pytest-based test suite verifying all key functionalities |
| **Jenkins Pipeline** | Automated CI/CD pipeline with build, test, SonarQube, and Docker integration |
| **Dockerfile** | Builds container images for deployment |
| **Kubernetes Manifests** | YAML files for deployment, service, and ingress configuration |
| **SonarQube** | Static code analysis and quality gates |
| **GitHub Repository** | Central VCS with branching, tagging, and automated triggers |

---

## 🧪 Features Implemented
- Flask modular architecture with version-controlled updates
- Automated unit testing using **Pytest**
- Continuous Integration via **Jenkins**
- Continuous Delivery/Deployment on **Kubernetes (Minikube / Cloud)**
- Containerization with **Docker & Podman**
- Deployment strategies:
  - Blue-Green Deployment  
  - Canary Release  
  - Shadow Deployment  
  - A/B Testing  
  - Rolling Update
- Code quality validation using **SonarQube**
- Versioned container images on **Docker Hub**

---

## 🧰 Tools and Technologies
| Category | Tools Used |
|-----------|-------------|
| Programming | Python, Flask |
| Version Control | Git, GitHub |
| CI/CD | Jenkins |
| Testing | Pytest |
| Containerization | Docker, Podman |
| Orchestration | Kubernetes, Minikube |
| Code Quality | SonarQube |
| Cloud (optional) | AWS / Azure / GCP |

---

## ⚙️ CI/CD Pipeline Workflow
1. Developer commits and pushes code to GitHub.
2. Jenkins automatically triggers a build pipeline:
   - Clones the repo  
   - Installs dependencies  
   - Runs Pytest test cases  
   - Performs SonarQube analysis  
   - Builds Docker image and tags version  
   - Pushes Docker image to Docker Hub  
   - Deploys latest image to Kubernetes cluster
3. Kubernetes deploys the new pod version following the selected deployment strategy.

---

## 🐳 Docker Commands
```bash
# Build Docker Image
docker build -t aceest_fitness:v1.3 .

# Run locally
docker run -p 5000:5000 aceest_fitness:v1.3

# Push to Docker Hub
docker tag aceest_fitness:v1.3 your_dockerhub_username/aceest_fitness:v1.3
docker push your_dockerhub_username/aceest_fitness:v1.3
