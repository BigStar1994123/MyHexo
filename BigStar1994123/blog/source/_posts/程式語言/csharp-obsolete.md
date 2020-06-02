---
title: C# 標示方法或變數已過時
tags:
  - C#
  - Obsolete
category:
  - 程式語言
date: 2019-01-16 18:26:15
---
# C# 標示方法已過時 #

這樣做  

```C#
[Obsolete("Method1 is deprecated, please use Method2 instead.")]
public void Method1()
{ … }
```

也可以這樣  

```C#
[Obsolete("Method1 is deprecated, please use Method2 instead.", true)]
```

其中 True 表示編譯時 Error  

```C#
Obsolete(String Message, Bool error)
```
