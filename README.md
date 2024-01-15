This repository contains the code and resources to understand docker, where I explore Docker from absolute zero to advanced concepts.

## Table of Contents

- [Part 1: Introduction to Docker](#part-1-introduction-to-docker)
  - [Problem Statement](#problem-statement)
  - [Installation](#installation)
  - [Understanding Images vs Containers](#understanding-images-vs-containers)
  - [Running Ubuntu Image in a Container](#running-ubuntu-image-in-a-container)
  - [Managing Containers](#managing-containers)
  - [Docker Compose](#docker-compose)
  - [Port Mapping](#port-mapping)
  - [Environment Variables](#environment-variables)
- [Part 2: Dockerization of Node.js Application](#part-2-dockerization-of-nodejs-application)
  - [Dockerfile](#dockerfile)
  - [Caching Layers](#caching-layers)
  - [Publishing to Docker Hub](#publishing-to-docker-hub)

## Part 1: Introduction to Docker

### Problem Statement

Docker simplifies the process of packaging, shipping, and running applications in isolated environments. This course aims to cover Docker fundamentals and advanced usage.

### Installation

Install Docker CLI and Desktop by following the instructions on the [official Docker website](https://www.docker.com/get-started).

### Understanding Images vs Containers

In Docker, an image is a lightweight, standalone, and executable package that includes everything needed to run a piece of software, including the code, runtime, libraries, and dependencies. A container is a running instance of an image.

### Running Ubuntu Image in a Container

docker run -it ubuntu
This command runs an interactive Ubuntu container.

Managing Containers

docker containers ls
docker containers ls -a
docker start <container_name>
docker stop <container_name>
docker exec -it <container_name> /bin/bash
These commands list, start, stop, and execute a command in a running container interactively.

Docker Compose
Docker Compose is a tool for defining and running multi-container Docker applications. It uses a YAML file to configure application services.

Port Mapping
docker run -it -p 6000:6000 <container_name>
docker run -it -p 6000:9000 <container_name>
These commands demonstrate port mapping between the host and the container.

Environment Variables
docker run -it -e HOST=8000 -p 8000:8000 <container_name> .
This command sets an environment variable during container creation.

Part 2: Dockerization of Node.js Application
Dockerfile
The Dockerfile provides instructions for building a Docker image for a Node.js application.

Caching Layers
Docker uses caching layers to speed up the build process by reusing previously built layers.

Publishing to Docker Hub
Before publishing, log in to Docker Hub using the following command:
docker login
Use the following command to publish the image:
docker push <image_name>

Docker Compose
Services
Docker Compose allows defining multiple services for an application in a single file.

Port Mapping
Port mapping in Docker Compose is specified in the docker-compose.yml file.

Environment Variables
Environment variables for services in Docker Compose are defined in the docker-compose.yml file.
