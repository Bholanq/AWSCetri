Amazon **ElastiCache** is a fully managed in-memory data store service(caching service) provided by AWS. It’s designed to deliver **ultra-fast performance** for applications that need low-latency access to data.

- A managed **caching layer** that sits between your application and your database
-  Helps **reduce database load** and **improve response times**
- Supports two engines:
    - **Redis** (more feature-rich)
    - **Memcached** (simpler, high-performance caching)
### How it works:
Instead of querying a database every time:
1. App checks ElastiCache first
2. If data exists → return instantly (cache hit)
3. If not → fetch from DB, store in cache (cache miss)

![[Pasted image 20260505151002.png]]

# Architecture ex
1. DB Cache

![[Pasted image 20260505151121.png]]

2. User Session Store
![[Pasted image 20260505151207.png]]

# Redis vs Memcached

![[Pasted image 20260505151352.png]]

Memcached - Sharding + Key-values
Redis - Replication + Multiple Datatypes  support(Sets etc.)

# Cache Security 

![[Pasted image 20260505155510.png]]

* Redis = IAM Auth + password/token + SSL(in-flight) + SG
* Memcached = SASL-based auth

# Patterns for ElastiCache 
- Lazy Load -Data is loaded into cache **only when it is requested**
- Write Through - Data is written to **cache and DB simultaneously**
- Session Store 

![[Pasted image 20260505155927.png]]

# Redis use case
![[Pasted image 20260505160134.png]]
- Redis Sorted Sets

