# Docker
## Build

#docker build --build-arg target/bases-microservice-slim-0.0.1-SNAPSHOT.jar -t tbulubas/bases-microservice-slim .
docker build -t tbulubas/bases-microservice-slim .

docker image ls | grep bases

## Test
docker run -d -p 8080:8080 --name bases-microservice-slim tbulubas/bases-microservice-slim

docker container ls -a | grep bases

docker exec -it bases-microservice-slim bash

## Check
curl -X GET http://localhost:8080/books
