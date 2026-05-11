In [AWS Glue](https://aws.amazon.com/glue/?utm_source=chatgpt.com), a **Crawler** is a service that automatically scans your data source, infers the schema, and creates/updates metadata tables in the Glue Data Catalog.
A crawler can scan:
- Amazon S3
- JDBC databases
- DynamoDB
- Delta Lake
- Iceberg/Hudi datasets
Most commonly:
- S3 buckets


![[Pasted image 20260509053512.png]]

# Schema Evolutions

> Automatically detecting and updating table schemas when the underlying data structure changes.

![[Pasted image 20260509053919.png]]
# What the Crawler Actually Does

Crawler:
1. scans S3 files
2. infers schema
3. compares with existing Glue Catalog schema
4. updates metadata if changes detected

Important:
```
Crawler updates metadata only
```
It does NOT modify actual files.