# CORD19 challenge Infrastructure
This is the repository to store all infrastructure related items to the challenge team.

## Prerequisites

### Jupyter

### Ambiverse-NLU

https://github.com/TrivadisPF/ambiverse-nlu

To start your analysis you have to build the Dockerfile, run the following command in the "dockers" directory
~~~~~~~~~~~~
docker build -t trivadis/ambiverse-nlu:latest .
~~~~~~~~~~~~
Then start the environment from the root directory of your git import:
~~~~~~~~~~~~
docker-compose -f docker-compose/service-postgres.yml up
~~~~~~~~~~~~


## Code
The code can be found here: 
https://github.com/TrivadisPF/CORD-19-_challengePF