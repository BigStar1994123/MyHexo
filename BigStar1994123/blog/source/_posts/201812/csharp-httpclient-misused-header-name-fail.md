---
title: C# HttpClient misused header name fail
tags:
  - 工作
  - C#
  - HttpClient
  - HTTP
category:
  - 工作日誌
  - 2018
  - 12月
date: 2018-12-13 12:05:16
---
# C# 使用 HttpClient 的時候出現 Misused header name. 的 Fail #

我的用法是醬子  
```
  httpClient.DefaultRequestHeaders.Add("Content-Type", "application/json");

```

沒錯 跟智障一樣  
解法可用  
```
  httpClient.DefaultRequestHeaders.Add("Accept", "application/json");

```

或是  
```
  httpClient.DefaultRequestHeaders
            .Accept
            .Add(new MediaTypeWithQualityHeaderValue("application/json")); //ACCEPT header

```

[Github: How do you set the Content-Type header for an HttpClient request?](https://stackoverflow.com/questions/10679214/how-do-you-set-the-content-type-header-for-an-httpclient-request)  

[Wikipedia: HTTP Header](https://zh.wikipedia.org/zh-tw/HTTP%E5%A4%B4%E5%AD%97%E6%AE%B5)