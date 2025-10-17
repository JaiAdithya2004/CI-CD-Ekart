# 🚀 Cloud-Native CI/CD Pipeline for Spring Boot Application  
[![Jenkins](https://img.shields.io/badge/Jenkins-Automation-blue?logo=jenkins)](https://www.jenkins.io/)
[![Docker](https://img.shields.io/badge/Docker-Containerization-blue?logo=docker)](https://www.docker.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-blue?logo=kubernetes)](https://kubernetes.io/)
[![SonarQube](https://img.shields.io/badge/SonarQube-Code_Quality-blue?logo=sonarqube)](https://www.sonarqube.org/)
[![Nexus](https://img.shields.io/badge/Nexus-Artifact_Repository-blue?logo=sonatype)](https://www.sonatype.com/)
[![AWS](https://img.shields.io/badge/AWS-EC2_Hosted-orange?logo=amazonaws)](https://aws.amazon.com/)
[![Trivy](https://img.shields.io/badge/Trivy-Security_Scan-green?logo=aqua)](https://aquasecurity.github.io/trivy/)

---

## 📘 Overview  

This project demonstrates a **complete cloud-native CI/CD pipeline** built on **AWS EC2**, integrating modern DevSecOps tools to automate every stage of software delivery — from **code commit** to **Kubernetes deployment**.  

The pipeline is designed for a **Spring Boot shopping cart application**, ensuring quality, security, and scalability with **zero manual intervention**.

---

## 🧩 Key Objectives  

✅ Automate **build, test, quality analysis, and deployment** using Jenkins  
✅ Enforce **DevSecOps** with SonarQube, OWASP, and Trivy  
✅ Containerize the app using **Docker** and deploy to **Kubernetes**  
✅ Manage **artifacts securely** using Nexus  
✅ Host the entire stack on **AWS EC2 instances**

---

## 🌐 Architecture Diagram  

![CI/CD Architecture](./WhatsApp%20Image%202025-10-17%20at%201.16.23%20PM.jpeg)

---

## ⚙️ CI/CD Workflow Breakdown  

1. **👨‍💻 Developer Commit (GitHub)**  
   - Source code pushed to GitHub triggers Jenkins via webhook.  

2. **⚙️ Compile & Unit Test (Maven + JUnit)**  
   - Jenkins compiles the project and runs unit tests for validation.  

3. **🔍 Static Code Analysis (SonarQube)**  
   - Scans for bugs, vulnerabilities, and code smells; generates quality reports.  

4. **🛡️ Security Scan (OWASP Dependency-Check)**  
   - Detects vulnerable libraries using the OWASP CVE database.  

5. **📦 Build & Upload Artifact (Maven + Nexus)**  
   - Maven packages the app and uploads the JAR/WAR file to Nexus.  

6. **🐳 Docker Image Build & Scan (Docker + Trivy)**  
   - Docker builds a container image using the Nexus artifact.  
   - Trivy scans the image for OS and dependency vulnerabilities.  

7. **☸️ Deploy to Kubernetes (AWS EC2 Cluster)**  
   - The verified Docker image is deployed to a Kubernetes cluster.  
   - Kubernetes ensures **scalability**, **load balancing**, and **rolling updates**.  

---

## 🧱 Jenkins Pipeline Visualization  

![Pipeline Stages](./Screenshot%202025-10-18%20001215.png)

| Stage | Description | Tool |
|:------|:-------------|:-----|
| Tool Install | Installs JDK, Maven, Docker, etc. | Jenkins |
| Git Checkout | Pulls latest code | GitHub |
| Code Compile | Compiles and resolves dependencies | Maven |
| Unit Testing | Runs automated tests | JUnit |
| SonarQube Analysis | Checks code quality | SonarQube |
| OWASP Dependency | Scans for CVE vulnerabilities | OWASP |
| Build | Packages the app | Maven |
| Deploy to Nexus | Uploads artifact | Nexus |
| Docker Build & Tag | Builds container image | Docker |
| Trivy Scan | Scans image for security issues | Trivy |
| Docker Push | Pushes image to registry | Docker |
| Kubernetes Deploy | Deploys image to cluster | Kubernetes |

---

## ☁️ AWS Infrastructure  

| Component | Purpose | Instance Type |
|------------|----------|----------------|
| Jenkins Master | CI/CD Orchestration | t2.medium |
| Nexus Repository | Artifact Storage | t2.micro |
| SonarQube Server | Code Quality Analysis | t2.medium |
| Kubernetes Cluster | Application Deployment | t3.medium (Master & Nodes) |

---

## 🧰 Toolchain Overview  

| Tool | Role | 
|------|------|
| **GitHub** | Version Control & Webhook Trigger |
| **Jenkins** | CI/CD Automation |
| **Maven** | Build & Dependency Management |
| **SonarQube** | Code Quality & Security Gate |
| **OWASP Dependency-Check** | Dependency Vulnerability Scanning |
| **Nexus Repository** | Artifact Storage |
| **Docker** | Containerization |
| **Trivy** | Container Vulnerability Scanning |
| **Kubernetes** | Orchestration & Deployment |
| **AWS EC2** | Cloud Infrastructure Hosting |

---
## 🧰 Workflow



![WhatsApp Image 2025-10-17 at 1 16 23 PM](https://github.com/user-attachments/assets/fced888d-912c-48f5-ad51-9b1aa5e25b47)




 <img width="1305" height="348" alt="Screenshot 2025-10-18 001215" src="https://github.com/user-attachments/assets/10b547cb-3155-44f9-b8ea-f79169f135d1" />






 

