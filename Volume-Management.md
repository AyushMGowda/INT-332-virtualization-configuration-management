# Docker Volume Management

```bash
docker volume create mydata
```

```bash
docker volume ls
```

```bash
docker volume inspect mydata
```

```bash
docker run -dit --name mycontainer -v mydata:/app/data ubuntu
```

```bash
docker exec -it mycontainer ls /app/data
```

```bash
docker inspect mycontainer
```

```bash
docker rm -f mycontainer
```

```bash
docker volume rm mydata
```

```bash
docker volume prune
```
