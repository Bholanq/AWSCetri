- When a message is polled by a consumer it becomes invisible to other consumers
![[Pasted image 20260510165310.png]]

- If a message is not processed within the visibility timeout, it will be processed twice. Either by the same consumer or another consumer 
- **ChangeMessageVisibility** - API in case the consumer needs more time to process the Message.

![[Pasted image 20260510165619.png]]