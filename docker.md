# Docker

Welcome to the **Docker Wiki**! This resource is designed to help developers understand and use Docker for containerization, automating the deployment of applications, and improving the efficiency of the development lifecycle.

## Description

Docker is an open-source platform used to automate the deployment, scaling, and management of applications in containers. A container is a lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, runtime, libraries, and dependencies.

Docker allows developers to build applications and services, package them with all necessary dependencies, and deploy them consistently across any environment. It is widely used in DevOps practices for creating consistent development environments, streamlining testing, and enabling continuous integration and continuous deployment (CI/CD) pipelines.

## Useful Links

- [Official Docker Documentation](https://docs.docker.com/)
- [Docker GitHub Repository](https://github.com/docker/docker)
- [Docker CLI Reference](https://docs.docker.com/engine/reference/commandline/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [Docker Hub](https://hub.docker.com/)

## Table of Contents

- [Description](#description)
- [Useful Links](#useful-links)
- [Docker Versions](#docker-versions)
- [Basic Docker Commands](#basic-docker-commands)

## Docker Versions

Docker has undergone several updates since its release. Some key versions include:

- **Docker 1.0**  
  Released in 2013, it marked Docker's official launch, introducing containerization features and establishing Docker as a leader in the container technology space.

- **Docker 1.12**  
  Introduced Docker Swarm mode, providing native clustering and orchestration for managing Docker containers in a distributed environment.

- **Docker 18.09**  
  Added major improvements in Kubernetes support, container networking, and image management, making Docker even more suitable for large-scale production environments.

- **Docker 20.10**  
  The latest stable version, providing ongoing improvements in security, performance, and compatibility with the Kubernetes ecosystem.

For a detailed list of Docker versions and release notes, visit the [Docker Version History](https://docs.docker.com/engine/release-notes/).

## Basic Docker Commands

Here are some basic Docker commands to help you get started with Docker:

**Install Docker**  
Follow the installation guide on the [Docker Documentation](https://docs.docker.com/get-docker/).

**Check Docker Version**  
```bash
docker --version
```

**Run a Docker Container**  
```bash
docker run hello-world
```
This command runs the official "hello-world" container, which prints a message confirming that Docker is installed correctly.

**List Running Containers**  
```bash
docker ps
```
This command shows all the currently running containers.

**List All Containers (including stopped)**  
```bash
docker ps -a
```

**Build an Image from a Dockerfile**  
```bash
docker build -t my-image .
```
This command builds a Docker image using the `Dockerfile` in the current directory.

**Run a Container from an Image**  
```bash
docker run -d --name my-container my-image
```
This runs a container from the `my-image` Docker image in detached mode (`-d`), naming it `my-container`.

**Stop a Running Container**  
```bash
docker stop my-container
```

**Remove a Stopped Container**  
```bash
docker rm my-container
```

**List Docker Images**  
```bash
docker images
```

**Remove a Docker Image**  
```bash
docker rmi my-image
```

**Using Docker Compose**  
Docker Compose is used to define and manage multi-container Docker applications. Here's how you can use it:

1. Create a `docker-compose.yml` file with your container definitions.
2. Run `docker-compose up` to start all containers defined in the Compose file.

Example of `docker-compose.yml`:
```yaml
version: '3'
services:
  web:
    image: nginx
    ports:
      - "8080:80"
```
This runs an Nginx container and maps port 8080 on the host to port 80 inside the container.

**View Logs of a Container**  
```bash
docker logs my-container
```

**Exec Into a Running Container**  
```bash
docker exec -it my-container /bin/bash
```
This opens an interactive terminal session inside a running container.

