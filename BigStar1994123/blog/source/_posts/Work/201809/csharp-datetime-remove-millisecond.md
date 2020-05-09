---
title: C# 移除 Datetime 後 Millisecond 的部分
tags:
  - 工作
  - C#
  - Datetime
category:
  - 工作日誌
  - 2018
  - 9月
date: 2018-09-27 11:45:32
---
# C# remove milliseconds #

millisecond 在 Datetime 內是用`Ticks`去做增減  

```C#
public static DateTime Trim(this DateTime date, long ticks)
{
   return new DateTime(date.Ticks - (date.Ticks % ticks), date.Kind);
}
```

參考  
[StackOverflow : Have datetime.now return to the nearest second](https://stackoverflow.com/questions/21704604/have-datetime-now-return-to-the-nearest-second)