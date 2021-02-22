# Deploying a simple Java App onto Docker

Here are the steps:
1. Create a springboot app with url /hello to say 'Hello Docker'
1. Add a Dockerfile
1. Build Docker image and tag it - 'docker build -t docker-springboot:v1 .'
1. List images 'docker images'.  Ensure the image shows up with the tag
1. Run the images 'docker run --publish 8080:8080 docker-springboot:v1'
1. Visit 'localhost:8080/hello', and it should display 'Hello Docker'
1. Identify the container ID using 'docker ps'
1. Stop the container using 'docker stop <imageIDFromAbove'


### Alternative using spring Buildpack: 
1. Image can also be built using 'mvn spring-boot:build-image'.  This creates the image and stores in local docker


### Alternative using google jib plugin:
1. It is trying to connect to gcr.io and failing.  Need to figure out whether it push to local docker image repo.

