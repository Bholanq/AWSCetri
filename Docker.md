[[AL's Docker]]
- Software Development Platform to deploy apps.
- Apps are packaged in containers that can run on any OS.
![[Pasted image 20260518090705.png]]

**Docker** is a platform that lets you package, distribute, and run applications inside lightweight, portable containers. Think of it as a way to bundle your app with everything it needs (code, libraries, dependencies, runtime) so it runs the same anywhere.

- **Containers**: Isolated environments where your app runs
- **Images**: Blueprints used to create containers
- **Docker Engine**: The runtime that builds and runs containers

![[Pasted image 20260518091146.png|342]]
- We can have multiple Containers on the same sever
- Containers can be repeated
# Where are Docker Images stored?
- Docker Repos
	- Docker Hub
	- Amazon ECR

![[Pasted image 20260518092757.png|348]]
# [[Docker vs Virtual Machines]]
VMs have a higher level of Isolation

![[Pasted image 20260518093129.png]]

## VM + Containers
Managed via Orchestrators - Cybernetics etc. 
![[Pasted image 20260603070017.png|434]]
# Getting Started with Docker

![[Pasted image 20260518093650.png|449]]
- Dockerfile - Text file that contains instructions on how to build the Docker Image.
- We build using the dockerfile  , along with everything else to build the Docker Image.

# Docker Containers Management on AWS

![[Pasted image 20260518094323.png]]

[[ECS]]
[[EKS]]
[[Fargate]]
[[ECR]]
[[Kubernetes]]

