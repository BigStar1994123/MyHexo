---
title: 過濾掉不合法的字元 使用 Regular Expression
tags:
  - 工作
  - Regex
  - Regular Expression
category:
  - 工作日誌
  - 2019
  - 1月
date: 2019-01-02 18:43:05
---

# 過濾掉不合法的字元 使用 Regular Expression #

醬子用就可以了  
`[^\W_]+`  

```C#
string s = @"zoo13579~!多奇數位@_$#%^%$&*().,>?]";
string r = Regex.Replace(s, @"[\W_]+", "");
```

[The Will Will Web : 如何利用 .NET 的 Regex 過濾所有特殊字元 (其他語言適用)](https://blog.miniasp.com/post/2010/04/27/How-to-filter-special-characters-using-NET-Regex.aspx)