---
title: 暫存的 MongoDB 語法 也許之後用的到
tags:
  - 工作
  - MongoDB
category:
  - 工作日誌
  - 2018
  - 11月
date: 2018-11-06 15:01:06
---
# 暫存MongoDb語法 #

```
  // https://stackoverflow.com/questions/30257013/mongodb-c-sharp-driver-2-0-update-document
  // https://rubikscode.net/2017/10/02/using-mongodb-in-c/
  // ★
  // http://mongodb.github.io/mongo-csharp-driver/2.7/getting_started/quick_tour/#insert-a-document
  // ★
  //var connectionString = _mongoDbConfig.ConnectionString;
  //var client = new MongoClient(connectionString);
  //var db = client.GetDatabase("PocketHiGamedataDb");
  //var playerInfoCollection = db.GetCollection<PocketHiPlayerInfoEntity>("pocketHiPlayerInfoEntities");
  //var filter = Builders<PocketHiPlayerInfoEntity>.Filter.Eq("_id", playerInfoId);
  //var newBravoEntity = new BravoEventEntity();
  //var update = Builders<PocketHiPlayerInfoEntity>.Update.Set("BravoEvent", newBravoEntity);
  //var result = playerInfoCollection.UpdateOne(filter, update);

  //var bravoCollection = db.GetCollection<BravoEventEntity>("bravoEventEntities");
  //bravoCollection.InsertOne(newBravoEntity);
  //userPlayerInfo.BravoEvent = newBravoEntity;
```