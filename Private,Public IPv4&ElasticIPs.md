![[Pasted image 20260501143548.png|493]]![[Pasted image 20260501143709.png|490]]

# Elastic IPs

Whenever you stop and start an instance, the IP resets. If we want a static IP, we need to use an Elastic IP.

An **Elastic IP (EIP)** in AWS is a **static, public IPv4 address** that you can allocate to your AWS account and then assign to resources like an **EC2 instance**.

### Why it exists

Normally, when you start/stop an EC2 instance, its public IP **changes**. That’s a problem if:

- You’re hosting a website
- You’ve whitelisted an IP somewhere
- You need a fixed endpoint

Elastic IP solves this by giving you a **permanent public IP** you control.