
![[Pasted image 20260504172704.png]]

![[Pasted image 20260504173631.png]]

[[Standard General Purpose]]
[[Infrequent Access]]
[[Glacier]]
[[Intelligent-Tiering]] 

[[S3 - Express - One Zone]]

[[Moving between Storage Classes, Lifecycle Rules]]

In Amazon S3, each storage class has a **minimum storage duration**—if you delete or transition objects before this period, you’re still charged as if they were stored for the full duration.

Here’s a clear breakdown:

###  S3 Storage Classes & Minimum Storage Duration

- **S3 Standard**  
    → No minimum storage duration
- **S3 Intelligent-Tiering**  
    → No minimum for Frequent/IA tiers  
    → Archive tiers behave like Glacier (see below)
- **S3 Standard-IA (Infrequent Access)**  
    → 30 days
- **S3 One Zone-IA**  
    → 30 days
- **S3 Glacier Instant Retrieval**  
    → 90 days
- **S3 Glacier Flexible Retrieval** (formerly Glacier)  
    → 90 days
- **S3 Glacier Deep Archive**  
    → 180 days