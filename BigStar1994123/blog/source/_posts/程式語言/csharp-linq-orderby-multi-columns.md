---
title: LINQ 依照多個 Columns 的排序方法
tags:
  - LINQ
  - C#
category:
  - 程式語言
date: 2019-01-23 19:48:29
---
# LINQ 依照多個 Columns 的排序方法 #

```C#
var list = new List<MyObject>{...};

var newList = list.Orderby(x => x.Id).ThenByDescending(x => x.Name).ToList();
```
