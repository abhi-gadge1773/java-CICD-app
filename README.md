# 🚀 Java CI/CD App

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Java](https://img.shields.io/badge/Java-8-blue)
![Docker Pulls](https://img.shields.io/docker/pulls/abhi2404/javaapp)
![Last Commit](https://img.shields.io/github/last-commit/abhi-gadge1773/java-CICD-app)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

This is a simple Java-based Maven application (`my-app1`) demonstrating a complete CI/CD pipeline using **Jenkins**, **Docker**, and **Docker Hub**. It includes automated build, test, image creation, and deployment processes.

---

## 🧰 Tech Stack

* **Java 8**
* **Maven**
* **Jenkins**
* **Docker**
* **Docker Hub**
* **Git & GitHub**

---

## 📁 Project Structure

```
my-app1/
├── src/                # Java source code
├── pom.xml             # Maven project descriptor
├── Dockerfile          # Container build instructions
├── Jenkinsfile         # CI/CD pipeline for Jenkins
└── README.md           # Project documentation
```

---

## ⚙️ How to Build

### 1. Clone the repository

```bash
git clone https://github.com/abhi-gadge1773/java-CICD-app.git
cd java-CICD-app/my-app1
```

### 2. Build using Maven

```bash
mvn clean package
```

> Output JAR will be generated in the `target/` folder as:
> `target/my-app1-1.0-SNAPSHOT.jar`

---

## 🐳 Docker Instructions

### 1. Build Docker Image

```bash
docker build -t abhi2404/javaapp .
```

### 2. Run Docker Container

```bash
docker run -p 8080:8080 abhi2404/javaapp
```

> Ensure your app listens on port **8080** (or change the mapping if needed)

---

## 🔄 CI/CD Pipeline with Jenkins

CI/CD is automated using the Jenkins pipeline defined in `Jenkinsfile` with stages:

| Stage              | Description                                             |
| ------------------ | ------------------------------------------------------- |
| `SCM Checkout`     | Clones the GitHub repo using Jenkins credentials        |
| `Build with Maven` | Compiles the project using `mvn clean package`          |
| `Docker Build`     | Builds a Docker image using the generated JAR           |
| `Docker Push`      | Pushes the image to Docker Hub under `abhi2404/javaapp` |

> Requires credentials in Jenkins:
>
> * `GitHub` (Git access token)
> * `DOCKER_HUB_PASSWD` (Docker Hub password)

---

## 🥪 Testing

JUnit is included in the project. Tests can be run using:

```bash
mvn test
```

---

## 📆 Deployment

Docker image is pushed to Docker Hub:
👉 [`abhi2404/javaapp`](https://hub.docker.com/r/abhi2404/javaapp)

Run anywhere using:

```bash
docker pull abhi2404/javaapp
docker run -p 8080:8080 abhi2404/javaapp
```

---

## 👤 Author

**Abhijeet Gadge**
🔗 [GitHub Profile](https://github.com/abhi-gadge1773)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE)

