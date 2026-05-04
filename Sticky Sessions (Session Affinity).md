- Stickiness - The same client is always redirected to the same instance behind a load balancer.
Works for:
1. CLB
2. ALB
3. NLB
In order to accomplish this we use cookies. except NLB

![[Pasted image 20260503172448.png]]


# Cookie Names

1. Application-based
2. Duration- based/ Persistent 

![[Pasted image 20260503174236.png]]

|Feature|**Application / Session Cookies**|**Duration-Based / Persistent Cookies**|
|---|---|---|
|**Definition**|Temporary cookies stored for a single session|Cookies stored for a fixed time period|
|**Lifetime**|Deleted when browser is closed|Remain until expiry date or manual deletion|
|**Storage**|Stored in memory (RAM)|Stored on disk (browser storage)|
|**Expiry**|No explicit expiry time|Has explicit expiry date/time|
|**Use Cases**|Login sessions, temporary state (shopping cart during session)|Remember me, user preferences, tracking|
|**Security**|Safer (short-lived)|Less safe if misused (long-lived)|
|**Example**|Logging into a website → session ends → cookie gone|“Remember me” → login persists across browser restarts|