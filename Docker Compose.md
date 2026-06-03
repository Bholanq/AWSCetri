![[Pasted image 20260603080531.png|355]]
Suppose you have multiple containers attached to the same network and within that network there's an order in which the containers must be turned on and off. Docker Compose takes care of that.
![[Pasted image 20260603081247.png|363]]

Each Service is a Container

**docker-compose.yml**
```
version: '3.1'

services:
  mysql_container:
    image: mysql:8.0
    container_name: mysql_container
    restart: always
    command: --default-authentication-plugin=mysql_native_password
    environment:
      MYSQL_ROOT_PASSWORD: demopassword
      MYSQL_DATABASE: demodb
    ports:
      - "3307:3306"
    healthcheck:
      test: ["CMD", "mysqladmin", "ping", "-h", "localhost", "-u", "root", "-p$${MYSQL_ROOT_PASSWORD}"]
      interval: 10s
      timeout: 5s
      retries: 5
    volumes:
      - ./MySQL/init.sql:/docker-entrypoint-initdb.d/init.sql

  flask_container:
    build: Flask/.    
    container_name: flask_container
    restart: always
    depends_on:
      mysql_container:
        condition: service_healthy
    ports:
      - "5000:5000"  
```

```
docker-compose up -d
#builds all the containers
```

```
docker-compose down
#removes all the container in the specified order
```

```
docker compose up -d --build
#used for rebuilding
```

![[Pasted image 20260603084411.png]]

Composed Stack

[[Docker Storages]]
