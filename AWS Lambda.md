![[Pasted image 20260505170442.png]]
**AWS Lambda is an event-driven, serverless Function as a Service (FaaS) provided by Amazon as a part of Amazon Web Services.**
## Supported Languages:

![[Pasted image 20260505170636.png]]

**AWS Lambda** is AWS’s core **serverless compute** offering—you run code in response to events without provisioning or managing servers.

# The main benefits of using Lambda over EC2 is:

- Executes your code **on demand**
- Scales automatically (from zero to thousands of concurrent executions)
- Charges you **per request + execution time**![[Pasted image 20260506115134.png]]

# Example Serverless Thumbnail creation
![[Pasted image 20260506115331.png]]

- YoAWS Lambda is an event-driven, serverless Function as a Service (FaaS) provided by Amazon as a part of Amazon Web Services.u write a function (Node.js, Python, Java, etc.)
- You upload it to AWS Lambda
- An **event triggers it**, such as:
    - HTTP request via API Gateway
    - File upload to S3
    - Database change (DynamoDB)
    - Scheduled job (cron)
- Lambda runs your code and returns the result

# Triggers
In **Amazon Web Services Lambda**, a **trigger** is simply **an event or condition that causes your Lambda function to run automatically**.

# Lambda Limits 
Important 

![[Pasted image 20260506121421.png]]

# Lambda Concurrency and Throttling 
![[Pasted image 20260506121848.png|471]]

### Limit 
= 1000 concurrent executions 
### Reserved Concurrency
= our own set limit of concurrent executions 
each invocations over the concurrency limit will trigger a "**Throttle**"

When an **AWS Lambda** function goes into **throttling mode**, it means the service is **rejecting new invocations** because you’ve hit a concurrency limit.

DLQ - Dead Limit Queue
# Lambda Concurrency Issue 
![[Pasted image 20260506123527.png]]

The concurrency limit applies to all the functions in your account. If one function goes beyond the limit, then the other functions will have to THROTTLE.

# Concurrency and Async invocations 
![[Pasted image 20260506124108.png]]


# Cold Start & Provisioned Concurrency 

Cold Start =A **cold start** happens when Lambda has to **create a new execution environment** before running your function. Everything has to be set up - takes time.

**Provisioned Concurrency** keeps Lambda environments **pre-initialized and ready**.
![[Pasted image 20260506124408.png]]

- Provisioned concurrency has additional costs

# [[Lambda SnapStart]]

# [[Customization at the edge]]


# Lambda by default 
- By default, your Lambda function is launched outside your own VPC(in an AWS-owned VPC)
- Can't access resource in your VPC so we need to launch lambda in our VPC
![[Pasted image 20260506141815.png]]


# Lambda in VPC

![[Pasted image 20260506141952.png]]


# Lambda with RDS Proxy

![[Pasted image 20260506142416.png]]


[[Invoking lambda from RDS & Aurora]]
[[RDS Event Notifications]]
