**Health checks** are how a load balancer (like ALB/NLB) decides whether a server is **able to handle requests or should be temporarily avoided**.

---
![[Pasted image 20260503232348.png]]
## Simple Definition (exam-ready)

> A health check is a periodic request sent by a load balancer to its targets to determine if they are healthy and capable of serving traffic.

## Example (ALB)

Health check config:

```
Protocol: HTTPPath: /healthPort: 80
```

ALB sends:

```
GET /health
```

If response:

- `200 OK` → Healthy
- `500 / no response` → Unhealthy