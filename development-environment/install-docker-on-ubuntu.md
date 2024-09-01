# Install Docker on Ubuntu

https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository

### Change to Bash
```shell
bash
```

### Set up Docker's `apt` repository

```shell
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

### Install the Docker packages

```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### Verify that the Docker Engine installation is successful by running the `hello-world` image

```shell
sudo docker run hello-world
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