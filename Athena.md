- **Serverless query service** to a analyze data stored in **Amazon S3**.
- Uses **standard SQL** to query the files(built on Presto)
![[Pasted image 20260507121122.png]]

# Performance
- use columnar data for cost saving
- compress data for smaller retrievals
- partition dataset in s3
- use larger files to minimize overhead
![[Pasted image 20260507121548.png]]

### [[Athena - Federated Query]]
