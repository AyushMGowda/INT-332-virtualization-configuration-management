# 🐳 Docker Basics – INT 332

### 1️⃣ What is Docker?

Docker is a containerization platform that allows applications to run in isolated environments called containers.

Containers package:
- Application code
- Dependencies
- Libraries
- Runtime

This ensures the app runs the same on every machine.

---

### 2️⃣ What is Containerization?

Containerization is a lightweight alternative to virtualization.

Instead of running a full OS for every application, containers share the host OS kernel but remain isolated.

---

### 3️⃣ Virtual Machines vs Containers

| Feature | Virtual Machine | Container |
|----------|----------------|-----------|
| OS | Full OS per VM | Shares host OS kernel |
| Size | Large (GBs) | Lightweight (MBs) |
| Boot Time | Minutes | Seconds |
| Performance | Slower | Faster |

---

### 4️⃣ Docker Architecture

Docker uses a Client-Server architecture:

- Docker Client → Runs commands
- Docker Daemon → Executes commands
- Docker Images → Blueprint
- Docker Containers → Running instance of image
- Docker Hub → Public image registry

---

### 5️⃣ Docker Image

An image is a read-only template used to create containers.
Example
```bash
docker pull nginx
```

---

### 6️⃣ Docker Container

A container is a running instance of an image.
Example:
```bash
docker run nginx
```

---

### 7️⃣ Basic Workflow

1. Pull image
2. Run container
3. Interact with container
4. Stop container
5. Remove container

---

### 8️⃣ Why Docker is Important in DevOps

- Consistent environments
- Faster deployments
- Microservices architecture
- CI/CD integration

