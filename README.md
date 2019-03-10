#Therapist Deployment
=============


Therapist area service for with several endpoints.


### How to run?
* Make sure you have PostGis server up and running on `localhost` 
* `docker run -p 5432:5432 --env POSTGRES_PASSWORD=therapist --env POSTGRES_DB=therapist --name postgis mdillon/postgis`
* `./mvnw clean install spring-boot:run`

### Create Docker image
* `./mvnw clean install dockerfile:build` or `./mvnw clean install -PbuildDocker -DskipTests`

### Push Docker image to Docker Hub
* `./mvnw clean install -Prelease`

### Run docker compose
* Go to /docker/test `/docker/docker-compose up`

### API Documentation

Docs can be found in swagger. Head to [/swagger-schema](http://localhost:8082/swagger-schema)
after server boots for raw schema or checkout [SwaggerUI](http://localhost:8082/swagger-ui.html) for nice interface

-------------


Links
* [Author's blog](http://rux.vc)
* [GitHub repo](https://github.com/ruXlab/kotlin-todo-server)

