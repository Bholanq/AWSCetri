When we want to have control on how the EC2 instance is placed under AWS infrastructure.

![[Pasted image 20260501150417.png]]

In AWS (and general data centers), a **rack** is a **physical metal frame or cabinet** that holds multiple servers and networking equipment.
 
**Strats:**
1. Spread 
2. Cluster
3. Partition 
## 1. Cluster Placement Group

**What it does:**  
Places instances **very close together** (same rack / same data center).

**Goal:**  
Maximize **performance and low latency**

**Use when:**

- High-performance computing (HPC)
- Big data jobs
- Machine learning workloads
- Applications needing **very fast network communication**

**Pros:**

- Extremely **low latency**
- High **network throughput**

**Cons:**

- **Single point of failure** (if hardware fails, many instances affected)

**Simple idea:**  
“All instances sit next to each other for speed”
![[Pasted image 20260501152046.png|325]]

## 2. Spread Placement Group

**What it does:**  
Spreads instances **across different physical hardware (racks)**.

**Goal:**  
Maximize **fault tolerance**

**Use when:**

- Critical applications
- Small number of instances where failure must be avoided

**Pros:**

- **High reliability**
- Each instance isolated from others

**Cons:**

- Limited to **7 instances per AZ**
- Higher latency compared to cluster

**Simple idea:**  
“Keep instances far apart to avoid simultaneous failure”

![[Pasted image 20260501152222.png]]
## 3. Partition Placement Group

**What it does:**  
Divides instances into **logical partitions**, and each partition is on separate hardware.
**Goal:**  
Balance **fault tolerance + scalability**

**Use when:**

- Distributed systems like:
    - Hadoop
    - Cassandra
    - Kafka

**Pros:**

- Failure affects only **one partition**
- Supports **large number of instances**

**Cons:**

- Not as low latency as cluster
- Slightly complex to manage
![[Pasted image 20260501152530.png]]

