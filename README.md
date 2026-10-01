# Secure Python DevSecOps Pipeline

A Python Flask web application secured with an automated **DevSecOps CI/CD pipeline** using GitHub Actions.

This project demonstrates how security can be integrated into different stages of the software development lifecycle, including source-code analysis, dependency scanning, container security, testing, and code quality.

---

## 📌 Project Overview

The objective of this project is to build a secure Python web application and integrate multiple security tools into a CI/CD pipeline.

The pipeline performs:

- Application testing using Pytest
- Static Application Security Testing (SAST) using CodeQL
- Dependency update management (SCA) using Dependabot
- Code quality and security analysis using SonarQube
- Docker image creation
- Container vulnerability scanning using Trivy

---

## 🏗️ Project Architecture

```text
                         Developer
                             |
                             v
                    GitHub Repository
                  secure-python-devsecops
                             |
                             v
                    GitHub Actions CI/CD
                             |
        +--------------------+--------------------+
        |                    |                    |
        v                    v                    v
     Pytest                CodeQL               Depandabot
   Unit Testing             SAST                 SCA
        |                    |                    |
        +--------------------+--------------------+
                             |
                             v
                         SonarQube
                  Code Quality + Security
                             |
                             v
                       Docker Build
                             |
                             v
                      Docker Image
                             |
                             v
                          Trivy
                  Container Vulnerability Scan
                             |
                             v
                       Deployment
