# Docker CookBook

## 1. Getting Started with Docker
>1.1. Installing Docker

```
sudo apt-get update
sudo apt-get install -y docker.io
sudo docker --version

```
Fix error in WSL Ubuntu on Window11
```bash
#System has not been booted with systemd as init system (PID 1). 
#Can't operate. Failed to connect to bus: Host is down
# https://askubuntu.com/questions/1379425/system-has-not-been-booted-with-systemd-as-init-system-pid-1-cant-operate

# Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json": dial unix /var/run/docker.sock: connect: permission denied
sudo chmod 666 /var/run/docker.sock
```

## 1.2. Running Hello World in Docker
```
sudo docker run busybox echo hello world
docker ps
docker ps -a
docker images
docker run -t -i ubuntu:20.10 /bin/bash

```