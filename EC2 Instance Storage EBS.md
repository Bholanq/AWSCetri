An EBS(Elastic Block Storage) Volume is a VIRTUAL network HARD drive that you can attach to your instances while they run.

- It allows your instance to persist data even after termination 
- **One instance at a time** 
- but an instance can have multiple EBS 
- **Bound to specific AZ**(An EBS made in us-east-1 can't be bound to an instance in us-east-2)

## EBS Volume
![[Pasted image 20260502091118.png]]

IOPS - Input output per second
**EBS doesn't necessarily have to be attached to an EC2 instance**
 ![[Pasted image 20260502091500.png]]

## [[EBS Volume Types]]
## Delete on Termination
root volume - deleted on instance termination
other volumes - not deleted on termination 

![[Pasted image 20260502091736.png]]


# [[EBS Snapshots]]