# DevOps_Lab3

## Run app

```
npm install
npm start
```

## Build from Dockerfile

```
docker build -t lab03 .
```

## Build from Dockerfile

```
docker build -t lab03 .
```

## Create additional bridge network for the future container

```
docker network create dockerlab
```

## To run the container on local

```
docker run --net dockerlab -p 80:80 -d --name lab03 --rm --cpus=1 -m 512m --memory-reservation=256m lab03
```

## Creating a tag before pushing to Docker Hub:

```
docker tag lab03 yabecarp/lab03:dockerlab03
```

## Push And Pull the image to Dockerhub

```
docker login
docker push yabecarp/lab03:dockerlab03
```

```
docker pull yabecarp/lab03:dockerlab03
```

## To run a container from the pulled image:

```
docker run --net dockerlab -p 80:80 -d --name lab03 --rm --cpus=1 -m 512m --memory-reservation=256m yanecarp/lab03:dockerlab03
```

## Stop container

```
docker stop lab03
```
