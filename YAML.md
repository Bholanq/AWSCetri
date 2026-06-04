**YAML** (YAML Ain't Markup Language) is a human-readable data serialization format commonly used for **configuration files**

## YAML Basics
### Key-Value Pairs

```
name: nginxversion: 1.0enabled: true
```
Equivalent JSON:
```
{  "name": "nginx",  "version": 1.0,  "enabled": true}
```
---
### Lists
```
ports:  
	- 80 
	- 443  
	- 8080
```
Equivalent JSON:

```
{  "ports": [80, 443, 8080]}
```
---
### Nested Objects
```
database:  host: localhost  port: 5432
```

Equivalent JSON:
```
{  "database": {    "host": "localhost",    "port": 5432  }}
```
---
## Indentation Matters
YAML uses **spaces**, not braces `{}`.
Correct:
```
app:  
	name: nginx  
	port: 80
```

```
apiVersion: v1
kind: Pod

metadata:
  name: nginx-pod

spec:
  containers:
    - name: nginx
      image: nginx
      ports:
        - containerPort: 80
```

