


day 13:


Docker commands:



# Docker Commands  
1. [ Image ](#image)
2. [ Container ](#container)
3. [image build & Tag ](#build)
4. [ image creation](#imagecreation)
---  

# docker image is the collection of softwares dependencys and librarys...

<a name="image"></a>
## Image  

###  To download all the dependencys in the docker..i.e to download complete docker image

docker pull nginx


###  To list images 
docker images 

 ### To install the image with specific tag
docker pull hello-world:linux


###  remove a specific image 
docker rmi hello-world:linux

if we didnt mention any tag it will remove latest tag image

###  To run particular image(Application)
docker run hello-world
after running the image the containers are created by default.

### to remove all unused images
docker image prune -a



<a name="container"></a>
## Container

### To list the running containers
 docker ps
 
### To list all the  containers i,e running, paused,exited.
docker ps -a

### running containers in background 
docker run -d nginx

### We cannot remove a running container directly we need to stop then only we can remove it.

### to remove container 
docker rm container_id

### to Stop
docker stop container id

### to Start
docker start container id

### to inspect 
docker inspect container id


<a name="build"></a>
## image & build

### Use below command to build image  

docker build --tag "<image-name>:<image-tag-version>" --file "/path/to/Dockerfile"  .
### note the . is also part of the syntax

### Renaming the image and tag

docker tag <image-name>:<current-tag> <image-name>:<new=tag>
ex:
docker tag customized-hello-world:v1.0 srinivasesapalli/hello-world-customized:v2




<a name="imagecreation"></a>
# docker image creation and running
--> first build the image ex: docker build --tag "<image-name>:<image-tag-version>" --file "/path/to/Dockerfile"  .
docker build --tag "custom-nginx:v1.0" --file "./Dockerfile" .

--> tag the image with the version
docker tag <image-name>:<current-tag> <image-name>:<new=tag>
ex:
docker tag customized-hello-world:v1.0 srinivasesapalli/hello-world-customized:v2
//srinivasesapalli/hello-world-customized:v2 --> dockerr hub repo name

--> push to docker hub

docker push srinivasesapalli/customnginx


--> to run in local port with port number
docker run -d -p 5051:80 --name custom-nginx-container custom-nginx:v1.0




Day 15:

## by default nginx runs on port 8080
##  running container on specific port

docker run -d -p <host_port>:<container_port> --name <container-name> <image-name>  

## to login into the container
docker exec -it container_id     terminal name(bash - for git bash)
ex: docker exec -it 1abcs bash


##  to check container volums
df -h



# Args & Environement Variables
### NOTE: The ARG arguments are only available when building the image, while ENV parameters are available to the application containers during build and when the container is running.

## passing arguments
docker build -t [image-name] --build-arg [arg-variable]=[value] .
## passing environment variables
docker run --name [container-name] -e "[variable-name]=[new-value]" [image-name]
## passing environment variables file
docker run --name [container-name] --env-file [path-to-env-file] [image-name]









