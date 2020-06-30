---
title: C# List Except 需要使用自訂的 IEqualityComparer 去比對
tags:
  - C#
  - List
category:
  - 程式語言
date: 2018-10-18 10:11:21
---
# List.Except 使用 Custom Class 做比對 #

需要自定義 IEqualityComparer  

[[筆記]C# 用Except做差集資料比對 實作紀錄](https://dotblogs.com.tw/noncoder/2018/06/07/except)  

不小心查到 LINQ Except 的 Source Code  
[Github : dotnet/corefx](https://github.com/dotnet/corefx/blob/master/src/System.Linq/src/System/Linq/Except.cs)