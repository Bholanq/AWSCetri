They control how traffic is allowed into and out of our EC2 instance.

- SG only contain **allow** rules 
- SG rules can be referenced by IP or other Security groups

![[Pasted image 20260501054429.png|513]]

- They act as a firewall to the EC2 instance 
- Controlling:
	- Access Ports 
	- Authorized IP Ranges - IPv4 and IPv6
	- Inbound Traffic - from other to the instance 
	- Outbound Traffic - from instance to the other 

By default Security group allows all outgoing traffic and all inbound traffic is blocked by default

![[Pasted image 20260501055124.png]]

time out - SG error
![[Pasted image 20260501055535.png]]

# Referencing Security Groups from other security groups

![[Pasted image 20260501055832.png]]

In a general sense, if an EC2 instance has an SG which authorizes another SG, then the other SG is allowed communication with the original EC2 instance.



# Some ports:

![[Pasted image 20260501060352.png]]

# [[SSH]] 

