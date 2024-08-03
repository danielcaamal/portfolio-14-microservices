# Portfolio 14 - Microservices

This project is a simple example of a microservices architecture using NestJS and Kubernetes.

## Introduction

The project is divided into 5 Microservices:

- **Client Gateway**: The entry point of the application. It receives the requests and forwards them to the correct service as REST API.
- **Auth Microservice**: Responsible for managing the authentication. It contains the connection with the database (PostgreSQL).
- **Orders Microservice**: Responsible for managing the orders. It contains the connection with the database (PostgreSQL).
- **Products Microservice**: Responsible for managing the products. It contains the connection with the database (PostgreSQL).
- **Payments Microservice**: Responsible for managing the payments. It contains the connection with stripe as a payment gateway.

## Technologies

- [NestJS](https://nestjs.com/): For the services
- [Docker](https://www.docker.com/): For the containerization of the services
- [PostgreSQL](https://www.postgresql.org/): For the databases
- [Prisma](https://www.prisma.io/): For the database connection
- [NATS](https://nats.io/): For the communication between the services
- [Stripe](https://stripe.com/): For the payment gateway
- [JWT](https://jwt.io/): For the authentication
- [MongoDB](https://www.mongodb.com/): For the user data
- [GCLOUD](https://cloud.google.com/): For the storage of the docker images and the CI/CD
- [Kubernetes](https://kubernetes.io/): For the deployment of the services

## Installation

1. Git clone the repository

```bash
git clone
```

2. Update the submodules

```bash
git submodule update --init --recursive
```

3. Create the .envs files

```bash
cp ./client-gateway/.env.template ./client-gateway/.env
cp ./orders-ms/.env.template ./orders-ms/.env
cp ./products-ms/.env.template ./products-ms/.env
cp ./payments-ms/.env.template ./payments-ms/.env
cp ./auth-ms/.env.template ./auth-ms/.env
```

4. Fill the .env files with the correct values or use the default values

5. Execute Docker Compose

```bash
docker-compose up -d --build
```

## Installation (Production)

1. Clone the repository and update the submodules

```bash
git clone --recurse-submodules
```

2. Create the main .env file

```bash
cp .env.template .env
```

3. Execute

```bash
docker-compose -f docker-compose.prod.yml up -d --build
```
