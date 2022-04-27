# AUTOMATION || USE DOCKER COMPOSE
## RUN DOCKER COMPOSE
```
docker-compose up
```

## STOP DOCKER COMPOSE
```
docker-compose down --rmi all -v
```

## Clear volume
```
docker volume rm $(docker volume ls -q)
```

# MANUAL TERMINAL
## Start
```
docker start [name_container]
```

## Stop
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

## CHECK CONTAINER (Running)
```
docker ps -a
```

## FOR DEVELOPING

### Run and want delete after stop
```
docker run --name [name_container] -p 4000:4000 --rm  [images]:[tag]
```

### Run and Use Volume
```
docker run --name [name_container] -p 4000:4000 --rm -v [relative_path]:/app -v /app/node_modules [images]:[tag]
```