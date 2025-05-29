# Java Spring Boot Application Template

This is a ready-to-go template for creating Spring Boot microservices using either **Maven** or **Gradle**, with support for:

- ✅ Java version selection (17 or 21)
- ✅ Build tool choice (Maven / Gradle)
- ✅ Preconfigured **Dockerfile**
- ✅ Pre-integrated **Jacoco** for test coverage
- ✅ REST Starter boilerplate

## Usage

This template is designed to be used inside **Backstage** via the scaffolder UI.

### Configuration Options

| Parameter     | Description                        |
|---------------|------------------------------------|
| `name`        | Name of your new app               |
| `buildTool`   | Either `maven` or `gradle`         |
| `javaVersion` | Choose between `17` or `21`        |

## Running the App

Build & run via Docker:

```bash
docker build --build-arg JAVA_VERSION=17 -t myapp .
docker run -p 8080:8080 myapp
