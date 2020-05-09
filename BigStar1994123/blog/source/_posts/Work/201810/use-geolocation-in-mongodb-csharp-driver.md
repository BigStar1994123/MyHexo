---
title: 在 MongoDB C# Drvier 使用 GeoLocation
tags:
  - 工作
  - C#
  - MongoDB
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-10-03 12:44:02
---
# GeoLocation in MongoDb C# Driver #

先記起來  
https://stackoverflow.com/questions/6993249/mongodb-geospatial-index-in-c-sharp  
https://stackoverflow.com/questions/17807577/how-to-create-indexes-in-mongodb-via-net  
https://stackoverflow.com/questions/30829282/findall-in-mongodb-net-driver-2-0  
https://stackoverflow.com/questions/33807787/mongo-db-near-query-in-c  

```
var gp =new GeoJsonPoint<GeoJson2DGeographicCoordinates>(new GeoJson2DGeographicCoordinates(coordinates[0], coordinates[1]));
var query=Builders<BsonDocument>.Filter.Near("Geo",gp,radius);
var result = await col.Find(query).ToListAsync();
```