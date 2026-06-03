# Docker Project – Nginx Static Website

## Overview

This project demonstrates the containerization of a simple static web page using Docker and Nginx. The application serves a custom HTML page through an Nginx web server running inside a Docker container.

This project was created as part of my Docker learning journey to gain hands-on experience with:

* Docker image creation
* Dockerfile configuration
* Container deployment
* Nginx web server
* Git and GitHub integration

---

## Project Structure

```text
docker-project/
├── Dockerfile
├── index.html
└── README.md
```

---

## Dockerfile

```dockerfile
FROM nginx
COPY index.html /usr/share/nginx/html/index.html
```

### Explanation

* `FROM nginx` – Uses the official Nginx image as the base image.
* `COPY index.html /usr/share/nginx/html/index.html` – Copies the custom web page into the default Nginx web root.

---

## Web Page Content

The application serves a simple HTML page:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Ashwini Docker Project</title>
</head>
<body>
    <h1>Hello from Ashwini's Docker Container!</h1>
    <p>Day 4 - Docker Learning Journey</p>
</body>
</html>
```

---

## Prerequisites

Before running this project, ensure the following are installed:

* Docker
* Git

Verify installation:

```bash
docker --version
git --version
```

---

## Clone the Repository

```bash
git clone https://github.com/Ashwini-dudu/Docker-project.git

cd Docker-project
```

---

## Build the Docker Image

```bash
docker build -t ashwini-nginx .
```

---

## Run the Container

```bash
docker run -d -p 80:80 --name ashwini-web ashwini-nginx
```

---

## Verify Container Status

```bash
docker ps
```

Expected output should show the container running and port 80 exposed.

---

## Access the Application

### Local Machine

```text
http://localhost
```

### AWS EC2 Instance

```text
http://<EC2-Public-IP>
```

Example:

```text
http://13.xxx.xxx.xxx
```

---

## Useful Docker Commands

### View Running Containers

```bash
docker ps
```

### View Container Logs

```bash
docker logs ashwini-web
```

### Stop Container

```bash
docker stop ashwini-web
```

### Start Container

```bash
docker start ashwini-web
```

### Remove Container

```bash
docker rm -f ashwini-web
```

### Remove Image

```bash
docker rmi ashwini-nginx
```

---

## Learning Outcomes

Through this project, I gained practical experience with:

* Building Docker images
* Working with Dockerfiles
* Running and managing containers
* Port mapping
* Serving static content using Nginx
* Version control using Git and GitHub

---

## Author

**Ashwini Kumari**

* Docker Enthusiast
* DevOps Learner
* Cloud & Infrastructure Professional

GitHub: https://github.com/Ashwini-dudu

