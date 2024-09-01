# Install Docker on Archlinux

### Install Docker

```shell
sudo pacman -S docker
```

### Docker Daemon

> if necessary

```shell
sudo systemctl enable docker
sudo systemctl start docker
```

### Get Permission Denied 

```shell
sudo groupadd docker
sudo usermod -aG docker $USER
# logout or
newgrp docker
```

### 도커 허브에 로그인

```shell
docker login --username $dockerId
```