# Custom Nginx Image
A Custom Nginx Image is a Docker image created by modifying the default Nginx image using a Dockerfile. It allows developers to customize the web server by adding configuration files, HTML pages, or other resources required for a specific application.

Instead of manually configuring a container every time it runs, a custom image packages all required settings and files into one reusable image. This makes deployment faster, consistent, and easier to manage.

## Create a Folder
```bash
mkdir custom-nginx
cd custom-nginx
```

#### Create **index.html**
```bash
<html>
<head><title>Docker Nginx</title></head>
<body>
<h1>Hello from Custom Docker Nginx</h1>
</body>
</html>
```

#### Create **default.conf**

```bash
server {
    listen 80;
    server_name localhost;

    location / {
        root /usr/share/nginx/html;
        index index.html;
    }
}
```

#### Create file **Dockerfile**

```bash
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
COPY default.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
```

#### Build the Image
```bash
docker build -t custom-nginx:v1 .
```

#### Run the Container
```bash
docker run -d -p 8080:80 --name nginx-container custom-nginx:v1
```
Open browser:
http://localhost:8080
