[[Horizontal vs Vertical Scaling ]]
High Availability & Scalability :
![[Pasted image 20260503091452.png]]

![[Pasted image 20260503091555.png]]

# Load Balancing 

- Load Balancers are servers that forward traffic to multiple servers(EC2 instances) Downstream.
![[Pasted image 20260503092010.png]]

- Only one end-point of connection for users 
![[Pasted image 20260503092121.png]]

**ELB is a MANAGED LOAD BALANCER, meaning its is maintained by AWS**

![[Pasted image 20260503092304.png]]

# [[Health Checks]]

Health Check is a method to verify if an instance is working, and if the Load Balancer should send traffic to it.

# Types of Load Balancers
1. CLB
2. [[ALB Application Load Balancer v2]]
3. [[NLB - Network Load Balancer]]
4. [[GWLB - Gateway Load Balancer]]
![[Pasted image 20260503092813.png]]

![[Pasted image 20260503093340.png]]


# Load Balancers Security Groups 

Basically Only allow traffic if it is coming from the load balancer. We accomplish this by linking Security groups.


![[Pasted image 20260503093550.png]]


# [[Sticky Sessions (Session Affinity)]]

# [[Cross-Zone Load Balancing]]

# [[SSL&TLS]]

# [[Connection Draining]] 

![[Pasted image 20260503195734.png]]
