# MacOS

```
docker version
docker info
docker --version
docker-compose --version
```

```
docker login
```

```
docker run hello-world
```

* see all available docker images
```
docker images
```

* see docker running
```
docker ps
```

* find image in docker hub image
```
https://hub.docker.com/search?q=docker%20airflow&type=image&page=2
https://hub.docker.com/r/puckel/docker-airflow
docker pull puckel/docker-airflow
docker run -d -p 8080:8080 puckel/docker-airflow webserver
docker ps
```

```
docker run -it --rm -p 8888:8888 jupyter/datascience-notebook
```

```
docker build -t <name> .
docker images
docker run -d -p 5000:5000 <name>
docker ps
docker tag python-helloworld dnlsfq/python-helloworld:v1.0.0
docker push dnlsfq/python-helloworld:v1.0.0
```

* dir
```
Dockerfile
app.py
requirements.txt
test_with_pytest.py
```

* Dockerfile
```
FROM python:3.8
LABEL maintainer="Katie Gamanji"

COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt

# command to run on container start
CMD [ "python", "app.py" ]
```

# Linux distro

```
systemctl status docker
systemctl stop docker
systemctl start docker
```

* starting up
```
sudo dockerd
```

# Windows

```
docker run --name repo alpine/git clone https://github.com/docker/getting-started.git
docker cp repo:/git/getting-started/ .
cd getting-started
docker build -t docker101tutorial .
docker run -d -p 80:80 --name docker-tutorial docker101tutorial
docker tag docker101tutorial dnlsfq/docker101tutorial
docker push dnlsfq/dockertutorial
```

### docker with download image 
```
search image at docker hub
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=<PASSWORD> -d mysql:Tag
docker start some-mysql
docker ps
```

```
docker run -p 3307:3306 --name my-mysql -e MYSQL_ROOT_PASSWORD=<PASSWORD> -d mysql/mysql-server:5.7
docker exec -it my-mysql /bin/bash

mysql -uroot -p -P3307 -h127.0.0.1
```

```
docker run -d --name mysqldb -p 3306:3306 -e MYSQL_ROOT_PASSWORD=<PASSWORD> mysql:latest
docker ps
docker stop
```

### docker with build image
```
docker image build -t dnlsfq/gsd:first-ctr . 
docker image ls
docker image push dnlsfq/gsd:first-ctr
docker image rm dnlsfq/gsd:first-ctr
docker container run -d --name web -p 8000:8080 dnlsfq/gsd:first-ctr
docker container ls
docker container stop web
docker container start web
docker container rm web
```

### docker with yml

```
docker-compose.yml
docker-compose up
```

```
docker-compose -f docker-compose-LocalExecutor.yml up -d
```

### docker ignore file
file that dont want to include in the container

.dockerignore
```
node_modules
npm-debug.log
```

### docker file
create an image based on instructions

Dockerfile
```
```

### docker create image

```
docker build -t <name> .
docker build -t algofields/simple-backend .
```
### docker see all images

```
docker images
```

### docker delete images

```
docker rmi <4 char image id>
docker rmi <4 char image id>-f
```

### docker run container from image 

```
docker run  -p <port number>:<port number> <image name>
docker run -p 4000:4000 algofields/simple-backend
```
### docker see container

```
docker ps
```

### docker stop container

```
docker stop <docker container id>
```

### push image to docker hub

```
docker push 
docker pull
```

## docker compose
manage multiple containers

### create docker compose

docker-compose.yml
```

```

# docker file sharing
windows 10 disable wsl2 option in docker
```
C:\Users\<name>\AppData\Roaming\Docker\<settings.json>
```
