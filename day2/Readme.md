:

### Ec2:
it's a virtual server. first we need launch i.e ceate one instance.
-> choose the name and  choose amazon machine image. that is selecting the ios to laubnch our instance.
-> it will automatically takes the intance type.
->key paoir: it's an authentication puropose just like the fingeroprint and it is used to securely launch our instance.

after launching aws instance it will create both public and private ip.
privateIp-> used to access the instance within the aws.
publicIP -> used to access the instance outside the aws.


-> public is not static it will change once we restart the server.
-> wher as private ip is static.


## ec2 instances: 
monitoring -> based on cpu credit usage balance we decrease or increase the servers.




git commands add them in git readme.md
Git clone Command:
---------------------

 $git clone https://github.com/SrinivasEsapalli/Devops_learning



if git command doesn't work  means use these comm


## to access ec2 instances:
--------------------------
-> open git bash
-> cd "particular name of folder in double quotes"
->check for the pem file(key value file) which we created
## run this command to allow permisssions in windows
### for windows chmod 777 AwsClass.pem 
### for apple same command in apple-> chmod 600 awsclass.pem

-> add an inbound rule to access it successfully
-> click on ssh connect and copy the ssh command i,e ssh -i"pemfile"@public Ip 


## security groups:
allows particular ip or users to the ec2 ...



## Deploy tomcat application:


### sudo -> sudo means super user

### installing application in server
sudo apt install nginx  
### nginx is a open source web server

### accessing the nginx application
service nginx status

 ## to start/stop/restart 
 service nginx start/stop/restart




### Deafualt nginx location
cd /var/www/html/
### to open the nginx  
-> cat index.nginx-debian.html   

### to renmove exisiting nginx html file 
rm index.nginx-debian.html

### to create new file
vi index.html

###commands
####q -> exit  
####:wq to save and exit
####ctrl+c --> come out from nginx loop
