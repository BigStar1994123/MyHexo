---
title: MongoDB C# Driver 簡易使用方式
tags:
  - 工作
  - MongoDB
  - C#
category:
  - 工作日誌
  - 2018
  - 11月
date: 2018-11-30 09:58:23
---
# 這篇 MongoDb C# Driver 的教學真低不錯 #

[C#操作MongoDB的簡單實例](https://hk.saowen.com/a/34794073f951e271d96c7cba6c78fcdefe240660afcd6dbb7ca133b687e65998)

下面這篇感覺就普普了 不過也是可以拿來做參考  
[在ASP.NET Core2上操作MongoDB就是能這麼的簡便酷爽（自動完成分庫分表)](https://hk.saowen.com/a/7bbc17c76d18582f718d80cfce5cafd3bcbc01ae34c273a52e9d42a32c8001b8)  

如何 Deserialize BsonValue  
[StackOverflow: Mongo C# Driver: Deserialize BsonValue](https://stackoverflow.com/questions/6700662/mongo-c-sharp-driver-deserialize-bsonvalue)  

以下是節錄部分我的 Code 主要是將一個 array string 轉成 array Object  
命名的很隨便 隨便參考就行  
```
  Console.WriteLine("Hello World.");
  var mongoServer = new MongoServer();
  var bList = mongoServer.Find("eventEntities", new BsonDocument());
  foreach (var b in bList)
  {
      if (b["BravoEvent"] == BsonNull.Value)
      {
          continue;
      }

      var filter = new BsonDocument
      {
          { "_id", b["_id"]}
      };

      var originCollection = b["BravoEvent"]["PossessedBravos"];
      var stringList = BsonSerializer.Deserialize<List<string>>(originCollection.ToJson());
      if (stringList.Count == 0)
      {
          continue;
      }

      var bArray = new BsonArray();
      foreach(var s in stringList)
      {
          bArray.Add(new BsonDocument { { "CollectionName", s }, { "CollectedTime", DateTime.Now } });
      }

      b["BravoEvent"]["PossessedBravos"] = bArray;

      mongoServer.Update("eventEntities", filter, b);
      Console.WriteLine(b["BravoEvent"]["PossessedBravos"]);
  }

  Console.WriteLine("Finish");
  Console.Read();
```