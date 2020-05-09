---
title: MongoImport Cheatsheet
tags:
  - 工作
  - MongoDB
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-10-02 10:27:58
---
# MongoDb Import 語法暫存 #

```
mongoimport.exe --host <host>:10255 -u aligala0928test -p <pwd> --db PocketHiPointLocation --collection bravoEventPoints --ssl --sslAllowInvalidCertificates --type json --file "D:\MongoDB\Server\4.0\bin\Bravo.json"
```