![[Pasted image 20260503094157.png]]This is used when you need **smart routing based on request content**.
- Works at:
    - **Layer 7 (Application layer)**
- Key features:
    - **Path-based routing (`/api`, `/login`)**
    - **Host-based routing (`api.example.com`, `app.example.com`)**
    - **Query-based routing**
    - **Supports microservices & containers (ECS, Kubernetes)**
    - WebSocket support
    - Integration with WAF (security)
![[Pasted image 20260503094648.png]]

We need one CLB per application in comparison. 

In the context of an **Application Load Balancer (ALB)**, an “application” doesn’t mean a single program or server. It refers to the **web service or system that handles HTTP/HTTPS requests at the application layer (Layer 7)**.

Think of it like this:

An **application = the logic that processes a user’s request and returns a response**

![[Pasted image 20260503095113.png]]

# Target Groups

A **target group** in AWS is basically the **destination where the load balancer sends traffic**.

![[Pasted image 20260503095339.png]]

Example:
![[Pasted image 20260503095500.png]]


# ****Good to Know:

![[Pasted image 20260503101020.png]]

- Fixed host-name of the LB
- Client IP remains anon to the LB
- supports redirect 

![[Pasted image 20260503105436.png]]

## We can make it so the Instance can only be accessed by ALB, and not view the individual instance. For enhanced security.