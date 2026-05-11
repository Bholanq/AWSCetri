Simple Queue Service

![[Pasted image 20260510135509.png]]

# SQS - Standard Queue
- fully managed service, used to decouple applications
- Attributes:
	- Unlimited Throughput, unlimited number of messages in the queue
	- Retention: 4-14 days. Default 4 days.
	- Low latency < 10 ms
	- Limitation : 1MB per message sent 
- Can have duplicates (at least once delivery)
	- You will receive the message
	-  But sometimes you may receive the **same message multiple times**
- Can have out of order (best effort ordering)
	- In Standard Queues, messages may not arrive in the same order they were sent.
[[Decoupling]]

# SQS - Producing Messages

- Producer to SQS using the SDK (SendMessage API)
- The message is persisted in the SQS until a consumer deletes it.
- Message retention as mentioned above.

![[Pasted image 20260510140624.png]]

# SQS - Consuming Messages

- Consumers on EC2, Servers, AWS Lambda **poll** SQS for messages. Upto 10 messages.
- The consumers then process the messages, after the processing is done the messages are deleted (DeleteMessage API).
 
![[Pasted image 20260510141030.png]]
# Multiple Consumers

![[Pasted image 20260510141419.png]]

# [[SQL with ASG]]

![[Pasted image 20260510142319.png]]

# [[SQS - Message Visibility Timeout]]

[[SQS - Long Polling]]

[[SQS - FIFO Queue]]

