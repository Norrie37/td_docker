
# Useful Commands

## Commands

Display images:

```bash
docker images
```

Run docker instance:

```bash
docker run
docker run -it <image_name> <process>

#Example:
docker run -it centos:7 bash
```

To list available processes or images:

```bash
docker ps
docker ps -l # To see the latest running/exited image
docker ps -a # To see all running/exited images
```
