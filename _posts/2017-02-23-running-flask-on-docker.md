---
title: Running Flask app on Docker
---

This article explains running a Flask app inside a Docker container
and use it from the host machine.

Note: This article is not an intro to Docker.
For installing Docker check this link - https://docs.docker.com/engine/installation/

Docker getting started - https://docs.docker.com/engine/getstarted/


### Clome the repo and build the docker image
```
$ git clone git@github.com:goutham2027/flask-code.git
$ cd flask-docker
$ docker build -t flask:latest .
```

### Running the container and mapping to host post 80
```
docker run -d -p80:5000 flask:latest
```
Visit localhost to verify.
