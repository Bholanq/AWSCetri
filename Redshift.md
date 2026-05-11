Amazon Redshift is AWS’s **fully managed data warehouse** service used for:

- Analytics
- BI dashboards
- Large-scale SQL queries
	- When compared to Athena, Redshift is better for large scale, workloads whereas Athena is better for occasional queries.
- OLAP workloads

![[Pasted image 20260508064303.png]]

- based on PostfreSQL, not used for OLTP BUT OLAP.

# Redshift Cluster n Architecture

![[Pasted image 20260508064830.png]]

# Snapshots and DR

![[Pasted image 20260508065406.png]]

- Redshift has **Multi-AZ** mode for some clusters.
- Snapshots of cluster for DR.

# Inserting data into Redshift 

![[Pasted image 20260508065809.png]]
- Kinesis Data Firehouse 
- S3 using COPY Command 
- EC2 Instance, JDBC Driver 

# [[Red Spectrum]]
