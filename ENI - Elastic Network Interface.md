![[Pasted image 20260501173224.png]]

**ENI (Elastic Network Interface)** in AWS is basically a **virtual network card** that you attach to an EC2 instance.

**ENI = Virtual Network Interface that enables communication for an EC2 instance inside a VPC**

A **VPC (Virtual Private Cloud)** in AWS is your **own isolated virtual network** inside AWS where you launch and control your resources (like EC2, databases, etc.).

**Attributes!**

### Elastic Network Interfaces (ENIs) are specifically designed to function within the boundaries of a single Availability Zone (AZ). This means that you cannot attach an ENI to an EC2 instance located in a different AZ.