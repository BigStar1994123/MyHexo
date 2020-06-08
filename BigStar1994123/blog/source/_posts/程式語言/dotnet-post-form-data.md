---
title: ASP.NET Core C# Post Form Data
tags:
  - ASP.NET Core
  - C#
  - HttpClient
category:
  - 程式語言
date: 2018-12-05 12:15:57
---
# ASP.NET Core 要怎麼 Post Form Data using HttpClient #

這樣就可以  
[StackOverflow: How to post data using HttpClient?](https://stackoverflow.com/questions/20005355/how-to-post-data-using-httpclient)  

```C#
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

```C#
var stringContent = await response.Content.ReadAsStringAsync();
```
