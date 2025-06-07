
# French-English Translator - DevOps CI/CD Pipeline


## 📋 Project Overview

A modern French-English translation web application showcasing **enterprise DevOps practices** including containerization, automated CI/CD pipelines, and cloud deployment on Microsoft Azure.

While the application itself is simple, the focus is on demonstrating **production-ready DevOps workflows** that can scale to any enterprise application.

## 🏗️ Architecture
GitHub Repository → GitHub Actions → Azure Container Registry → Azure Container Instances

### Tech Stack
- **Frontend:** Vanilla JavaScript with modern CSS (Glassmorphism design)
- **API:** MyMemory Translation API (free tier)
- **Containerization:** Docker with Nginx Alpine
- **CI/CD:** GitHub Actions
- **Cloud Platform:** Microsoft Azure
- **Infrastructure:** Azure Container Registry + Azure Container Instances

## 🚀 Features

### Application Features
- ✅ Bidirectional French ↔ English translation
- ✅ Real-time translation with debouncing
- ✅ Character counter and validation
- ✅ Modern responsive design
- ✅ Mobile-optimized interface

### DevOps Features
- ✅ Automated CI/CD pipeline
- ✅ Containerized deployment
- ✅ Automated testing and health checks
- ✅ Zero-downtime deployments
- ✅ Cloud-native architecture
- ✅ Proper secrets management

## 🔄 CI/CD Pipeline

### Pipeline Triggers
- **Push to main branch:** Triggers full build and deployment
- **Pull requests:** Runs tests only (no deployment)

### Pipeline Stages

1. **Build & Test**
   - Checkout source code
   - Build Docker image locally
   - Run container health checks
   - Validate application functionality

2. **Deploy to Production**
   - Authenticate with Azure
   - Build production Docker image
   - Push to Azure Container Registry
   - Deploy to Azure Container Instances
   - Generate public URL

### Sample Pipeline Output
```bash
✅ Build and Test completed in 2m 15s
✅ Container health check passed
✅ Deploy to Production completed in 3m 42s
🚀 Application deployed: http://translator-app-123.eastus.azurecontainer.io
🛠️ Local Development
Prerequisites

Docker installed
Git installed

Quick Start
bash# Clone the repository
git clone https://github.com/metro98/french-english-translator-devops.git
cd french-english-translator-devops

# Build and run locally
docker build -t translator-app .
docker run -p 8080:80 translator-app

# Open browser
open http://localhost:8080
Development with Docker Compose
bash# Run with hot reload (development mode)
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
📊 Monitoring & Observability
Health Checks

Automated: Pipeline includes container health verification
Manual: Access health endpoint (if implemented)
Azure Portal: Container insights and metrics

Logging

Application Logs: Available in Azure Container Instances
Pipeline Logs: GitHub Actions provides detailed execution logs
Access Logs: Nginx access/error logs in container

🔒 Security
Secrets Management

Azure credentials stored in GitHub Secrets
Container registry authentication via secure tokens
No sensitive data in source code

Container Security

Alpine Linux base image (minimal attack surface)
Non-root user execution
Security headers configured in Nginx

💰 Cost Management
Current Azure Resources

Container Registry: Basic tier (~$5/month)
Container Instances: Pay-per-use (~$10-20/month for demo usage)
Total Estimated Cost: ~$15-25/month

Cost Optimization

Containers auto-stop when not in use
Basic tier registries for development
Resource limits prevent cost overruns

🚀 Deployment
Automatic Deployment
Every push to main branch triggers automatic deployment:

Code changes pushed to GitHub
GitHub Actions builds and tests
Production image created and pushed to ACR
New container deployed to ACI
Application accessible at new URL

Manual Deployment
bash# Trigger deployment manually
git commit --allow-empty -m "Deploy to production"
git push origin main
🧪 Testing
Automated Tests

Container health checks
HTTP response validation
Application functionality verification

Manual Testing
bash# Test the live application
curl -f http://translator-app-XXX.eastus.azurecontainer.io

# Test translation functionality
# (Use browser interface for full testing)
📈 Future Enhancements
Tier 2 (Intermediate)

 Infrastructure as Code (Terraform)
 Multi-environment deployments (staging/production)
 Security scanning integration
 Advanced monitoring with Azure Monitor

Tier 3 (Advanced)

 Kubernetes deployment (AKS)
 GitOps with ArgoCD
 Blue-green deployments
 Comprehensive observability stack

🤝 Contributing

Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request


🙏 Acknowledgments

MyMemory Translation API for free translation services
Microsoft Azure for cloud infrastructure
GitHub Actions for CI/CD platform
Docker for containerization technology


⭐ Star this repository if it helped you learn DevOps practices!
