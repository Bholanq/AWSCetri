An **Auto Scaling Group (ASG)** in AWS is a service that automatically **adds or removes EC2 instances** based on demand, while also **maintaining availability and health**.

ASGs don't cost anything but the instance they create do!

1. **Scale out**
2. **Scale in**
3. Ensure Min/Max instances 
4. Auto register new instance to LB
5. re-create instances in-case pervious were terminated

![[Pasted image 20260503185232.png]]

**MIN/MAX/DESIRED Capacity:**

![[Pasted image 20260503185442.png]]

**ASG w LB**:

![[Pasted image 20260503185606.png]]

# Attributes:
Launch Template
![[Pasted image 20260503185648.png]]

Similar to EC2 instances

# [[CloudWatch]] 
-  It is possible to scale and ASG using CloudWatch alarms.

![[Pasted image 20260503185822.png]]


# Scaling Policies

![[Pasted image 20260503193121.png]]

- Dynamic Scaling 
	- Target - Scale based on some target - eg. avg ASG CPU
	- Simple/Step - Based on CloudWatch alarm
- Scheduled 
	- As it sounds
- Predictive - based on predictive Scaling 
- ![[Pasted image 20260503193357.png]]

# Metric to Scale on 

**ANY CUSTOM METRIC**
![[Pasted image 20260503193538.png]]

# Scaling Cooldown - 5 MIN

![[Pasted image 20260503193659.png]]

