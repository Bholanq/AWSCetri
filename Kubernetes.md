Kubernetes manages PODs not Containers.
PODs are just wrappers around containers.

These pods need to live on some env. This could be VMs, OR our own Machine, very similar to Docker Containers.

# Kubectl
- Kube Control
	[[kubectl commands]]
	
**kubectl** is the command-line tool used to interact with a Kubernetes cluster.
A Kubernetes cluster contains of nodes which are VM's with containers in them.
- Controller nodes - Doesn't usually have containers since its resources are used for mgmt.
- Worker nodes

![[Pasted image 20260604082415.png|389]]

![[Pasted image 20260604083018.png|386]]

The API Server is the only thing that talks to **etcd**.
- **etcd** is Kubernetes' distributed key-value database.
- Think of it as the **single source of truth** for the entire Kubernetes cluster 
- stores the state of our clusters
![[Pasted image 20260604083056.png|594]]

### Scheduler
The **Scheduler** decides **where a Pod should run**.
### Controller-manager
The **Controller Manager** continuously checks whether the cluster's actual state matches the desired state.

eg. if the the cluster node has 1 pod less, it will create that pod.
It runs multiple controllers, such as:

- Deployment Controller
- ReplicaSet Controller
- Node Controller
- Job Controller
- Endpoint Controller
### kubelet
The **Kubelet** runs on **every worker node**.
It is the agent responsible for making sure the containers assigned to that node are actually running.

![[Pasted image 20260604083346.png|385]]
# Container Runtime

![[Pasted image 20260604090812.png|385]]

![[Pasted image 20260604091328.png|697]]

[[Manifest]]
