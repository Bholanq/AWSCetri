- **Amazon Kinesis Data Streams (KDS)** is a fully managed AWS service used for **real-time data streaming**. It lets you continuously collect, process, and analyze large streams of data as they arrive.

![[Pasted image 20260510193058.png]]

# Features
- Retention up to 365 days
- Data can't be deleted form Kinesis 
- ![[Pasted image 20260510193405.png]]
- KPL - Optimize Production Applications
- KCL - Optimize Client Applications

### Capacity Modes

Shard:
- A stream is made up of shards.
- Each shard provides:
    - **1 MB/sec write** capacity
    - **2 MB/sec read** capacity
- You scale by increasing/decreasing shards.
Record:
- The actual data (payload) sent into the stream.
- Includes:
    - Data blob
    - Partition key
    - Sequence number

![[Pasted image 20260510193817.png]]
