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
  * Networking (To communicate with other containers and host)
  * Dependencies
  * Operating System (Carved from Host-OS)

Docker:

1. sets up containers
2. monitors it, and
3. tears it down when it's no longer needed

Docker is a:

* client program (i.e. a command that you type at the terminal)

* server program (i.e. it can manage a Linux system)

* program that builds containers from code

* service that distributes containers (i.e. allows sharing of containers)

* company that facilitates and manages the docker ecosystem

## Docker Flow - How to Work with Containers

## Build Docker Images

## Docker Networking, ETC
