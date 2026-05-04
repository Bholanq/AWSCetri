# AWS Regions 
- basically data centers
- eg. some services are region scoped because the datacenters responsible for providing those services are region-locked.

# Q. How to choose a region?

1. Compliance 
2. Proximity and Latency
3. Available services
4. Pricing 

# Availability Zones 

![[Pasted image 20260429232948.png|430]]

# AWS Points of Prescence - Edge Locations 

# 1. [[IAM]]
# 2. How can users access AWS?
To access AWS there are three options:
1. AWS management Console 
2. AWS CLI 
3. AWS SDK

CLI and SDK are protected by [[AWS Access & Access Keys]]

# 3. [[AWS CloudShell]]

# 4. [[EC2 - Elastic Compute Cloud]] 

### * Never enter your API Keys(Access ID and Secret Access ID) into your EC2 Instance, because then anyone using the that EC2 instance will be able to access your credentials.
# * Use IAM roles instead. 
We can assign IAM roles to Instances by instance->action->security 

# 5. [[ELB - Elastic Load Balancing]] 

# 6. [[ASG - Auto Scaling Groups]]

# 7. [[RDS - Relational Database Service]]

# 8. [[Amazon Aurora]] (incomp)

# 9. [[AWS S3]]


