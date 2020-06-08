---
title: ASP.NET Core C# Json 序列化/反序列化
tags:
  - ASP.NET Core
  - C#
  - Json
category:
  - 程式語言
date: 2018-12-05 12:15:57
---
# ASP.NET Core Json 序列化/反序列化 ##

[StackOverflow: JSON serialization/deserialization in ASP.Net Core](https://stackoverflow.com/questions/29841503/json-serialization-deserialization-in-asp-net-core)  

```C#
#using Newtonsoft.Json
....
JsonConvert.DeserializeObject(json);
```
