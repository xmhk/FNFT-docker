
# FNFT-docker

## quick bootstrap of Docker machines for testing FNFT / FNFTpy

### create new local docker machine (LDM) for  virtualbox
docker-machine create --driver virtualbox docker-local

### start LDM
docker-machine start docker-local

### copy files to LDM
docker-machine scp Dockerfile docker-local:

### ssh into LDM
docker-machine ssh docker-local

### build a docker image on LDM	
docker image build --file Dockerfile  --tag test1:test1 .

### start the docker image created in LDM, interactively
docker container run -it --name mytestrun6 test1:test1
