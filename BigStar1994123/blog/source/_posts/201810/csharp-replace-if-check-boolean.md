---
title: C# 取代 IF 的 Boolean Check 方式
tags:
  - 工作
  - C#
  - Boolean
category:
  - 工作日誌
  - 2018
  - 10月
date: 2018-11-01 11:36:02
---
# C# 取代 if 內的 boolean check #

有沒有想過為什麼 if (int)  
當 int > 0 return true else return false  

可以用 `implicit operator bool`  
[StackOverflow : implicit operator bool](https://stackoverflow.com/questions/21485644/implicit-bool-and-operator-override-handle-if-statements-correctly)  
