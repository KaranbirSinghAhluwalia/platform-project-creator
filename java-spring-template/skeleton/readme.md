# ${{ values.projectName }}

This is a Spring Boot application scaffolded and deployed using [Backstage](https://backstage.io), with support for Docker, Helm, and GitOps workflows via ArgoCD.

## Build Tool: `${{values.buildTool}}`
## Java Version: `${{values.javaVersion}}`

---

## Features

- Spring Boot REST API  
- Docker containerization  
- Helm charts for Kubernetes deployment  
- GitOps-ready (ArgoCD integration)  
- CI/CD pipeline ready  
- Scaffolded using Backstage Software Templates  

---

## Run Locally

### With Maven

```bash
./mvnw spring-boot:run
```

### With Gradle

```bash
./gradlew bootRun
```

> Ensure Java `${{values.javaVersion}}` is installed locally.

---

## Docker

### Build Docker Image

```bash
docker build -t ${{ values.projectName }}:latest .
```

### Run the Docker Container

```bash
docker run -p 8080:8080 ${{ values.projectName }}:latest
```

> Visit the app at: [http://localhost:8080](http://localhost:8080)

---

## Kubernetes Deployment with Helm

This project includes a Helm chart under the `charts/` directory.

### Prerequisites

- Kubernetes cluster (Minikube, GKE, etc.)
- Helm 3.x+

### Deploy using Helm

```bash
helm install ${{ values.projectName }} ./charts/${{ values.projectName }}
```

---

## Project Structure

```text
.
├── Dockerfile
├── README.md
├── pom.xml or build.gradle
├── src/
│   ├── main/java/com/example/${{ values.projectName }}/HelloController.java
│   └── test/
└── charts/
    └── ${{ values.projectName }}/
```
