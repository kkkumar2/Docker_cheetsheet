```git bash
docker ps    : to list running containers
docker ps -a : to list all the containers
docker images : to list all the images
docker rm [container] : to remove the container based on container id or name
docker rmi [image] : to remove the image based on the image name

docker run [image] : will create a container , pull image if not present and run it and exit 
docker run [options] [image] [command]

docker run --rm [IMAGE] – removes a container after it exits.

docker run -td [IMAGE] – starts a container and keeps it running.

docker run -it [IMAGE] – starts a container, allocates a pseudo-TTY connected to the container’s stdin, and creates an interactive bash shell in the container.

docker run -it-rm [IMAGE] – creates, starts, and runs a command inside the container. Once it executes the command, the container is removed.

docker exec -it [container id] bash : to get into container with interactive mode

docker start : to start a existing present container which is not running

docker stop : to stop a running container


Docker RUN :

TAGS : go to dockerhub and install the necessary version(tags) based on requirement
STANDARD_INPUT : if user needs to provide a prompt then go with interactive mode
PORT MAPPING : If u deploy something using your py script it will be deployed in that container only to expose that url to outside world u to have port map it
		docker run -p 8000:5000 [image]  ( 8000 is port number outside container , 5000 is port number inside container)

VOLUME MAPPING : to store the data of the container in the host os, so that data lost is not there once the container gets removed 

INSPECT : docker inspect [image name] : will give lot of details about image
LOGS : docker logs [image name] : will give the logs about image


DOCKER IMAGES :

DOCKERFILE :

from ubuntu 
RUN apt-get-update  : to update ubuntu to latest version
Run apt-get-install -y python3 python3-pip
RUN pip3 install flask
RUN mkdir /opt/app

WORKDIR /opt/app
COPY . /opt/app

ENTRYPOINT FLASK_APP=/opt/app/app.py flask run --host=0.0.0.0


DOCKER BUILD :

docker build [Dockerfile path] -t(tags) MK/demo1  MK:username , demo1 : image name

DOCKER PUSH :

docker push MK/demo1

```

