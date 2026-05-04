**Amazon EFS (Elastic File System)** is a different type of storage from EBS—it’s built for **shared access across multiple EC2 instances**. Those Instances can be in different AZ.

You have 3 EC2 instances behind a load balancer:

- Users upload images/files
- If you use **EBS**:
    - Each instance has its own storage
    - Files uploaded to one instance are NOT visible to others
- If you use **EFS**:
    - All instances share the same file system
    - Upload once → accessible everywhere


![[Pasted image 20260502183829.png]]

![[Pasted image 20260502184008.png]]

**Uses Security Groups to control access to EFS**
**Compatible with Linux based AMI only(Not Windows)**

![[Pasted image 20260502184423.png]]

> If the question says **“unpredictable or variable workload” → Elastic Throughput**  
> If it says **“consistent high throughput regardless of size” → Provisioned**  
> If nothing special is mentioned → **Bursting (default)**

### **1. Bursting Throughput (Default)**
- Throughput is **linked to the size of your file system**
- The more data you store, the higher your baseline throughput
- Supports **bursting** using credits (like CPU credits)
### **2. Provisioned Throughput**
- You **manually set the throughput** (independent of storage size)
- You pay for the throughput you provision
### **3. Elastic Throughput (Newer & recommended in many cases)**
- Throughput **automatically scales up/down** based on workload
- No need to manage burst credits or provision capacity

# EFS - Storage Classes

![[Pasted image 20260502185458.png|412]]
# Storage Tiers

> **EFS storage tiers optimize cost by moving less-used data to cheaper storage automatically.**

### **1. Standard Storage**

- For **frequently accessed data**
- Stored across multiple AZs → **high availability**
- **Low latency** access

**Use cases:**

- Active web content
- Applications with frequent reads/writes
- Shared file systems used daily

---

### **2. Infrequent Access (EFS IA)**

- For **rarely accessed data**
- **Much cheaper storage cost**
- But **higher access cost** (you pay when you read/write)

**Important:**

- Slightly higher latency than Standard

**Use cases:**

- Backups
- Old files/logs
- Data not accessed often

---

### **3. Archive (EFS Archive)**

- For **very rarely accessed data**
- **Lowest storage cost**
- **Highest access latency** (not instant like Standard)

**Use cases:**

- Compliance data
- Long-term retention
- Data you almost never access

---

## **Lifecycle Management (Automation)**

You don’t have to move files manually.

EFS can **automatically shift files** between tiers:

- Standard → IA (after X days of no access)
- IA → Archive (after longer inactivity)

Example:

- File not used for 30 days → moves to IA
- Not used for 90 days → moves to Archive