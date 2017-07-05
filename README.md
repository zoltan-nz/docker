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

```
docker stack ls                                            # List stacks or apps
docker stack deploy -c <composefile> <appname>  # Run the specified Compose file
docker service ls                 # List running services associated with an app
docker service ps <service>                  # List tasks associated with an app
docker inspect <task or container>                   # Inspect task or container
docker container ls -q                                      # List container IDs
docker stack rm <appname>                             # Tear down an application
```