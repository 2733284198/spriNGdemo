# Spring Boot 2.0 Demo with Angular 4

This project is the Spring version of https://github.com/marco76/java-demo
The scope of the application is to show the new features of the next version of Spring.
Angular 4 (Angular CLI) is used to communicate with the server.
This architecture is one of the most common in the professional environnements:
Spring <--> REST Services <--> Angular (JS Framework)


## Features


- Spring Boot 2.0 features
- - Bean Validation 2.0 (alpha)

## How to install

__Prerequisites__

- you need maven, npm, git

__Production mode__

- clone the git project
from the root of the project launch mvn package this generates a package named ROOT.war in the PROJECT/server/target directory
you can deploy this package in your favourite application server. The Angular application should answer at the requests to http://localhost:8080
Development mode

__Development mode__

- clone the git project
You can start the server using your favourite IDE. The project uses a standard Maven directory structure. You need to configure the server to deploy the server.war artifact.
from the PROJECT/client/src directory install the npm packages : npm install
launch the client with ng serve. The client uses the port 4200 (default for Angular CLI) and you can navigate to http://localhost:4200

__Docker image__
 
 You can find the docker image here : https://hub.docker.com/r/javaee/java-demo/
 
 The docker image install a linux distribution, download the sources and the required libraries and application server (custom edition).
 It compiles the sources codes and deploy the application on the port 80.
 
 You can run it with this instruction: docker run --rm -it -p 80:80  javaee/java-demo
 
## How the code is organized
The code structure has been adapted to easily found the ressources of the demo and doesn't follow the best practices for an enterprise project.

The package _io.springdemo.common.web_ contains common classes for the infrastructure of the project.

The package _io.springdemo.examples_ contains the specific code used for each example. The code is grouped by feature (beans, DTO, resources, services together) and not on technical layers.