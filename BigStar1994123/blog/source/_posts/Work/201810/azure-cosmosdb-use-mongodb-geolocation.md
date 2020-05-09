---
title: Azure CosmosDB 使用 MongoDB Geolocation
tags:
  - 工作
  - MongoDB
  - Azure CosmosDB
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-10-17 16:42:52
---
# Azure CosmosDB 使用 MongoDB GeoLocation功能 #

真D好難  

首先先到Azure CosmosDb 你的Collection設定內  
將includedPaths改成  
```
  {
      "path": "/*",
      "indexes": [
          {
              "kind": "Range",
              "dataType": "Number",
              "precision": -1
          },
          {
              "kind": "Range",
              "dataType": "String",
              "precision": -1
          }
      ]
  }
```

然後再用程式碼加入2dsphere的index  
```
  IndexKeysDefinition<BravoPoint> keys = "{ Location: \"2dsphere\" }";
  var indexModel = new CreateIndexModel<BravoPoint>(keys);
  var s = collection.Indexes.CreateOne(indexModel);
```

最後可以得出Result  
```
  var gp = new GeoJsonPoint<GeoJson2DGeographicCoordinates>
      (new GeoJson2DGeographicCoordinates(121.575163, 25.078124));
  var query = Builders<BravoPoint>.Filter.Near("Location", gp, 10000);
  var result = collection.Find(query).ToList();
```

## MongoDb ##

[MongoDB 學習筆記四 C#調用MongoDB](https://blog.csdn.net/xundh/article/details/49449467)