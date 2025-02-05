# ci-cd-pipeline-devops
This repository demonstrates a CI/CD pipeline using GitHub Actions, Docker, and Terraform to automate the build, test, deployment, and infrastructure provisioning of a web application.
# Features
- **Automated Build & Test**: Runs unit tests on every push to `main`.
- **Docker Image Deployment**: Builds and pushes Docker images to **Docker Hub**.
- **Server Deployment**: Deploys the application to a remote server via SSH.
- **Infrastructure as Code (IaC)**: Uses **Terraform** to provision cloud resources.
- **GitHub Actions Workflow**: Manages the entire CI/CD pipeline.

## Technologies Used
- **GitHub Actions** (CI/CD workflow)
- **Node.js** (Application & Testing)
- **Docker** (Containerization)
- **Terraform** (Infrastructure as Code)
- **AWS** (Cloud Deployment)

## Setup Instructions

### 1. Fork & Clone the Repo
```bash
   git clone https://github.com/your-username/ci-cd-pipeline-devops.git
   cd ci-cd-pipeline-devops
```

### 2. Set Up GitHub Secrets
- `DOCKER_USERNAME` & `DOCKER_PASSWORD` (Docker Hub credentials)
- `AWS_ACCESS_KEY_ID` & `AWS_SECRET_ACCESS_KEY` (AWS credentials for Terraform)

### 3. Push Code to Trigger the Workflow
```bash
   git add .  
   git commit -m "Initial commit"  
   git push origin main  
```

### 4. Monitor Actions & Deployments
Check the **GitHub Actions** tab for CI/CD execution.

## Workflow Overview

### **1. Build Stage**
- Pulls the latest code from the repository.
- Sets up Node.js and installs dependencies.
- Runs unit tests.

### **2. Dockerization & Push to Registry**
- Builds a Docker image from the source code.
- Pushes the image to **Docker Hub**.

### **3. Deployment to Server**
- Logs into the remote server.
- Pulls the latest Docker image.
- Runs the application in a Docker container.

### **4. Infrastructure Provisioning with Terraform**
- Initializes Terraform and sets up cloud resources.
- Applies the infrastructure changes to **AWS**.

---

## Contribution
Feel free to contribute by submitting pull requests. Ensure all tests pass before submitting changes.

## License
MIT License

