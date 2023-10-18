# Day 6
## VPC  

### Create VPC
Name: MyVPC-DemoClass
IPV4 CIDR: 10.0.0.0/16

Here, a new VPC will be created.

### CIDR -> classless inter-domain routing. it allows the range of IP into the vpc.

### Create Subnets  

We are creating 4 subnets according to our vpc architecture.
Name: Public-1A
AZ: us-east-2a
IPV4 CIDR: 10.0.1.0/24

Name: Private-1A
AZ: us-east-2a
IPV4 CIDR: 10.0.2.0/24

Name: Public-2A
AZ: us-east-2b
IPV4 CIDR: 10.0.3.0/24

Name: Private-2A
AZ: us-east-2b
IPV4 CIDR: 10.0.4.0/24

### Enable Public IP
Enable Auto Assign Public IP to the public subnets.
it will create a public server for our public subnets.

### Create Internet Gateway
Name: MyIGW
VPC: MyVPC

here we are creating an internet gateway, and then we need to attach the gateway to our VPC because many VPC are available in the cloud.

##### note Routing table will be automatically created along with the VPC. But we created the subnets because we can create as many as according to our requirement and here one Routing table is mandatory for the availability Zones.

### Attach IGW to RT
Add Internet Gateway in the main route table on 0.0.0.0/0  

so that there will be a route created to the internet gateway and the routing table
