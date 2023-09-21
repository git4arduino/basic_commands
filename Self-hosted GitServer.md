# 10 Self-hosted Git-Server

```
sudo apt-get update

sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

```
sudo docker run hello-world
```

```
sudo apt install docker-compose
```

```
cd /usr/local/sbin
mkdir gitea
cd gitea
```

```
nano docker-compose.yml
```

```
version: "3"

services:
  gitea:
    image: gitea/gitea
    container_name: gitea
    environment:
      - USER_UID=1000
      - USER_GID=1000
    restart: always
    volumes:
      - ./gitea:/data
      - /etc/timezone:/etc/timezone:ro
      - /etc/localtime:/etc/localtime:ro
    ports:
      - "3001:3000"
      - "222:22"
```

```
docker-compose up -d

http://159.60.1.1:3001/
```

## NGINX Reverse Proxy Manager

```
cd /usr/local/sbin
mkdir nginxpm
nano docker-compose.yml
```

```
version: '3.8'
services:
  app:
    image: 'jc21/nginx-proxy-manager:latest'
    restart: unless-stopped
    ports:
      - '80:80'
      - '81:81'
      - '443:443'
    volumes:
      - ./data:/data
      - ./letsencrypt:/etc/letsencrypt
```

```
docker-compose up -d

http://159.69.117.69:81
```

```
Standardzugangsdaten
	Email:    admin@example.com
	Password: changeme
```
