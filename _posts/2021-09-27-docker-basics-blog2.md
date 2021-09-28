---
layout: post
title:  "2. Docker Basics"
date:   2021-09-28 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head></html>

# Docker Basics

![docker logo](/images/docker-logo.jpg)

`Docker` is an open-source, PaaS (Platform as a Service) used for containerization through the utilization of OS-level virtualization directly in the Linux kernal. Similar to a Virtual Machine, Docker is able to run applications in a `sandbox environment` in order for developers to easily test and play with their applications in a consistent and secure environment. 

The advantage of using containers rather than a dedicated VM would be the reduction of used kernal space compared to the higher CPU usage that a VM uses when utilizing their own individual OS. This advantage can be visualized when viewing a Virtual Machine as a standalone environment that host "virtual hardware" which includes setting up its own BIOS, disk storage, CPU, RAM, etc. In comparison, a container uses the host's hardware and Operating System through the usage of the Docker Engine.

<br />

# Docker Components

![docker 3 components](/images/docker-3-components.png)

> **Note:** The three componets that are needed to run Docker's System are a `build component`, the `run component,` and the `distribution component`. These components correspond to the three vital Docker tools: images, containers, and the engine. 

## Docker Images
    [x] build component
    [ ] run component
    [ ] distribution component

- A Docker Image is a collection of read only files that contain tools, such as libraries and dependancies, that are necessary to run and configure the corresponding container. 
- An image is created through the usage of files that are known as `layers` that are dependant on the layer it is built on top of. These layers are "laid" on top of each other after each subsequent image-to-container creation and stores the history and changes to the container over time. 

![docker image layers](/images/docker-image-layers.jpg)

> **Note:** A Docker Image can be created from an existing image or through the creation of a Dockerfile (explained below).

## Docker Containers
    [x] build component
    [x] run component
    [ ] distribution component 

- Containers are real and live enviroments that are interactable with users and adminstrators. These environments can host applications that are abstracted from After creation, our Docker Containers (environments) are able to start up, stop, run, be moved, and be deleted.

## Docker Engine
    [x] build component
    [x] run component
    [x] distribution component 

- With these three components working in conjuntion, a service called the `Docker Engine` (or the Docker Daemon) is able to run on the user's host machine and performs all the actions necessary in order to build, run, and distribute the selected Docker Container. This daemon is able to listen for Docker API request and manages Docker's tools for the client

<br />

# DockerFile

A `Dockerfile` is essentially a simple text document that contains the instructions and commands that a user would normally run on their command line and instead the Dockerfile uses those commands together in order to automate the image creation process. 

```
$ docker build
```

The docker build command is able to create an image from a Dockerfile alongside a provided recursively processed context. This `context` would be the  `Path` (the filesystem location) or `URL` (Git repository location). `Build` is not run by the Command Line Interface (CLI) but rather by the Docker daemon. The context is sent to the daemon first and files are used according to the instructions inside of the Dockerfile.  A Dockerfile is able to be moved throughout your file system with the following command: 

```
$ docker build -f /path/to/your/Dockerfile
```
Every Dockerfile line begins with a `FROM` isntruction and follows an "instruction argument" format, which is then read by Docker in sequential order.
The following instructions are supported by Docker and are to be followed with their corresponding environemnt variables.
```
ADD
COPY
ENV
EXPOSE
FROM
LABEL
ONBUILD
STOPSIGNAL
USER
VOLUME
WORKDIR
```

---
## References

Basics of Docker [https://contribute.docker.com/docs/communityleaders/eventhandbooks/react/basics/](https://contribute.docker.com/docs/communityleaders/eventhandbooks/react/basics/)
<!-- ^ this is the useful one -->
Docker [https://www.ibm.com/cloud/learn/docker](https://www.ibm.com/cloud/learn/docker) 
<!-- ^ this one didnt have that much useful info actually -->
Docker Image [https://jfrog.com/knowledge-base/a-beginners-guide-to-understanding-and-building-docker-images/]

DockerFile [https://docs.docker.com/engine/reference/builder/](https://docs.docker.com/engine/reference/builder/)

Docker vs. VM [https://runnable.com/docker/why-use-docker](https://runnable.com/docker/why-use-docker)