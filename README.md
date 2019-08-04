# SEAPay

## Table of Contents

- [Description](#description)
- [Installation](#installation)
- [Requirement](#requirement)
- [Running the Project](#running-the-project)


## Description
 
Seapay is a fintech app consists of 4 different services
  - API gateway
    - API gateway service routes all requests to other services
  - User account
    - User account service takes care of user management: user creation, get user data, etc
  - Wallet
    - Wallet service handles all wallet functionalities: update balance, get balance, create wallet, etc
  - Transaction
    - Transaction service manage all transaction data

The project itself has 4 modules
 - seapay-api
   - a module that abstracts interface for all services
 - seapay-common
   - a module that groups all common functionalities used by all services
 - seapay-domain
   - the bussiness logic for all services goes here
 - seapay-monolith
   - an entry point of our monolithic app, including all handlers

## Requirement

- [Java Development Kit 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Postgresql 10](https://www.postgresql.org/download/)
- Make


## Installation

- Clone this repository to your machine

```
git clone https://github.com/blurey8/seapay-microservice
```

- Move to the project directory

```
cd seapay-microservice
```

- Run the Makefile using the command below. It will setup the database, running the test and build the project automatically

```
make all
```

- It's done. Now you can run the project.

## Running the Project

You can run the project by executing this command

### User

```
make run-user
```

### Transaction

```
make run-transaction
```

### Gateway

```
make run-gateway
```

### Monolith

```
make run-monolith
```

If you have run all of the service, you can check the project by making get request on [http://localhost:8080/ping](http://localhost:8080/ping) to make sure that the server has running.

---

- Repository: https://github.com/sea-compfest/seapay-microservice
