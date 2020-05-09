---
title: ASP.NET Core C# Post Form Data
tags:
  - 工作
  - ASP.NET Core
  - C#
category:
  - 工作日誌
  - 2018
  - 12月
date: 2018-12-05 12:15:57
---
# ASP.NET Core 要怎麼 Post Form Data #

似乎這樣就可以  
[StackOverflow: How to post data using HttpClient?](https://stackoverflow.com/questions/20005355/how-to-post-data-using-httpclient)  
```
var comment = "hello world";
var questionId = 1;

var formContent = new FormUrlEncodedContent(new[]
{
    new KeyValuePair<string, string>("comment", comment),
    new KeyValuePair<string, string>("questionId", questionId)
});

var myHttpClient = new HttpClient();
var response = await myHttpClient.PostAsync(uri.ToString(), formContent);

```

And if you need to get the response after post, you should use:  

```
var stringContent = await response.Content.ReadAsStringAsync();
```