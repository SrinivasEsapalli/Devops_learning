


day 13:


Docker commands:



# Docker Commands  
1. [ Image ](#image)
2. [ Container ](#container)
3. [image build & Tag ](#build)


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
```
docker build --tag "<image-name>:<image-tag-version>" --file "/path/to/Dockerfile"  .
### note the . is also part of the syntax

### Renaming the image and tag

docker tag <image-name>:<current-tag> <image-name>:<new=tag>
ex:
docker tag customized-hello-world:v1.0 srinivasesapalli/hello-world-customized:v2



## docker image
--> first build the image
--> tag the image with the version
--> push to docker hub







