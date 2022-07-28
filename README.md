<p align="center"><img src="https://raw.githubusercontent.com/MagicalStrangeQuark/MagicalStrangeQuark/master/assets/docker.svg" width="400"></p>

<p align="center">Sample <a href="https://www.docker.com">👉 Docker 👈</a> study documentation</p>

<p align="center">
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/license/Whopag/Docker">
    </a>
    <a href="#">
        <img alt="Languages" src="https://img.shields.io/github/languages/count/Whopag/Docker">
    </a>
	<a href="#">
        <img alt="Repository Size" src="https://img.shields.io/github/repo-size/Whopag/Docker">
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

<h6 align="center">Setting up Memory Limit in 128M and CPU to 0.5 Core</h6>

```bash
docker container run -d -p 8080:80 -m 128M --cpus 0.5 --name nginx nginx

docker container inspect --format='{{.HostConfig.Memory}}' nginx

docker container inspect --format='{{.HostConfig.NanoCpus}}' nginx
```

<h6 align="center">Update container CPU Usage on the Fly</h6>

```bash
docker container update --cpus 0.2 nginx
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

<h6 align="center">If we kill the entry point process, we kill the container, so we can use `ctrl + pq`</h6>

```bash
docker container run --name admiring_burnell -it ubuntu

docker container attach admiring_burnell
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
```

```bash
apt install wget
```

```bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```

```bash
source ~/.bashrc
```

```bash
nvm install node
```

```bash
node --version
```

```bash
exit
```

```bash
docker container commit -m "Adicionado nvm e wget" <container-id>
```

<h6 align="center">History</h6>

```bash
	docker image history <image-id>
```

<h6 align="center">Volumes</h6>

```bash
mkdir /Users/wesleyterres/Workspace/Docker/giropops
```

```bash
docker container run -it --mount type=bind,source=/Users/wesleyterres/Workspace/Docker/giropops,destination=/giropops ubuntu
```

```bash
docker container run -it --mount type=bind,source=/Users/wesleyterres/Workspace/Docker/giropops,destination=/giropops,ro ubuntu
```

```bash
docker volume create giropops
```

```bash
docker volume inspect giropops
```

```bash
docker volume rm giropops
```

```bash
docker volume prune
```

```bash
docker run -it --privileged --pid=host ubuntu nsenter -t 1 -a bash
```

```bash
ls /var/lib/docker/volumes/giropops/_data
```

```bash
touch BANANAS
```

```bash
touch APPLES
```

```bash
docker container run -it --mount type=volume,source=giropops,destination=/giropops ubuntu
```

```bash
docker container create -v /Users/wesleyterres/Workspace/Docker/giropops --name dbdados centos
```

```bash
docker container run -d -p 5432:5432 --name pgsql1 --volumes-from dbdados -e POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker kamui/postgresql
```

```bash
docker container run -it --mount type=volume,src=dbdados,dst=/data --mount type=bind,src=/opt/backup,dst=/backup ubuntu tar -cvf /backup/bkp-banco.tar /data
```

```bash
docker container run -ti --mount type=bind,src=/volume,dst=/volume ubuntu
```

```bash
docker container run -ti --mount type=bind,src=/root/primeiro_container,dst=/volume ubuntu
```

```bash
docker container run -ti --mount type=bind,src=/root/primeiro_container,dst=/volume,ro ubuntu
```

```bash
docker volume create giropops
```

```bash
docker volume inspect giropops
```

```bash
docker volume rm giropops
```

```bash
docker volume prune
```

```bash
docker container run -d --mount type=volume,source=giropops,destination=/var/opa  nginx
```

```bash
docker container create -v /data --name dbdados centos
```

```bash
docker run -d -p 5432:5432 --name pgsql1 --volumes-from dbdados -e POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker kamui/postgresql
```

```bash
docker run -d -p 5433:5432 --name pgsql2 --volumes-from dbdados -e  POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker kamui/postgresql
```

```bash
docker run -ti --volumes-from dbdados -v $(pwd):/backup debian tar -cvf /backup/backup.tar /data
```

<h4 align="center">Network</h4>

```bash
docker network create network-test
```

```bash
docker network ls
```

```bash
docker network inspect network-test
```

```bash
docker network rn network-test
```

```bash
docker pull postgres:latest
```

```bash
docker run --name some-postgres -e POSTGRES_PASSWORD=secret -p 5432:5432 -v "$($pwd)/data:/var/lib/postgresql/data" -d postgres:latest
```

<h6 align="center">Logs</h6>

```bash
docker container logs -f admiring_burnell
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

```bash
FROM ubuntu:latest

LABEL APP="ubuntu-server"

ENV APP_VERSION="1.0.5"

RUN apt-get update && apt-get install -y stress && apt-get clean

CMD stress --cpu 1 --vm-bytes 64M --vm 1
```

<h6 align="center">Remove all images</h6>

```bash
docker rmi -f $(docker images -aq)
```

<h6 align="center">Stop all running containers</h6>

```bash
docker stop $(docker ps -a -q)
```

<h6 align="center">Docker Shell vs. Exec Form</h6>

###### Shell form

```bash
FROM alpine:latest

# /bin/sh -c 'echo $HOME'
RUN echo $HOME

# /bin/sh -c 'echo $PATH'
CMD echo $PATH
```

###### Exec form

```bash
FROM alpine:latest

RUN ["pwd"]

CMD ["sleep", "1s"]
```

<h6 align="center">PgAdmin4</h6>

```bash
docker run --name db -p 5432:5432 -e POSTGRES_PASSWORD=password -d postgres:latest
```

```bash
sudo docker run -p 8080:80 --link db:postgres -e "PGADMIN_DEFAULT_EMAIL=wesleyfloresterres@gmail.com" -e "PGADMIN_DEFAULT_PASSWORD=password" -d dpage/pgadmin4:latest
```

<h4 align="center">Registry</h4>

<h6 align="center">Docker Hub</h6>

```bash
docker pull postgres:latest
```

```bash
docker image tag postgres:latest wesleyfloresterres/postgres:latest
```

```bash
docker login
```

```bash
docker image push wesleyfloresterres/postgres:latest
```

<h6 align="center">Localhost</h6>

```bash
docker container run -d -p 5000:5000 --restart=always --name registry registry:2

docker pull postgres:latest

docker image push localhost:5000/postgres:latest

curl localhost:5000/v2/_catalog

curl localhost:5000/v2/postgres/tags/list

docker container exec -it registry sh

ls /var/lib/registry/docker/registry/v2/repositories/postgres
```

<h4 align="center">Docker Machine</h4>

```bash
brew install docker-machine
```

```bash
docker-machine create --driver virtualbox giropops
```

```bash
docker-machine ip giropops
```

```bash
docker-machine ls
```

```bash
docker-machine rm giropops
```

docker-machine ssh giropops

<h6 align="center">Run this command to configure your shell:</h6>

```bash
eval $(docker-machine env giropops)
```
