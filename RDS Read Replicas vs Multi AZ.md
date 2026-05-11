
Read Replicas - Read-only copies of DBs

- Up to 15 Read Replicas
- Can be within AZ, or Cross AZ
- Replication are ASYNC, so reads are eventually consistent 
- Replicas can be promoted to their own DB

![[Pasted image 20260504121915.png]]

**Asynchronous (ASYNC) replication** is a data replication method where the **primary database does not wait for the replica to confirm the update** before completing a write operation.
## Simple definition

When data is written to the primary DB:
1. It is **committed immediately**
2. Then changes are **sent to replicas in the background**
So, primary is fast — but replicas may be slightly behind.

# Use cases

![[Pasted image 20260504122241.png]]

#### Read Replicas are only used for SELECT statements

# Network cost
Only when data goes across AZ not when within the same AZ

![[Pasted image 20260504122424.png]]

# Multi AZ - Disaster Recovery

**Multi-AZ (Multi–Availability Zone)** is a high-availability feature in AWS databases where your data is **automatically replicated to a STANDBY INSTANCE in a different Availability Zone**.



- ### Cannot be read or written - only Disaster Recovery
- but in case an DR does occur a stand-by is promoted to a Master DB
- **Read Replicas can also be used as Multi AZ for DR**
- **Synchronous** 

![[Pasted image 20260504122803.png]]

# Single AZ to Multi AZ
![[Pasted image 20260504123401.png]]

# [[RDS Custom]]
