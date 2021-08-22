<p align="center"><img src="docker.svg" width="400"></p>

<p align="center">Sample <a href="https://www.docker.com">👉 Docker 👈</a> study documentation</p>

<p align="center">
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/license/Whopag/Docker">
    </a>
    <a href="#">
        <img alt="Languages" src="https://img.shields.io/github/languages/count/Whopag/Docker">
    </a>
    <a href="#">
        <img alt="Last Commit" src="https://img.shields.io/github/last-commit/Whopag/Docker">
    </a>
</p>

<h6 align="center">Website</h6>
    
<p align="center">
	<a href="https://www.docker.com">https://www.docker.com</a>
</p>

<h6 align="center">Docker Hub</h6>

<p align="center">
    <a href="https://hub.docker.com">https://hub.docker.com</a>
</p>

<h6 align="center">Installing On Manjaro</h6>

```bash
	pacman -Sy docker
```

<h6 align="center">Starting Service</h6>

```bash
	systemctl start docker.service
```

<h6 align="center">Stopping Service</h6>

```bash
	systemctl stop docker.service
```

<h6 align="center">Starting On System Boot</h6>

```bash
	systemctl enable docker.service
```

<h6 align="center">Testing the Installation</h6>

```bash
	docker -v || docker --version || docker version
```

```bash
	docker container run -it hello-world
```

<h6 align="center">Listing all local images</h6>

```bash
	docker images
```

<h6 align="center">Running NGINX image</h6>

```bash
	docker pull nginx:stable
```

```bash
	docker container run --publish 8080:80 --detach --name webserver nginx
```

```bash
	firefox --new-tab http://127.0.0.1:8080
```

<h6 align="center">Show running container(s)</h6>

```bash
	docker container ls
```

<h6 align="center">Show detailed information about Docker process</h6>

```bash
	docker info
```

<h6 align="center">Show Docker help</h6>

```bash
	docker --help
```

<h6 align="center">Stopping a Docker container</h6>

```bash
	docker container stop <id>
```

<h6 align="center">Remove one of more container(s)</h6>

```bash
	docker container rm [<id> <id> <id> ...]
```

<h6 align="center">Remove one of more image(s)</h6>

```bash
	docker rmi [<id> <id> <id> ...]
```

<h6 align="center">Restart a stopped process</h6>

```bash
	docker container start [<id> <id> <id> ...]
```

<h6 align="center">Show container processes</h6>

```bash
	docker container top <id>
```

<h6 align="center">Show processes details</h6>

```bash
	docker container inspect <id>
```

<h6 align="center">Show performace statistics of a container</h6>

```bash
	docker container stats <id>
```

<h6 align="center">Ubuntu</h6>

```bash
	docker pull ubuntu

	docker container run -it --name ubuntu ubuntu /bin/bash
	
	apt-get update

	apt-get install git

	git --version

	exit

	docker container start <ubuntu-container-id>

	docker container attach <ubuntu-container-id>
```

<h6 align="center">Run a command inside a container without enter in</h6>

```bash
	docker container exec <container-id> <command>
```

```bash
	docker container exec 8e83ad7f335e ls -lh
```

<h6 align="center">Rename a container</h6>

```bash
	docker container rename <old-container-name> <new-container-name>
```

<h6 align="center">Remove all stopped container(s)</h6>

```bash
	docker container prune
```

<h6 align="center">Remove all images</h6>

```bash
	docker system prune -a
```

<h6 align="center">Cloud9</h6>

```bash
	docker pull linuxserver/cloud9
```

<h6 align="center">Commit</h6>

```bash
	docker container run -it ubuntu

	apt install wget

	wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash

	source ~/.bashrc

	nvm install node

	node --version

	exit

	docker container commit -m "Adicionado nvm e wget" <container-id>
```

<h6 align="center">History</h6>

```bash
	docker image history <image-id>
```

<h6 align="center">Network</h6>

```bash
	docker network create network-test

	docker network ls

	docker network inspect network-test

	docker network rn network-test
```

```bash
	docker pull postgres:latest
	
	docker run --name some-postgres -e POSTGRES_PASSWORD=secret -p 5432:5432 -v "$($pwd)/data:/var/lib/postgresql/data" -d postgres:latest
```

<h6 align="center">Dockerfile</h6>

```Dockerfile
	FROM ubuntu:latest
	LABEL maintainer="Wesley Flôres"
```

```bash
	docker build -t wesleyflores/ubuntu:latest .
```

```bash
	docker build -t wesleyflores/ubuntu:latest Dockerfile
```