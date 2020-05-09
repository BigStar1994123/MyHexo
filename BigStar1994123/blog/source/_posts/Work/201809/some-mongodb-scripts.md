---
title: 紀錄一下MongoDb語法
tags:
  - 工作
  - MongoDB
category:
  - 工作日誌
  - 2018
  - 9月
date: 2018-09-27 11:45:32
---
# 紀錄一下MongoDb語法 #

```MongoDB
db.supplyPoints.find({ Location:
   { $geoWithin:
      { $centerSphere: [ [ 121.57501, 25.07812 ], 5 / 3963.2 ] } } })
```

```MongoDB
db.supplyPoints.createIndex({ Location: "2dsphere" })

var METERS_PER_MILE = 1609.34
db.supplyPoints.find({ Location: { $nearSphere: { $geometry: { type: "Point", coordinates: [ 121.57501, 25.07812 ] }, $maxDistance: 5 * METERS_PER_MILE } } })
```