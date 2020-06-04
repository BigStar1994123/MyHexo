---
title: 如何同時間打很多個 Request
tags:
  - C#
  - Task
category:
  - 程式語言
date: 2019-01-02 18:36:10
---
# 如何同時間打很多個 Request (這算 DDOS?) #

[StackOverflow : C# - how to do multiple web requests at the same time](https://stackoverflow.com/questions/52338042/c-sharp-how-to-do-multiple-web-requests-at-the-same-time)  

```C#
await Task.WhenAll(requests);
```
