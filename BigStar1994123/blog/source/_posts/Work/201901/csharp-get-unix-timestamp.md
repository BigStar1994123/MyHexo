---
title: 如何在 C# 內取得 Unix TimeStamp
tags:
  - 工作
  - C#
  - Unix TimeStamp
category:
  - 工作日誌
  - 2019
  - 1月
date: 2019-01-23 19:48:29
---
# 如何在 C# 內取得 Unix TimeStamp #

## 方法一 ##

```C#
var unixTimestamp = (Int32)(DateTime.UtcNow.Subtract(new DateTime(1970, 1, 1))).TotalSeconds;
```

## 方法二 ##

```C#
var foo = DateTime.UtcNow;
long unixTime = ((DateTimeOffset)foo).ToUnixTimeSeconds();
```

[StackOverflow : How to get the unix timestamp in C#](https://stackoverflow.com/questions/17632584/how-to-get-the-unix-timestamp-in-c-sharp)