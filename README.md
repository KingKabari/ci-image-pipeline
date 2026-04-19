# CI Image Pipeline

## Overview
This project demonstrates a simple CI/CD pipeline that automatically builds and pushes a Docker image to Docker Hub whenever code is pushed to the `main` branch.

---

## Application
A minimal Node.js application that prints:

```
CI Pipeline App Running
```

---

## How It Works

### 1. Code Push
Whenever code is pushed to the `main` branch, the GitHub Actions workflow is triggered.

---

### 2. CI Pipeline Steps

The workflow performs the following:

- Checks out the repository code  
- Runs a basic validation step  
- Logs in to Docker Hub using stored secrets  
- Builds a Docker image  
- Tags the image with:
  - `latest`
  - the Git commit SHA  
- Pushes both tags to Docker Hub  

---

## Docker Image Tagging

Two tags are generated for every build:

- **latest**  
  Refers to the most recent version of the application  

- **commit SHA**  
  A unique identifier for each build based on the Git commit  
  (ensures traceability and version control)

---

## Docker Hub Repository

https://hub.docker.com/r/kingkabari/ci-image-pipeline
