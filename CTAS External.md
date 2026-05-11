Create Table as Select 
Creates table using meta-data that is derived from a a select statement. The meta-data of the selected table is also stored in the catalog.

![[Pasted image 20260508125842.png|339]]
# CTAS Managed
The only difference between External and Managed, is the location where the meta data of the CTAS table is stored. 
In External it is storage in an external location in S3, while in Managed it is stored in a location managed by Glue itself.

![[Pasted image 20260508143646.png|340]]






