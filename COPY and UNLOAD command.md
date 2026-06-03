
In AWS, the **`UNLOAD` command** is primarily used in **Amazon Redshift** to **export data from a Redshift table to Amazon S3**.
### What it does

`UNLOAD` takes query results or entire tables from Redshift and writes them out as files in S3.

Instead of pulling data row-by-row to a client, it efficiently pushes data out in parallel from the cluster.

|Command|Direction|Purpose|
|---|---|---|
|COPY|S3 → Redshift|Load data into Redshift|
|UNLOAD|Redshift → S3|Export data out|
