![[Pasted image 20260507135845.png]]

Service role for lambda is automatically created by AWS.

The general code available for an lambda function is:
```
import json
def lambda_handler(event, context):
    # TODO implement
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }
```


Where `event` parameter is all the input coming from the previous entity.

![[Pasted image 20260507141932.png]]
upon running a lambda function - there's an output and a response.
## 1. Output (General Result)
The **output** is whatever your Lambda function returns after execution.
```
def lambda_handler(event, context):
    return "Hello World"
```
## 2. Response (Formatted Reply to Caller)
A **response** is the structured data sent back to the service or client that invoked Lambda.
```
def lambda_handler(event, context):
    return {
        "statusCode": 200,
        "headers": {
            "Content-Type": "application/json"
        },
        "body": '{"message":"Success"}'
    }
```

