<p align="center"><img src="docker.svg" width="400"></p>

<p align="center">Sample <a href="https://www.docker.com/">👉 Docker 👈</a> study documentation</p>

<p align="center">
    <a href="https://opensource.org/licenses/MIT">
        <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/languages/count/MagicalStrangeQuark/DockerPHPHelloWorld">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/last-commit/MagicalStrangeQuark/DockerPHPHelloWorld">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/followers/MagicalStrangeQuark?style=social">
    </a>
</p>

<h2 align="center">Website</h2>

<h3 align="center">
    <a href="https://www.docker.com">https://www.docker.com</a>
</h3>

<h3 align="center">
    <a href="https://hub.docker.com">Docker Hub</a>
</h3>

<h4 align="center">Installing</h4>

```bash
	sudo pacman -Sy docker
```

<h4 align="center">Starting Service</h4>

```bash
	sudo systemctl start docker.service
```

<h4 align="center">Stopping Service</h4>

```bash
	sudo systemctl stop docker.service
```

<h4 align="center">Starting On System Boot</h4>

```bash
	sudo systemctl enable docker.service
```

<h4 align="center">Testing the Installation</h4>

```bash
	docker -v || docker --version || docker version

	sudo docker run hello-world
```

<h4 align="center">Listing all local images</h4>

```bash
	docker images
```

<h4 align="center">Running NGINX image</h4>

```bash
	docker pull nginx || docker pull nginx:stable
```

```bash
	docker container run --publish 8080:80 --detach --name webserver nginx
```

```bash
	firefox --new-tab http://127.0.0.1:8080/
```

<h4 align="center">Show running container(s)</h4>

```bash
	sudo docker container ls
```

<h4 align="center">Show detailed information about Docker process</h4>

```bash
	sudo docker info
```

<h4 align="center">Stopping a Docker container</h4>

```bash
	sudo docker container stop <id>
```

<h4 align="center">Show Docker help</h4>

```bash
	sudo docker --help
```

<h4 align="center">Remove one of more container(s)</h4>

```bash
	sudo docker container rm [<id> <id> <id> ...]
```

<h4 align="center">Restart a stopped process</h4>

```bash
	sudo docker container start [<id> <id> <id> ...]
```

<h4 align="center">Show container processes</h4>

```bash
	sudo docker container top <id>
```

<h4 align="center">Show processes details</h4>

```bash
	sudo docker container inspect <id>
```

<h4 align="center">Show performace statistics of a container</h4>

```bash
	sudo docker container stats <id>
```

<h4 align="center">Ubuntu</h4>

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

<h4 align="center">Run a command inside a container without enter in</h4>

```bash
	sudo docker container exec <container-id> <command>
```

```bash
	sudo docker container exec 8e83ad7f335e ls -lh
```