# Docker Databases

This repository hold all my databases including MySQL and PostgreSQL.

The databases are deployed in docker containers and orchestrated using docker compose.

## Environment Variables

To connect to the databases you will have to provide some environment variables in the docker-compose.yml file.
Some defaults have been set in the file, you can override them with whatever you like.

Example PostgreSQL environment variables:

`POSTGRES_USER`
`POSTGRES_PASSWORD`

Example MySQL environment variables:

`MYSQL_PASSWORD`
`MYSQL_USER`
`MYSQL_DATABASE`

## Run Locally

This project requires that you already have docker and docker compose installed locally on your machine.

You can find instructions for setting up docker [here](https://docs.docker.com/engine/install/) and to setup docker compose follow this [link](https://docs.docker.com/compose/install/)

Clone the project

```bash
  git clone https://github.com/adebay8/databases
```

Go to the project directory

```bash
  cd databases
```

Create the directories for the database volumes

```bash
  mkdir postgres-db
  mkdir mysql-db
```

Spin up the database containers.

You use the -d option to ensure the containers run in the background

```bash
  docker compose up -d
```

To spin up the individual database containers.

```bash
  docker compose up mysql -d
  docker compose up postgres -d
```

Check status of database containers

```bash
  docker ps -a
```

## Optimizations

In the future I am hoping to add other databases including MongoDB, MariaDB, Redis Servers etc.
