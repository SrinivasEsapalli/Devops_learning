


day 13:


Docker commands:



# Docker Commands  
1. [ Image ](#image)
2. [ Container ](#container)
3. [ Running Container ](#run)

---  

# docker image is the collection of softwares dependencys and librarys...

<a name="image"></a>
## Image  

###  To download all the dependencys in the docker..i.e to download complete docker image

docker pull nginx


###  To list images 
docker images 

 To install the image with specific tag
docker pull hello-world:linux


###  remove a specific image 
docker rmi hello-world:linux

if we didnt mention any tag it will remove latest tag image

###  To run particular image(Application)
docker run hello-world
after running the image the containers are created by default.


<a name="container"></a>
## Container

### To list the running containers
 docker ps
 
To list all the  containers i,e running, paused,exited.
docker ps -a

### running containers in background 
docker run -d nginx

### We cannot remove a running container directly we need to stop then only we can remove it.

### to Stop
docker stop container id

### to Start
docker start container id

### to inspect 
docker inspect container id








