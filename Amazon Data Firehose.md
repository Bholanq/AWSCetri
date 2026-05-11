![[Pasted image 20260511001752.png]]

Amazon Kinesis Data Firehose is a **fully managed data delivery service** used to **capture, transform, and load streaming data** into destinations like:

- Amazon S3
- Amazon Redshift
- Amazon OpenSearch Service
- Splunk
- HTTP endpoints

It is mainly used for **streaming ETL and data loading**.

```
Application → Firehose → Raw Data in S3
                           ↓
                      Glue ETL Job
                           ↓
                  Cleaned Analytics Data
```

Firehose transports data.  
Glue processes and transforms it.

![[Pasted image 20260511002458.png]]

![[Pasted image 20260511002613.png]]

