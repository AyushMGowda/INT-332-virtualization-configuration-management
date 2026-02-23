# 🐳 Docker Basic Commands


## 🔍 Check Installation
```bash
docker --version
docker info
```


## 📦 Working with Images
```bash
Search Image
docker search nginx
Pull Image
docker pull nginx
docker pull ubuntu:22.04
List Images
docker images
Remove Image
docker rmi <image_id>
```


## 🚀 Working with Containers

#### Run Container

```bash
docker run nginx
docker run -it ubuntu
docker run -d nginx
```
-it → interactive terminal
-d → detached mode (background)
-p → port

#### Run with Port Mapping
```bash
docker run -d -p 8080:80 nginx
```
Host:Container
Access via → http://localhost:8080


#### List Running Containers
```bash
docker ps
```
#### List All Containers
```bash
docker ps -a
```
#### Stop Container
```bash
docker stop <container_id>
```
#### Start Container
```bash
docker start <container_id>
```
#### Restart Container
```bash
docker restart <container_id>
```
#### Remove Container
```bash
docker rm <container_id>
```


## 🧠 Inspect & Debug

#### Execute Command Inside Running Container
```bash
docker exec -it <container_id> /bin/bash
```

#### View Logs
```bash
docker logs <container_id>
```
#### Inspect Container Details
```bash
docker inspect <container_id>
```
This shows networking, IP, volumes, everything. Don’t ignore this command.


## 🧹 Cleanup Commands

#### Remove All Stopped Containers
```bash
docker container prune
```
### Remove Unused Images
```bash
docker image prune
```
#### Remove Everything Unused
```bash
docker system prune -a
```
#### Rename Container
```bash
docker rename <oldname> <newname>
Show Resource Usage
docker stats
```
