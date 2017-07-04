DOCKER EXPERIMENT
=================

```
docker run hello-world
docker build -t friendlyhello .
docker images
docker run --publish 4000:8080 freindlyhello
docker run --detach --publish 4000:8080 friendlyhello
docker container ls
docker ps
docker stop 1234
docker login
docker tag image username/repository:tag
docker push username/repository:tag
docker run -p 4000:8080 username/repository:tag
docker image rm username/repository:tag
```