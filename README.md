# React + Nginx Docker Deployment with CI/CD Pipeline

This repository demonstrates the deployment of a React application served using Nginx. The project includes a Dockerfile, a CI/CD pipeline, and a virtual machine setup for hosting the application with secure configuration and logging.

---

## 🚀 Project Overview

### Features
1. **React Application**: Built and served using Nginx in a Docker container.
2. **Dockerized Deployment**: Includes a `Dockerfile` and `docker-compose.yml` for containerization and service management.
3. **CI/CD Pipeline**:
   - Builds the Docker image.
   - Pushes it to a container registry (e.g., Docker Hub, Azure Container Registry).
   - Updates the image on the host VM and restarts the container automatically.
4. **Virtual Machine Hosting**:
   - Single VM with 1 CPU, 1 GB RAM.
   - Public IP access with strict security rules.
5. **Logging**:
   - Persistent logs from the container mapped to a folder on the host VM.
6. **Versioning**:
   - Docker images tagged using a consistent versioning strategy (e.g., `v1`, `v2`, `latest`).

---

## 📂 Project Structure

```plaintext
.
├── Dockerfile               # Dockerfile to build and serve React app with Nginx
├── docker-compose.yml       # Docker Compose for managing services
├── .github/workflows        # CI/CD pipeline configuration for GitHub Actions
│   └── ci-cd-pipeline.yml
├── src/                     # React app source code
├── public/                  # React app static assets
├── README.md                # Project documentation
└── scripts/                 # Scripts for VM and deployment setup
