---
title: C# 檢查 Regular Expression 正確
date: 2018-12-14 16:13:06
tags:
  - 工作
  - C#
  - Regular Expression
category:
  - 工作日誌
  - 2018
  - 12月
---
# C# 檢查 Regular Expression #

就醬  
```
var match = Regex.Match(input, regex, RegexOptions.IgnoreCase);

if (!match.Success)
{
    // does not match
}
```

## 檢查 Regex 正確的一個網站 ##

[regex101](https://regex101.com/)  