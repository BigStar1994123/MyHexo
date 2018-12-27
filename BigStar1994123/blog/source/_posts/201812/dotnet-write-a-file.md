---
title: ASP.NET Core 寫入文字檔案
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
# ASP.NET Core 寫入文字檔案 #

[StackOverflow: How to write to a file in .NET Core?](https://stackoverflow.com/questions/35310078/how-to-write-to-a-file-in-net-core)  

大概長這樣  
```
var logPath = System.IO.Path.GetTempFileName();
var logFile = System.IO.File.Create(logPath);
var logWriter = new System.IO.StreamWriter(logFile);
logWriter.WriteLine("Log message");
logWriter.Dispose();

```