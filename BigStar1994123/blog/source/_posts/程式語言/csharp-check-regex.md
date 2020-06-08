---
title: C# 檢查 Regular Expression 正確
date: 2018-12-14 16:13:06
tags:
  - C#
  - Regex
  - Regular Expression
category:
  - 程式語言
---
# C# 檢查 Regular Expression #

就醬  

```C#
var match = Regex.Match(input, regex, RegexOptions.IgnoreCase);

if (!match.Success)
{
    // does not match
}
```

## 檢查 Regex 正確的一個網站 ##

[regex101](https://regex101.com/)  
