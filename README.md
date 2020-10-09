<p align="center"><img src="docker.svg" width="400"></p>

<p align="center">Sample PHP Hello World app with  <a href="https://www.docker.com/">👉 Docker 👈</a></p>

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

<h4 align="center">Listing all Local Images</h4>

```bash
	sudo docker images
```