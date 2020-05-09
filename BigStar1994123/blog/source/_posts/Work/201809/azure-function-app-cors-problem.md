---
title: 20180917工作日誌
tags:
  - 工作
  - Azure
  - Azure Function Application
  - CORS
category:
  - 工作日誌
  - 2018
  - 9月
date: 2018-09-17 18:55:03
---
# Azure Function Proxy CORS 問題解決方式 #

今天要做 QRCode for dynamic url ，  
想到可以利用 Azure Function 來重新導向，  
手機板正常可使用，  
電腦版瀏覽器會遇到 [CORS(Cross-Origin Resource Sharing)](https://developer.mozilla.org/zh-TW/docs/Web/HTTP/CORS) 的問題。  

解決方式如下：  
[Micorsoft : Docs](https://docs.microsoft.com/en-us/sandbox/functions-recipes/proxies#creating-an-http-redirect)  
[Medium : Use Azure Functions Proxies to solve CORS issues](https://medium.com/@Sneezry/use-azure-functions-proxies-to-solve-cors-issues-572916535fca)  