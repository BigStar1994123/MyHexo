---
title: MongoDB C# Driver 的一些東西
tags:
  - 工作
  - MongoDB
  - Document Database Providers
category:
  - 程式語言
date: 2018-10-22 15:59:56
---
# MongoDB #

## MongoDb Host ##

[The mongo Shell](https://docs.mongodb.com/manual/mongo/)

## MongoDb Index ##

[雷伊的工作心得 : [mongoDB]index功能的筆記](https://blog.xuite.net/flyingidea/blog/68050501-%5BmongoDB%5Dindex%E5%8A%9F%E8%83%BD%E7%9A%84%E7%AD%86%E8%A8%98)

## EntityFrameworkCore MongoDb Provider ##

更新之後dbcontext都壞了  
今天終於找到原因  
我之前都用`BsonDateTime`存日期  
現在Provider改用`DateTime`去存  
然後就爆炸了  

另一點是不能使用`IList`做為宣告
```
 because it is of type 'IList<string>' which is not a supported primitive type or a valid entity type.
```

`List`似乎也是
```
 because it is of type 'List<string>' which is not a supported primitive type or a valid entity type.
```