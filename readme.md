Docker:
--------------
nodejs application with mongodb for persistence with docker.
---
mongodb and mongo-express are configured in compose file: mongo.yaml
to start mongodb and mongo-express container:
    `docker compose -f mongo.yaml up`
    
to stop mongodb and mongo-express container:
    `docker compose -f mongo.yaml down`

docker-compose:
takes care of creating a netowk.

to start nodejs app, you can either <br>
    - push your app image and include it in the docker compose file <br>
    - run with `node server.js`

Dockerfile:
    - To containerize own application
    - FROM, ADD, COPY, RUN, CMD
    -could be multistage docker with multiple FROM 

docker-compose.yaml:
   
    - Structed file with multile docker commands.
    ex:
    ```
    mongo.yaml
    version: '3'
    services:  --> Lists the container to be creted.
        mongodb:
            image: mongo
        ports:
            -27017:27017
        environment:
            -MONGO-INITDB_ROOT_USERNAME=admin
            -MONGO_INITDB_ROOT_PASSWORD=password ```

ECR: Elastic Container Registry.
