# Building-SpringBoot-MicroServices
This repository deals with the highlighting of the importance of Microservices in real world scenarios by building them from scratch to building Apache Kafka and RabbitMq  to handle real streaming data

## Introduction
### What are Microservices? 
Microservices allow large applications to be split into smaller pieces that operate independently. Each 'piece' has its responsibilities and can carry them out regardless of what the other components are doing.  In other words it can also be defined as small, independent components that you can combine to build larger applications. These components can be rescaled, debugged and built independently which increases the rescalability and debugging , testing processes of traditional Monolithic applications will be light weighted. 

### Differences between Microservice Architecture and Monolithic Architectures
![Image showing differences between MicroService and Monolithic Architecture](https://github.com/srinathsai/Building-SpringBoot-MicroServices/blob/main/differences%20between%20monolithic%20and%20micoservices.png)

## Features of Microservices that were explored :
  - Load Balancing between Using Spring service registry.
  - Routing of APIs with Spring cloud's API gateway.
  - Externalization of configuration with the help of Spring config server.
  - Distributed tracing of an API request from starting to ending of it using Spring Micrometer.
  - The 3 ways called RestTemplate, Spring cloud openFeign and webclient are analyzed for handling the APIs request between Microservices.
  - Minimization of sending Post request of refresh by using Spring bus.
  - Apache Kafka and RabbitMQ message brokers are tested for handling real live streaming data.

## Requirements :
  - Intellij Idea or any Java IDE.
  - Postman Client.
  - Docker Desktop, Docker Hub.
  - JDK with a version of 17 and 17+ installed in pc.
  - MySQL.

## Implementation :
### Initial process - 
  - At first required number of independent springboot projects which will be independent microservices are built with necessary dependencies from Spring initializer.  In my case Employee service, organization service and department service are 3 individual springBoot Microservices that were developed and explored all the features of Micorservices on these 3 core springboot projects.
  - Create 3 seperate databases one for each in MySQL. (Because each independent Microservice can have it's own database).
  - Configure all these applications.properties files to respective dbs that were created in above step.
  - For each of 3 springboot projects develop necessary Rest APis . I have developed 2 api request methods for each one is for saving entity in database (Push request), next is get request. These 2 api request methods are built fro each springboot project using DTO and mappers.
  - Remember all these 3 springboot server.ports in application.properties must be different because being different servers allows us to run them simultaneously.
  - Check your logic of your api requesting methods using postMan for GET requests if you designed any or check for records in 3 databases for POST requests if you designed any.
  - Once the logic of all your api request methods are correct, now we can explore all the features of the Microservices which are as below :
