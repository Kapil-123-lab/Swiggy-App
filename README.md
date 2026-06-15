# Swiggy-App

# 🚀 End-to-End DevOps CI/CD Pipeline for Swiggy Application

## 📌 Project Overview

This project demonstrates the implementation of a complete **DevOps CI/CD pipeline** for a containerized web application. The objective was to automate the software delivery lifecycle, from source code integration to deployment, using industry-standard DevOps tools and practices.

The pipeline integrates **GitHub**, **Jenkins**, **SonarQube**, **Docker**, **Docker Hub**, and **AWS/Linux environments** to achieve continuous integration, automated code quality analysis, containerization, and deployment automation.

This project showcases practical experience in building production-ready CI/CD workflows that improve deployment consistency, reduce manual effort, and accelerate software delivery.

---

## 🛠️ Technology Stack

| Category | Tools |
|-----------|--------|
| Source Code Management | Git, GitHub |
| CI/CD | Jenkins |
| Code Quality Analysis | SonarQube |
| Containerization | Docker |
| Container Registry | Docker Hub |
| Operating System | Linux / Windows |
| Cloud Platform | AWS EC2 |
| Webhook Integration | ngrok |

---

# 🏗️ Project Architecture

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ├── Source Code Checkout
    │
    ├── SonarQube Code Analysis
    │
    ├── Quality Gate Validation
    │
    ├── Application Build
    │
    ├── Docker Image Build
    │
    ├── Docker Image Push
    │
    ▼
Docker Hub
    │
    ▼
Docker Container Deployment
    │
    ▼
Running Application
```

---

# ⚙️ Workflow Explanation

## Step 1: Source Code Management

- Application source code is maintained in a GitHub repository.
- Developers push changes to GitHub.

### Benefits

- Version control
- Collaboration
- Source code tracking

---

## Step 2: Continuous Integration with Jenkins

Jenkins automatically triggers the pipeline whenever code changes are pushed to GitHub.

### Activities Performed

- Workspace cleanup
- Source code checkout
- Dependency installation
- Build execution

### Benefits

- Automated builds
- Faster feedback cycle
- Reduced manual effort

---

## Step 3: Static Code Analysis using SonarQube

Jenkins integrates with SonarQube to perform automated code quality checks.

### Analysis Includes

- Code smells
- Bugs
- Vulnerabilities
- Maintainability issues

### Benefits

- Improved code quality
- Early issue detection
- Secure coding practices

---

## Step 4: Quality Gate Validation

The pipeline validates SonarQube Quality Gates before proceeding.

### Purpose

Ensures only quality-approved code moves to the deployment stage.

### Benefits

- Enforces quality standards
- Prevents defective code deployment

---

## Step 5: Docker Image Build

After successful validation:

- Docker image is created.
- Application is packaged into a portable container.

### Benefits

- Environment consistency
- Simplified deployment
- Scalability

---

## Step 6: Docker Hub Integration

The generated Docker image is pushed to Docker Hub.

### Benefits

- Centralized image repository
- Easy image distribution
- Version management

---

## Step 7: Application Deployment

Docker image is deployed as a running container.

### Benefits

- Rapid deployment
- Easy rollback capability
- Platform-independent execution

---

# ⭐ Key Features

### CI/CD Automation

Implemented an end-to-end automated software delivery pipeline.

### Code Quality Enforcement

Integrated SonarQube Quality Gates to ensure code quality compliance.

### Containerization

Packaged the application into Docker containers for consistent deployments.

### Automated Deployment

Reduced manual deployment efforts through pipeline-driven deployments.

### Docker Registry Integration

Automated image publishing to Docker Hub.

### DevOps Best Practices

Applied continuous integration and continuous delivery principles.

### Webhook-Based Automation

Configured webhook integration to trigger builds automatically.

---

# 🎯 Challenges Faced

## 1. SonarQube Webhook Integration

### Challenge

Jenkins was running locally and SonarQube Quality Gate validation required webhook communication.

### Solution

Configured ngrok tunneling to expose the local Jenkins instance and established webhook connectivity.

---

## 2. Jenkins Tool Configuration

### Challenge

Pipeline execution failed due to incorrect JDK and Sonar Scanner configurations.

### Solution

Configured:

- JDK 21
- Sonar Scanner
- NodeJS
- Jenkins Global Tool Configuration

---

## 3. Jenkins Service Failure

### Challenge

Jenkins failed to start after Java reconfiguration.

### Solution

- Reinstalled JDK
- Updated JAVA_HOME
- Corrected Jenkins Java executable path
- Restarted Jenkins service

---

## 4. Git Branch Checkout Issue

### Challenge

Jenkins could not find the target branch.

### Solution

Verified repository branch naming and updated pipeline checkout configuration.

---

## 5. Docker Deployment Issues

### Challenge

Container deployment occasionally failed due to existing container conflicts.

### Solution

Implemented container cleanup before deployment:

```bash
docker rm -f swiggy
```

---

# 📚 Key Learnings

Through this project, I gained hands-on experience in:

### DevOps Practices

- Continuous Integration
- Continuous Delivery
- Release Automation

### Jenkins

- Pipeline creation
- Tool management
- Build automation
- Pipeline troubleshooting

### SonarQube

- Static code analysis
- Quality Gates
- Code quality management

### Docker

- Image creation
- Container lifecycle management
- Registry integration

### GitHub

- Source code management
- Branch management
- Webhook configuration

### AWS & Linux

- Application deployment
- Infrastructure management
- Container hosting

### Troubleshooting Skills

- Jenkins service debugging
- Java configuration issues
- Pipeline failures
- Docker deployment issues

---

# 🚀 Future Improvements

## Kubernetes Deployment

Move from standalone Docker containers to Kubernetes orchestration.

### Benefits

- Auto-scaling
- High availability
- Self-healing

---

## Infrastructure as Code (IaC)

Integrate Terraform for infrastructure provisioning.

### Benefits

- Automated infrastructure creation
- Consistent environments

---

## Monitoring & Observability

Implement:

- Prometheus
- Grafana

### Benefits

- Real-time monitoring
- Alerting
- Performance tracking

---

## Security Scanning

Add:

- Trivy
- OWASP Dependency Check

### Benefits

- Vulnerability detection
- Secure deployments

---

## Automated Testing

Integrate:

- Unit testing
- Integration testing

### Benefits

- Improved software quality
- Reduced production issues

---

## GitOps Implementation

Implement GitOps workflows using ArgoCD.

### Benefits

- Declarative deployments
- Improved change management

---

# 📈 Business Impact

- Reduced manual deployment effort
- Improved deployment consistency
- Faster release cycles
- Enhanced code quality
- Increased delivery reliability
- Better visibility into software quality

---

# 🏆 Conclusion

This project successfully demonstrates the implementation of a complete DevOps CI/CD pipeline using Jenkins, SonarQube, Docker, Docker Hub, GitHub, and AWS/Linux environments.

The solution automates the software delivery lifecycle, enforces code quality standards, simplifies deployments through containerization, and follows modern DevOps best practices. The project provided valuable hands-on experience in automation, containerization, quality assurance, and deployment management, strengthening practical DevOps and Site Reliability Engineering skills.

---
