---
title: C# 使用 HttpClient 進行 Post 動作
date: 2018-12-14 16:13:06
tags:
  - C#
  - HttpClient
category:
  - 程式語言
---
# C# Post by HttpClient #

大概是醬  

```C#
var content = new StringContent(jsonObject.ToString(), Encoding.UTF8, "application/json");
var result = client.PostAsync(url, content).Result;
```  

[StackOverflow: POSTing JsonObject With HttpClient From Web API](https://stackoverflow.com/questions/6117101/posting-jsonobject-with-httpclient-from-web-api)  
