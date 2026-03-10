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

### Run First Container
```bash
docker run -dit --name web --network mynetwork nginx
```

### Run Second Container
```bash
docker run -it --name tester --network mynetwork busybox
```

### Test Container Communication
```bash
ping web
```

### Check Network Details
```bash
docker network inspect mynetwork
```

### Cleanup
```bash
docker stop web tester
docker rm web tester
docker network rm mynetwork
```
