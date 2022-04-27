# AUTOMATION || USE DOCKER COMPOSE
## RUN DOCKER COMPOSE
```
docker-compose up
```

## STOP DOCKER COMPOSE
```
docker-compose down --rmi all -v
```

## CLEAR VOLUME
```
docker volume rm $(docker volume ls -q)
```

# MANUAL TERMINAL
## START
```
docker start [name_container]
```

## STOP
```
docker stop [name_container]
```

## CHECK IMAGES
```
docker images
```

## BUILD IMAGES
```
docker build -t [name_images]:[tag] [directory]
```

## DELETE IMAGES
```
docker image rm [name_images]
```

## CHECK CONTAINER (Running)
```
docker ps -a
```

## FOR DEVELOPING

### RUN AND WANT DELETE AFTER STOP 
```
docker run --name [name_container] -p 4000:4000 --rm  [images]:[tag]
```

### RUN AND USE VOLUME
```
docker run --name [name_container] -p 4000:4000 --rm -v [relative_path]:/app -v /app/node_modules [images]:[tag]
```

## Sharing Images on Docker Hub
```
docker build -t [username_docker]/[name_repo_docker] [directory]
docker login
docker push [username_docker]/[images]:[tagname]
```