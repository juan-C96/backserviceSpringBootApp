# ShipSpringBootApp

This project is a spacecraft management application that allows performing CRUD (Create, Read, Update and Delete) operations on an H2 database. Currently, Postman is used to verify its operation until the interface instructions are ready.

## Features

- **Spaceship Management:** Allows you to add, view, modify, and delete spaceships.
- **Robust Backend:** Implemented in Spring Boot, providing a RESTful API to handle CRUD operations.
- **Microservices Registry:** Integration with Eureka Server for service registration and discovery.
- **In-Memory Database:** Uses H2 for fast and easy storage during development.

## Technologies Used

- **Backend:** Spring Boot
- **Database:** H2
- **Containerization:** Docker and Docker Compose
- **Microservices:** Eureka Server

## Related Projects

### Ship Boot

The **ShipBoot** project is located in a separate repository, where you can find the implementation details and source code for the spaceship management application.

- Repository Link: [ShipBoot Repository](https://github.com/juan-C96/ShipSpringBootApp)

## Dependencies 

### Java Version 

- **Java:** 23 

### Eureka Server

The **EurekaServer** project uses the following dependencies: 

- **Spring Boot Starter Parent:** 3.3.5 
- **Spring Boot Starter Web** 
- **Spring Cloud Starter Netflix Eureka Server** 
- **Spring Cloud Starter Netflix Eureka Client** 
- **Spring Boot Starter Test** 

### Ship Boot 

The **ShipBoot** project uses the following dependencies: 

- **Spring Boot Starter Parent:** 3.3.5 
- **Spring Boot Starter Data JPA** 
- **Spring Boot Starter Web** 
- **Spring Boot DevTools** 
- **H2 Database** 
- **Spring Boot Starter Test** 
- **Spring Boot Starter AOP** 
- **Spring Cloud Starter Netflix Eureka Client** 

### Spring Cloud Versions

- **Spring Cloud Dependencies:** 2023.0.3

### Notes

- Spring Boot and Spring Cloud dependency versions are configured through dependency management, meaning that the versions are managed by the `spring-boot-starter-parent` and `spring-cloud-dependencies`.

## Installation

To run this project locally, make sure you have [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/) installed. Then, follow these steps:

1. Clone the repository.
2. Run `docker-compose up` to build and run the services.

## Usage

Once the application is up and running, you will be able to access:

- **Eureka Server:** [http://localhost:8761](http://localhost:8761)
- **Ship CRUD application:** [http://localhost:8080/api/ships](http://localhost:8080/api/ships)
- **Use [Postman](https://www.postman.com/)** to manage ships.

## Requests

- **GET:** 
  - `"/api/ships"`: Get all ships.
  - `"/api/ships/{id}"`: Get ship by id.
  - `"/api/ships/search?name={name}"`: Get ship by string.

- **POST:** `"/api/ships"`: Create new ship with body: 

    ```json
    {
        "name": "Voyager9",
        "speed": 25.5,
        "fuelCapacity": 1000.0,
        "cargoCapacity": 500.0
    }
    ```

- **PUT:** `"/api/ships/{id}"`: Update ship with body:

    ```json
    {
        "name": "Voyager12",
        "speed": 22.5,
        "fuelCapacity": 1020.0,
        "cargoCapacity": 52.0
    }
    ```

- **DELETE:** `"/api/ships/{id}"`: Delete ship by id.