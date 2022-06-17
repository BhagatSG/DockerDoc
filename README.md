# DockerDoc
Command used frequently in Docker

history | grep "docker"  
docker builder prune  
docker system df  

# Docker Image Building from a Dockerfile
time DOCKER_BUILDKIT=1 docker image build -t image_name:image_version(latest) --no-cache .


# Listing of Images in Docker
docker images


# Removing a docker image
docker rmi image_id


# Running a container from Docker Images
docker run -itd -p 1402:1433 --name docker_name ubuntu:18.04(Image name & version from above Image list)

docker run -itd -p 1402:1433 --name docker_name --hostname docker_name ubuntu:18.04

docker run -itd --name ubuntu_testing ubuntu:18.04

docker run -itd -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=Password@123" -p 1401:1433 --name docker_name mcr.microsoft.com/mssql/server:2017-latest

docker run -itd -p 8001:8000 --name docker_name image_name:image_version


# Listing of all docker Running Containers
docker ps


# Listing of all docker Running & Stopped Containers
docker ps -a


# Entering into docker conatiner
docker exec -it d3b77443c0de(container_id) bash
or 
docker attach d3b77443c0de(container_id)


# Exiting docker container
ctrl+p+q


# Stopping a container
docker stop container_id


# Removing a container
docker rm container_id


# Copying files from local machine to Docker Container
docker cp file/folder_name d3b77443c0de:/code/


# Copying files from Docker Container to local machine
docker cp d3b77443c0de:/code/file/folder_name .

