**Amazon DynamoDB** is a **fully managed NoSQL database** designed for **high performance, low latency, and massive scalability**.'

- Key-Value + document database
- serverless
- auto scaling 
![[Pasted image 20260506145518.png]]

- IAM Security 
- Tables classes - Standard + IA
# Basics
### **Rapidly Evolving Schema**
- Situations where the Schema needs to evolve,  then DynamoDB is a better choice than RDS and Aurora.
**Made of Tables - but in JSON format**
```
User Table
PK: user_id

Item:
{
  "user_id": "101",
  "name": "John",
  "age": 25
}
```
 ![[Pasted image 20260506145755.png]]
In **Amazon DynamoDB**, an **item** is basically a **single record (row) in a table**.
The equivalent of a **column** (from SQL) is called an **attribute**.

![[Pasted image 20260507051848.png]]

# DynamoDB - Read/Write Capacity Modes

- Provisioned Mode(Default) - Need to plan capacity beforehand.
	- RCUs(Read Capacity Units)
	- WCUs(Write Capacity Units)
- On-demand Mode - Read/Write Auto scales with the workload.

![[Pasted image 20260507052323.png]]

# WCU and RCUs are decoupled 
![[Pasted image 20260507112859.png]]

[[DynamoDB Accelerator(DAX)]]
[[Stream Processing]]
[[Global Tables]]
[[Disaster Recovery]]

# Integration with S3
 ![[Pasted image 20260507055622.png]]

