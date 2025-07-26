# SKYCONNECT - Flight Booking System

## Table of Contents
- [Description](#description)
- [Microservices Breakdown](#microservices-breakdown)
- [Tech Stack](#tech-stack)
- [Diagram](#diagram)
- [Setup Guide For Every Service](#setup-guide-for-every-service)

## Description
The architecture of SKYCONNECT is based on microservices, where each service is responsible for a specific piece of functionality. This approach ensures that the system is scalable, maintainable, and can be developed and deployed independently.

## Microservices Breakdown

| Service | Description | GitHub Repo |
|--------|-------------|-------------|
|**API Gateway** | Acts as the single entry point to route requests to all services, handles reverse proxy and rate limiting | [API Gateway](https://github.com/sohamsolankii/SKYCONNECT/tree/main/Flights-API-Gateway) |
|**Auth Service** | Handles user authentication and authorization using JWT + bcrypt | [Auth Service](https://github.com/sohamsolankii/SKYCONNECT/tree/main/Flights-API-Gateway) |
|**Flights & Search Service** | Lists flights and handles search functionality by source/destination/date | [Flights & Search Service](https://github.com/sohamsolankii/SKYCONNECT/tree/main/Flight-Search-Service) |
|**Booking Service** | Books flights, manages seat availability and user bookings | [Booking Service](https://github.com/sohamsolankii/SKYCONNECT/tree/main/Flight-Booking-Service) |
|**Reminder Service** | Sends booking reminders using RabbitMQ | [Reminder Service](https://github.com/sohamsolankii/SKYCONNECT/tree/main/Flight-Notification-Service) |

## Tech Stack
- NodeJS, ExpressJS, MySQL, Sequelize, RabbitMQ, NodeMailer, JWT, Winston, Swagger

## Diagram
![Architecture Diagram](https://github.com/sohamsolankii/SKYCONNECT/blob/main/skyconnect.png)

## Setup Guide For Every Service

- Download this template from GitHub and open it in your favorite text editor.
- Go inside the folder path and execute the following command:
  ```
  npm install
  ```
- In the root directory, create a `.env` file and add the following environment variables:
    ```
        PORT=<port number of your choice>
    ```
    Example: 
    ```
        PORT=3000
    ```
- Go inside the `src` folder and execute the following command:
    ```
      npx sequelize init
    ```
- By executing the above command, you will get migrations and seeders folders along with a config.json inside the config folder.
- If you're setting up your development environment, then write the username of your database, password of your database, and in dialect mention whatever database you are using (e.g., mysql, mariadb, etc.).
- If you're setting up test or production environment, make sure you also replace the host with the hosted database URL.

- To run the server, execute:
 ```
 npm run dev
 ```