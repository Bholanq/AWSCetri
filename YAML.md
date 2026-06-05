**YAML** (YAML Ain't Markup Language) is a human-readable data serialization format commonly used for **configuration files**

## YAML Basics
### Key-Value Pairs

```
name: nginx
version: 1.0
enabled: true
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

# Example

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


```
{
  "apiVersion": "v1",
  "kind": "Pod",
  "metadata": {
    "name": "nginx-pod"
  },
  "spec": {
    "containers": [
      {
        "name": "nginx",
        "image": "nginx",
        "ports": [
          {
            "containerPort": 80
          }
        ]
      }
    ]
  }
}
```

| YAML                          | JSON                    |
| ----------------------------- | ----------------------- |
| `key: value`                  | `"key": "value"`        |
| Indentation                   | Nested `{}` objects     |
| `- item`                      | Array `[]` elements     |
| `containers:` followed by `-` | `"containers": [ ... ]` |
| `containerPort: 80`           | `"containerPort": 80`   |

```
containers:
  - name: nginx
    image: nginx
  - name: redis
    image: redis
```

```
{
  "containers": [
    {
      "name": "nginx",
      "image": "nginx"
    },
    {
      "name": "redis",
      "image": "redis"
    }
  ]
}
```

The `-` applies to the entire indented block that follows it at the same indentation level

```
{
  "containers": [
    {
      "name": "nginx",
      "image": "nginx",
      "ports": [
        {
          "containerPort": 80
        }
      ]
    }
  ]
}
```

