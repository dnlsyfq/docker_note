# MacOS

```
docker version
docker info
docker --version
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

