## **Documentation for Project 15**

### AWS Cloud Solution For 2 Company Websites Using A Reverse Proxy Technology

### Creating a VPC

![Creating-our-VPC](./Images/Creating-our-VPC.png)

### Enabling DNS Hostnames

![Enabling-DNS-Hostnames](./Images/Enabling-DNS-Hostnames.png)

### Creating Internet Gateway

![Creating-internet-gateway](./Images/Creating-internet-gateway.png)

### Attaching our Internet Gateway to our VPC

![attaching-our-igw-to-our-VPC](./Images/attaching-our-igw-to-our-VPC.png)

![attaching-our-igw-to-our-VPC](./Images/Attached-to-Our-VPC.png)

![attaching-our-igw-to-our-VPC](./Images/attaching-our-igw-to-our-VPC-2.png/)

### Creating Route Table for our Public Subnet

![public-subnet-route-table](./Images/public-subnet-route-table.png)

### Creating Route Table for our Private Subnet

![private-subnet-route-table-created](./Images/private-subnet-route-table-created.png)

### Associating our Public Subnets with our Public Route Table

![private-subnets-associated-with-private-route-table](./Images/public-subnets-associated-with-public-route-tables.png)

### Associating our Private Subnets with our Private Route Table

![private-subnets-associated-with-private-route-table](./Images/private-subnets-associated-with-private-route-table.png)

### Editing the route for our Public Route Table

![Editing-route-for-our-public-route-table](./Images/Editing-route-for-our-public-route-table.png)

### Creating a NAT Gateway to associate with Private Route Table

### Allocating an Elastic IP for our NAT Gateway

![Allocating-Elastic-IP-for-our-NAT-Gateway](./Images/Allocating-Elastic-IP-for-our-NAT-Gateway.png)

### NAT Gateway created for our private route table

![NAT-gateway-created-for-our-private-route-table](./Images/NAT-gateway-created-for-our-private-route-table.png)

### Editing the route for our Private Route Table and associating our NAT Gateway with our Private route Table

![Editing-route-for-our-private-route-table](./Images/Editing-route-for-our-private-route-table.png)

### Creating Security Groups for our External ALB and our resources

![Security-Group-created-for-our-ext-ALB](./Images/Security-Group-created-for-our-ext-ALB.png)

### Creating Security Group for our Bastion host to allow ssh access only from our computer IP not from anywhere

![security-group-for-bastion-host-to-allow-ssh-access](./Images/security-group-for-bastion-host-to-allow-ssh-access.png)

### Creating Security Group for our Reverse Proxy Server (Nginx) to allow HTTP and HTTPS traffic from our external ALB and ssh access from our Bastion Server

![Security-group-created-for-Reverse-Proxy](./Images/Security-group-created-for-Reverse-Proxy.png)

### Creating Security Group for our Internal ALB to allow HTTP and HTTPS traffic from Nginx Reverse Proxy

![Security-group-created-for-Internal-ALB](./Images/Security-group-created-for-Internal-ALB.png)

### Creating Security Group for our Web servers to allow HTTP and HTTPS Traffic from our Internal Load Balancer and ssh access from Bastion Host

![Security-group-created-for-Webservers](./Images/Security-group-created-for-Webservers.png)

### Creating Security Group for Datalayer access to NFS Database and Bastion

![Security-group-created-for-Datalayer](./Images/Security-group-created-for-Datalayer.png)

### Creating a certificate in order to create an application Load Balancer

![Requesting-a-certificate-for-creating-ALB](./Images/Requesting-a-certificate-for-creating-ALB.png)

### Certificate issued after creating record in route 53

![Certificate-issued](./Images/Certificate-issued-after-creating-record-in-Route53.png)

### Creating EFS for Private Subnet 1 and 2 so that our webservers in that subnet will be able to mount on that storage

![Creating-Efs-for-our-webservers](./Images/Creating-Efs-for-our-webservers.png)

### Creating access points that our webservers will use to mount, one for wordpress Webserver and another one for Tooling Webserver

![wordpress-webserver-Access-point-created](./Images/wordpress-webserver-Access-point-created.png)

![Tooling-webserver-Access-point](./Images/Tooling-webserver-Access-point.png)

### Creating RDS, which involves creating a KMS key in a KMS Store and creating a Subnet Group

### Creating a KMS Key to encrypt the Database Instance

![Creating-RDS-Key-to-encrypt-database-instance](./Images/Creating-RDS-Key-to-encrypt-database-instance.png)

### Creating a Subnet Group for our RDS Which Resides in Subnet 3 and 4
![Subnet-Group-Created](./Images/Subnet-Group-Created.png)

### Creating a Database (RDS)
![Database-Created](./Images/Database-Created.png)

### Setting up our compute resources for Bastion, Webservers and Nginx

### AMI's Created for our 3 Resources
![AMIS-created-for-our-resources](./Images/AMIS-created-for-our-resources.png)

## Setting up our Bastion
### Installing epel-release and remi-repo
![installing-epel-release-and-remi-repo-on-bastion](./Images/installing-epel-release-and-remi-repo-on-bastion.png)

![installing-epel-release-and-remi-repo-on-bastion-2](./Images/installing-epel-release-and-remi-repo-on-bastion-2.png)

### Installing tools needed for our Bastion to run
![tools-installed-for-bastion](./Images/tools-installed-for-bastion.png)

### chrony started and running
`sudo systemctl start chronyd`
`sudo systemctl enable chronyd`

![chrony-started-and-running](./Images/chrony-started-and-running.png)

### Installing tools needed for our Bastion to run
![tools-installed-for-bastion](./Images/tools-installed-for-bastion.png)

## Setting up our Nginx
### Installing epel-release and remi-repo for Nginx
![installing-epel-release-and-remi-repo-on-Nginx-1](./Images/installing-epel-release-and-remi-repo-on-Nginx-1.png)

![installing-epel-release-and-remi-repo-on-Nginx](./Images/installing-epel-release-and-remi-repo-on-Nginx.png)

### Installing epel-release and remi-repo for Nginx
![installing-epel-release-and-remi-repo-on-Nginx-1](./Images/installing-epel-release-and-remi-repo-on-Nginx-1.png)

### chrony started and running
`sudo systemctl start chronyd`
`sudo systemctl enable chronyd`

![chrony-started-and-running-on-Nginx](./Images/chrony-started-and-running-on-Nginx.png)

### Installing all necessary tools on Nginx
![installing-necessary-tools-on-Nginx](./Images/installing-necessary-tools-on-Nginx.png)

### Configuring SE Linux Policies for Nginx
![selinux-policy-configured-for-nginx](./Images/selinux-policy-configured-for-nginx.png)

### Installing Amazon EFS Utility for Mounting our Target on the Elastic File System
![amazon-efs-utility-installed](./Images/amazon-efs-utility-installed.png)

### Setting up Self Signed Certificate for our Nginx Instance
![setting-up-self-signed-cert-1](./Images/setting-up-self-signed-cert-1.png)

![setting-up-self-signed-cert-2](./Images/setting-up-self-signed-cert-2.png)

## Setting up our Webserver

### Installing epel-release and remi-repo on Our Webserver
![installing-epel-release-and-remi-repo-on-webserver-1](./Images/installing-epel-release-and-remi-repo-on-webserver-1.png)

![installing-epel-release-and-remi-repo-on-webserver-2](./Images/installing-epel-release-and-remi-repo-on-webserver-2.png)

### Installing all necessary tools on Webserver
![installing-necessary-tools-on-Webserver](./Images/installing-necessary-tools-on-Webserver.png)

### chrony started and running
`sudo systemctl start chronyd`
`sudo systemctl enable chronyd`

![chrony-started-and-running-on-webserver](./Images/chrony-started-and-running-on-webserver.png)

### Configuring SE Linux Policies for Webserver
![selinux-policy-configured-for-webserver](./Images/selinux-policy-configured-for-webserver.png)

### Installing Amazon EFS Utility for Mounting our Target on the Elastic File System
![amazon-efs-utility-installed-on-webserver](./Images/amazon-efs-utility-installed-on-webserver.png)

### Setting up Self Signed Certificate for our Apache webserver Instance

### Using Openssl command to generate our key and certificate
![mod-ssl-installation-for-apache-webserver](./Images/mod-ssl-installation-for-apache-webserver.png)

### Specifying path to our generated key and cert in ssl.conf config file
![Specifying-path-to-our-key-and-cert-in-ssl-config-file](./Images/Specifying-path-to-our-key-and-cert-in-ssl-config-file.png)

### Specifying path to our generated key and cert in ssl.conf config file, changing it from default to our generated key and cert name
![Specifying-path-to-our-key-and-cert-in-ssl-config-file](./Images/Specifying-path-to-our-key-and-cert-in-ssl-config-file.png)

### Creating an AMI for each of our instances
![amis-created-for-each-of-our-instances](./Images/amis-created-for-each-of-our-instances.png)

## Creating target Groups for applications behind our Load Balancers

![target-group-created-for-nginx](./Images/)


### Creating a target group for our required resources, nginx, tooling and wordpress servers
![target-group-created-for-nginx](./Images/target-group-created-for-our-resources.png)
