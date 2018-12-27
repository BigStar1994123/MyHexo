---
title: ASP.NET Core 使用 HttpClientFactory with Polly
tags:
  - 工作
  - ASP.NET Core
  - HttpClient
  - Polly
category:
  - 工作日誌
  - 2018
  - 12月
date: 2018-12-11 12:52:46
---
# .NET Core 中正確使用 HttpClient #

HttpClientFactory 好像蠻好用的  
[Liam Wang: .NET Core 中正确使用 HttpClient 的姿势](https://www.cnblogs.com/willick/p/net-core-httpclient.html)

## .Net Core 中結合 HttpClientFacotry 使用 Polly ##

基本上就是這篇的中譯  
[Github: Polly: Polly and HttpClientFactory](https://github.com/App-vNext/Polly/wiki/Polly-and-HttpClientFactory)  

[Liam Wang: 在 .NET Core 中结合 HttpClientFactory 使用 Polly（上篇）](https://www.cnblogs.com/willick/p/HttpClientFactory-Polly-1.html)  
[Liam Wang: 在 .NET Core 中结合 HttpClientFactory 使用 Polly（中篇）](https://www.cnblogs.com/willick/p/HttpClientFactory-Polly-1.html)  
[Liam Wang: 在 .NET Core 中结合 HttpClientFactory 使用 Polly（下篇）](https://www.cnblogs.com/willick/p/HttpClientFactory-Polly-1.html)  

## Request 失敗就一直重 Try 的專有名詞 ##

叫做 Exponential-Backoff
[Github: Polly](https://github.com/App-vNext/Polly/wiki/Retry#exponential-backoff)  