# Docker CLI

### Downloads the Ubuntu image from Docker Hub
```bash
docker pull ubuntu
```
![Container Output](screenshots_and_images/cli1.png)
### Lists all downloaded images
```bash
docker images
```
![Container Output](screenshots_and_images/cli2.png)
### Creates and runs a container from the Ubuntu image
```bash
docker run ubuntu
```
### Runs Ubuntu with terminal access
```bash
docker run -it ubuntu /bin/bash
```
### Stops a running container
```bash
docker stop <container_id>
```
![Container Output](screenshots_and_images/cli3.png)
### Removes a container
```bash
docker rm <container_id>
```
### Deletes the Ubuntu image
```bash
docker rmi ubuntu
```
### Cleans unused containers, images, and networks
```bash
docker system prune -a
```
### Nuclear Clean
```bash
docker system prune -a –volumes
```
