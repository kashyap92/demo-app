Docker:
--------------
nodejs application with mongodb for persistence with docker.
--
Dockerfile:
    - To containerize own application
    - FROM, ADD, COPY, RUN, CMD
    -could be multistage docker with multiple FROM 

docker-compose:
takes care of creating a netowk.

docker-compose.yaml:
    - Structed file with multile docker commands.
    ex:
    mongo.yaml
    version: '3'
    services:  --> Lists the container to be creted.
        mongodb:
            image: mongo
        ports:
            -27017:27017
        environment:
            -MONGO-INITDB_ROOT_USERNAME=admin
            -MONGO_INITDB_ROOT_PASSWORD=password

Execute: 'docker-compose -f mongo.yaml up'
ECR: Elastic Container Registry.
