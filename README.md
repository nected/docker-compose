# Nected Platform docker-compose file
This repository provides docker-compose files that enable you to run a local instance of the Nected Platform. 


## Prerequisites

To use these files, you must first have the following installed:

- [Docker](https://docs.docker.com/engine/installation/)
- [docker-compose](https://docs.docker.com/compose/install/)

## How to use

The following steps will run a local instance of the Nected Platform using the default configuration file (`docker-compose.yml`):

1. Clone this repository.
2. Change directory into the root of the project.
3. Run the `docker-compose up` command.

```bash
git clone https://github.com/nected/docker-compose.git
cd  docker-compose
docker-compose up
```


## How to access

1. Open browser and access `http://localhost:3000`
2. Use credential `dev@nected.local / devPass123` to signin

IMPORTANT: While accessing rule and workflow api from other services, replace `http://10.10.0.1:8002/` with `http://localhost:8002/`