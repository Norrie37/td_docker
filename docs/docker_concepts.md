# Docker Concepts

## Intro to Docker

General introduction to Docker:

* Docker carves up a host-OS or computer into sealed containers that run your code.

* Containers are portable and can ship code via systems

* Docker can be used to build and share containers.

Note: Docker Containers are not VMs. There's only the host OS running - which is carved up into isolated containers.

### Container

A container is:

* Self-contained sealed unit of software

* Container contains everything required to run the code

* A container has all the:
  * Code
  * Configs
  * Processes
  * Networking *(To communicate with other containers and the host)*
  * Dependencies
  * Operating System *(Carved from Host-OS)*

Docker:

1. sets up containers
2. monitors it, and
3. tears it down when it's no longer needed

Docker is a:

* client program *(i.e. a command that you type at the terminal)*

* server program *(i.e. it can manage a Linux system)*

* program that builds containers from code

* service that distributes containers *(i.e. allows sharing of containers)*

* company that facilitates and manages the docker ecosystem

## Docker Flow - How to Work with Containers

Info: This section is about what docker does

### Image

In docker it all begins with an ***image***. An image is:

* every file that makes up just enough of the OS to do what you neeed to do.

The ***docker run*** command takes an image and turns it into a living, running **container** with a **process** in it that's doing something.

Example on how to run an image:

```bash

docker run -it centos:7 bash
```

Generally, we initiate docker run to proceed to the next phase of docker flow, which is a **Running Container**.

### Running Container

A **running container** is container derived from an image. You move to a **stopped container** when you exit a running container.

### Stopped Container

Stopped containers are not seen by default.
To see a stopped container, enter the following command:

```bash
docker ps -a # -> To see all containers
docker ps -l # -> To see the last running container
```

When a process exists the file/container is still there.

## Build Docker Images

Stopped containers can be used to build images.
Say you have a container that has a file in it which you wish to use in the future:

* Started from a base image
* Installed own software
* Have a container that has custom software installed on it

We use the ***docker commit*** to build images. So ***docker run*** and ***docker commit*** are complementary to each other:

* ***Docker run*** creates containers from an image. And ***Docker commit*** takes stopped containers and builds new images out of them.

Docker commit doesn't overwrite the original image, it acts as a template for a new image.

```bash
docker commit <image-id>
```

### Tagging

When creating a new docker image, the image-ID is usually very long. It is recommended to tag the new image so that you can reference the image via the tag - instead of the image ID.

```bash
docker tag <new-image-id> <tag-name>
```

Recommended shortcut:

```bash
docker commit <image-id> <new-image>
```

## Running Processes in Containers

***Docker run*** gives an image name and the process to run in that container.

## Docker Networking, ETC

