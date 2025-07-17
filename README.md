# Java CI/CD App 🚀

A Spring Boot Java application demonstrating a complete CI/CD pipeline — from code commit through build, test, containerization, and deployment — using modern DevOps tooling.

## Features

- **📦 Spring Boot REST API** – A basic Java app built with Maven.
- **CI with GitHub Actions** – Automatically builds, tests, and analyzes code on each commit or pull request.
- **Containerization with Docker** – Builds a Docker image and runs the app locally.
- **Docker Compose** – Runs the app with dependencies in a single config.
- **(Optional) Kubernetes Deployment** – Launches the app in a K8s cluster.
- **(Optional) Terraform Infrastructure** – Spins up required cloud resources via IaaC.

---

## 🛠️ Getting Started

### Prerequisites

- Java 17+
- Maven 3.8+
- Docker & Docker Compose
- (Optional) Kubernetes (`kubectl`) & Terraform (v1.x)

### Run Locally with Maven

```bash
git clone https://github.com/abhi-gadge1773/java-CICD-app.git
cd java-CICD-app
./mvnw clean package
java -jar target/*.jar
