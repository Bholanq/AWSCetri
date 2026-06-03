![[Pasted image 20260603090716.png]]

**Docker volumes** are the **preferred way to store persistent data** used by Docker containers.

In simple terms:

> A volume is a **storage area outside the container’s writable layer**, used to keep data safe even if the container is deleted.


### Docker Storage types:
1. Volumes - Stored in Docker’s internal directory
2. Bind Mounts - Directly maps a host folder to a container
3. tmpfs mounts


![[Pasted image 20260603091549.png]]
