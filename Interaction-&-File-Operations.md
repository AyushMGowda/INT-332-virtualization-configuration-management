# Interaction & File Operations

```bash
docker exec -it <container> ls /
```
```bash
docker exec -it <container> /bin/bash
```
```bash
mkdir /data
```
```bash
echo "Hello Docker" > /data/test.txt
```
```bash
docker attach <container>
```
```bash
docker cp <container>:/data/test.txt C:\Users\HP\Desktop\
```
```bash
docker cp C:\Users\HP\Desktop\test.txt <container>:/data/sample.txt
```
```bash
docker exec -it <container> ls /data
```
```bash
docker exec -it <container> cat /data/sample.txt
```
