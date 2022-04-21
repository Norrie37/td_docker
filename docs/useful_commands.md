
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

## SCP commands

SCP command to compy from local to remote:

```bash
scp file.txt remote_username@10.10.0.2:/remote/directory # File Copy
scp -r /local/directory remote_username@10.10.0.2:/remote/directory # Directory Copy
```

For instance:

```bash
scp -r app ocp@152.67.101.182/home/
```
