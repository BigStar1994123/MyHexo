---
title: ASP.NET Core 寫入文字檔案
tags:
  - ASP.NET Core
  - C#
  - File
category:
  - 程式語言
date: 2018-12-05 12:15:57
---
# ASP.NET Core 寫入文字檔案 #

[StackOverflow: How to write to a file in .NET Core?](https://stackoverflow.com/questions/35310078/how-to-write-to-a-file-in-net-core)  

大概長這樣  

```C#
var logPath = System.IO.Path.GetTempFileName();
var logFile = System.IO.File.Create(logPath);
var logWriter = new System.IO.StreamWriter(logFile);
logWriter.WriteLine("Log message");
logWriter.Dispose();

```
