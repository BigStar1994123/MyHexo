---
title: Redis Commander 在 Local 端跑
tags:
  - 工作
  - Redis
  - Redis Commander
category:
  - 工作日誌
  - 2019
  - 1月
date: 2019-01-07 18:39:47
---
# Redis Commander 在 Local 端跑 #

先把這個弄成一個 File 可叫做 docker-compose.yml  

```yml
version: '3'
services:
  redis:
    container_name: redis
    hostname: redis
    image: redis
    ports:
     - "6379:6379"

  redis-commander:
    container_name: redis-commander
    hostname: redis-commander
    image: rediscommander/redis-commander:latest
    restart: on-failure
    environment:
    - REDIS_HOSTS=local:redis:6379
    ports:
    - "8081:8081"
```

然後 Run 下面這行指令  

```cmd
docker-compose up
```