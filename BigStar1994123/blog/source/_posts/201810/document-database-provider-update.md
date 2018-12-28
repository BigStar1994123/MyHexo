---
title: Document Database Providers Update
tags:
  - 工作
  - EntityFramework
  - Document Database Providers
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-10-23 11:01:36
---
# MongoDb EntityFramework Provider 更新之後要改好多東西 #

1. IList >> List
2. BsonDateTime >> DateTime

強制要改，否則實體會炸開來，  
最後

3. List\<string>不可用，出現 `list<string> is not a supported primitive type or a valid entity type`  

原生的EntityFramework的限制的樣子  
感謝鮑大人幫我找到解法  
[StackOverflow : How to persist a list of strings with Entity Framework Core?](https://stackoverflow.com/a/52499249)  
利用 `Entity Framework Core 2.1` 的 `Value Conversions` 可解  

比較之前的 EF 就只能 List property 掛個 `[Notmapped]` 然後配合用 Json.NET 或 Automapper 把顯示出來的和存起來的做轉換

4. Dictionary\<string, MyObject>也不可用，出現同3的錯誤

一樣利用 `Value Conversions` 可解  
[Jerrie Pelser : Store a Dictionary as a JSON string using EF Core 2.1](https://www.jerriepelser.com/blog/store-dictionary-as-json-using-ef-core-21)  