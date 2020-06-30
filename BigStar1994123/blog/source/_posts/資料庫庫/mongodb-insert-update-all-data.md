---
title: MongoDB insert/update all data
tags:
  - MongoDB
category:
  - 資料庫庫
date: 2018-10-18 10:11:21
---
# MongoDB 的一些 Script #

`insert for all data`  
db.BravoEventPoints.update({}, {$set : {"StartTime" : new ISODate("2012-01-10")} }, {upsert:false, multi:true})  
[StackOverflow : Mongodb Add new field to every document](https://stackoverflow.com/questions/7714216/add-new-field-to-every-document-in-a-mongodb-collection)  

`// update for all data`  
db.BravoEventPoints.update({}, {$set: {"EndTime" : null }}, {multi:true})  
db.BravoEventPoints.updateMany({},{$set: {"StartTime" : null }})  
[StackOverflow : Mongodb update all](https://stackoverflow.com/questions/9038547/mongodb-update-every-document-on-one-field)  