## [[AMI - Amazon Machine Image]]
# Infrastructure as a service 
- Renting Virtual Machines/Services - EC2
- Storing data on Virtual Drives - EBS
- Distributing load across machines - ELB
- Scaling the services using a auto-scaling group - ASG

# **Bound to an AZ**

EC2 sizing and config options?

![[Pasted image 20260430155425.png|482]]

# EC2 User Data

- It is possible to bootstrap our instances using an **EC2 User Data** Script
- bootstrapping means launching commands when the machine starts
- the script is run only once at the instance **first start** 
- Automates boot tasks such as:
	- installing updates/softwares
	- Downloading common files form the internet 
	- etc
- the EC2 User Data Script runs with the root user.

# EC2 Instance Types
- different types optimized for different use cases
![[Pasted image 20260430162541.png|155]]
compute - C series
memory - R series, Some X,z instance 
storage - OLTP, NoSQL, Cache 

## Naming Convention of Instances

# `m5.2xlarge`

m: instance class
6: generation
2xlarge: size within the instance class(memory size RAM)

### eg. t2.micro - General Purpose free tier EC2 instance 

# [[Security Groups]]

# EC2 Instances Purchasing Options:

![[Pasted image 20260501072829.png]] ![[Pasted image 20260501073446.png]]

# [[Spot Fleets & EC2 Spot Instance Requests & Cancellation]]
# [[Private,Public IPv4&ElasticIPs]]

# [[Placement Group]]

# [[ENI - Elastic Network Interface]]

# [[EC2 Hibernate]]

# [[EC2 Instance Storage EBS]]

# [[EC2 Instance Store]]

# [[Amazon EFS - Elastic File System]]
