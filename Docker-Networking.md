# Docker Networking

### Create a Custom Network
```bash
docker network create mynetwork
```

### Check Existing Networks
```bash
docker network ls
```
Now you'll see:
mynetwork

![Container Output](screenshots_and_images/networking1.png)
### Run First Container
```bash
docker run -dit --name web --network mynetwork nginx
```
![Container Output](screenshots_and_images/networking2.png)
### Run Second Container
```bash
docker run -it --name tester --network mynetwork busybox
```
### Test Container Communication
```bash
ping web
```
![Container Output](screenshots_and_images/networking3.png)
### Check Network Details
```bash
docker network inspect mynetwork
```
![Container Output](screenshots_and_images/networking4.png)
![Container Output](screenshots_and_images/networking5.png)
![Container Output](screenshots_and_images/networking6.png)
### Cleanup
```bash
docker stop web tester
docker rm web tester
docker network rm mynetwork
```
![Container Output](screenshots_and_images/networking7.png)
