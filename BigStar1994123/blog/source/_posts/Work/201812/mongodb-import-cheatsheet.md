---
title: MongoDB Import 小抄
date: 2018-12-26 11:46:03
tags:
  - 工作
  - MongoDB
category:
  - 工作日誌
  - 2018
  - 12月
---
# MongoDB Import 語法暫存 #

```
mongoimport.exe  --host <host>:10255 -u <user> -p <password> --db <DbName> --collection <CollectionName> --ssl --sslAllowInvalidCertificates --type json --file <FileLocation> --jsonArray
```