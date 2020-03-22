# CORD19 challenge Infrastructure
This is the repository to store all infrastructure related items to the challenge team.

## Prerequisites
consider raising the http timeout:

~~~~~~~~~~~~
export COMPOSE_HTTP_TIMEOUT=40000
~~~~~~~~~~~~
### Jupyter

### Ambiverse-NLU

Clone this repository:
https://github.com/TrivadisPF/ambiverse-nlu

Before starting Ambiverse you have to build the Dockerfiles

First building the db
~~~~~~~~~~~~
docker build -t trivadis/nlu-db-postgres:latest dockers/postgres
~~~~~~~~~~~~
And the NLU service
~~~~~~~~~~~~
docker build -t trivadis/ambiverse-nlu:latest dockers/nlu
~~~~~~~~~~~~

## Run
It is advisable as the jupyterlab needs some time to start to set the following in the shell before runnign:
~~~~~~~~~~~~
export COMPOSE_HTTP_TIMEOUT=400
~~~~~~~~~~~~

In order to start the stack you have to run:
~~~~~~~~~~~~
docker-compose -f cord19_stack.yml up -d
~~~~~~~~~~~~
This will take some time. It depends on your network speed (downloading the 25GB Database dump from the MPI) and CPU speed (storing back the DB in the Postgres).


## Code
The code can be found here: 
https://github.com/TrivadisPF/CORD-19-_challengePF