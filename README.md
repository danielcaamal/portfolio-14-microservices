# Portfolio 14 - Microservices

This project is a simple example of a microservices architecture using NestJS and Docker.

## Introduction

The project is divided into 3 services:

- **Client Gateway**: The entry point of the application. It receives the requests and forwards them to the correct service as REST API.
- **Orders Microservice**: Responsible for managing the orders. It contains the connection with the database (PostgreSQL).
- **Products Microservice**: Responsible for managing the products. It contains the connection with the database (PostgreSQL).

## Technologies

- [NestJS](https://nestjs.com/): For the services
- [Docker](https://www.docker.com/): For the containerization of the services
- [PostgreSQL](https://www.postgresql.org/): For the databases
- [Prisma](https://www.prisma.io/): For the database connection
- [NATS](https://nats.io/): For the communication between the services

## Installation

1. Create the .envs files

```bash
cp .env.template .env
cp ./client-gateway/.env.template ./client-gateway/.env
cp ./orders-ms/.env.template ./orders-ms/.env
cp ./products-ms/.env.template ./products-ms/.env
```

2. Fill the .env files with the correct values or use the default values

3. Execute Docker Compose

```bash
docker-compose up -d
```
