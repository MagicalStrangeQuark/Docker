<p align="center"><img src="docker.svg" width="400"></p>

<p align="center">Sample <a href="https://www.docker.com/">👉 Docker 👈</a> study documentation</p>

<p align="center">
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/license/Whopag/Docker">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/languages/count/Whopag/Docker">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/last-commit/Whopag/Docker">
    </a>
</p>

<h2 align="center">Website</h2>
    
<p align="center">
	<a href="https://www.docker.com">https://www.docker.com</a>
</p>

<p align="center">
    <a href="https://hub.docker.com">https://hub.docker.com</a>
</p>

<h6 align="center">Installing</h6>

```bash
	sudo pacman -Sy docker
```

<h6 align="center">Starting Service</h6>

```bash
	sudo systemctl start docker.service
```

<h6 align="center">Stopping Service</h6>

```bash
	sudo systemctl stop docker.service
```

<h6 align="center">Starting On System Boot</h6>

```bash
	sudo systemctl enable docker.service
```

<h6 align="center">Testing the Installation</h6>

```bash
	docker -v || docker --version || docker version

	sudo docker run hello-world
```

<h6 align="center">Listing all local images</h6>

```bash
	docker images
```

<h6 align="center">Running NGINX image</h6>

```bash
	docker pull nginx || docker pull nginx:stable
```

```bash
	docker container run --publish 8080:80 --detach --name webserver nginx
```

```bash
	firefox --new-tab http://127.0.0.1:8080
```

<h6 align="center">Show running container(s)</h6>

```bash
	sudo docker container ls
```

<h6 align="center">Show detailed information about Docker process</h6>

```bash
	sudo docker info
```

<h6 align="center">Stopping a Docker container</h6>

```bash
	sudo docker container stop <id>
```

<h6 align="center">Show Docker help</h6>

```bash
	sudo docker --help
```

<h6 align="center">Remove one of more container(s)</h6>

```bash
	sudo docker container rm [<id> <id> <id> ...]
```

<h6 align="center">Remove one of more image(s)</h6>

```bash
	sudo docker rmi [<id> <id> <id> ...]
```

<h6 align="center">Restart a stopped process</h6>

```bash
	sudo docker container start [<id> <id> <id> ...]
```

<h6 align="center">Show container processes</h6>

```bash
	sudo docker container top <id>
```

<h6 align="center">Show processes details</h6>

```bash
	sudo docker container inspect <id>
```

<h6 align="center">Show performace statistics of a container</h6>

```bash
	sudo docker container stats <id>
```

<h6 align="center">Ubuntu</h6>

```bash
	docker pull ubuntu

	sudo docker container run -it --name ubuntu ubuntu /bin/bash
	
	apt-get update

	apt-get install git

	git --version

	exit

	docker container start <ubuntu-container-id>

	docker container attach <ubuntu-container-id>
```

<h6 align="center">Run a command inside a container without enter in</h6>

```bash
	sudo docker container exec <container-id> <command>
```

```bash
	sudo docker container exec 8e83ad7f335e ls -lh
```

<h6 align="center">Rename a container</h6>

```bash
	sudo docker container rename <old-container-name> <new-container-name>
```

<h6 align="center">Remove all stopped container(s)</h6>

```bash
	sudo docker container prune
```

<h6 align="center">Remove all images</h6>

```bash
	sudo docker system prune -a
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