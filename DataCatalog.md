![[Pasted image 20260508121956.png|349]]
We can't read/query data which is present in the .csv format, what GlueCatalog will do is extract the metadate and schema of the .csv files and create an object which can be queried and store that in the catalog.

In AWS, particularly within **AWS Glue Data Catalog** and **Athena**, the hierarchy is structured as **Catalog > Database > Table**(metadata organization), where each term has a distinct scope and function.

A **catalog** is a higher-level container that stores metadata about databases, tables, schemas, locations, permissions, etc.
Think of it as a **master index** or **metadata repository**.
A catalog may contain multiple databases.

# External Table 

An **external table** in AWS is a table where:
- The **table metadata** is stored separately in the Glue Catalog.
- The **actual data files** remain in external storage like **S3**

![[Pasted image 20260508123143.png]]

[[CTAS External]]
[[CTAS Managed]]

| Feature                    | Managed CTAS        | External CTAS |
| -------------------------- | ------------------- | ------------- |
| Data ownership             | Engine              | User          |
| Storage location           | Default warehouse   | Custom path   |
| DROP TABLE deletes data    | Yes                 | No            |
| Better for                 | Internal processing | Data lakes    |
| S3 path controlled by user | Usually no          | Yes           |
| Safer for shared datasets  | No                  | Yes           |
