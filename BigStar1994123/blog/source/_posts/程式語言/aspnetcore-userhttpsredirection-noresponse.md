---
title: ASP.NET Core UserHttpsRedirection 無憑證無 Response 問題
tags:
  - ASP.NET Core
  - Postman
category:
  - 程式語言
date: 2018-10-23 11:01:36
---
# ASP.NET Core 內在 app.UserHttpsRedirection() 後 Postman 打 沒反應的問題 #

此問題發生原因是在本機端沒有憑證用於Https，  
可在自身專案內加入一個開發用的憑證，  
`dotnet dev-certs https --help`  
醬子應該就可以用了  
[Configuring HTTPS in ASP.NET Core 2.1](https://asp.net-hacker.rocks/2018/07/05/aspnetcore-ssl.html)  