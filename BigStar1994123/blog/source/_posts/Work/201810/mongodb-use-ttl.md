---
title: Use TTL(Time To Live) in MongoDB
tags:
  - 工作
  - MongoDB
  - TTL
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-10-16 13:50:26
---
# 在 MongoDB 內使用 TTL #

TTL == Time To Live  
用於存放暫存資料  
`var collection = _database.GetCollection<Student>("Students");`

舊的實作方法(已過時)  
```
  var index = collection.Indexes.CreateOne(Builders<Student>.IndexKeys.Ascending("expireAt"),
              new CreateIndexOptions { ExpireAfter = new TimeSpan(0, 0, 20) });
```

新的實作方法  
```
  var options = new CreateIndexOptions { ExpireAfter = new TimeSpan(0, 0, 20) };
  var index = new CreateIndexModel<Student>(Builders<Student>.IndexKeys.Ascending("expireAt"),options);
  collection.Indexes.CreateOne(index);
```