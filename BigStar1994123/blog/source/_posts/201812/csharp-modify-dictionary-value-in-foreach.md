---
title: 在 Foreach Dictionary 改數值
tags:
  - 工作
  - C#
  - Foreach
  - Dictionary
category:
  - 工作日誌
  - 2018
  - 12月
date: 2018-12-13 12:05:16
---
# 我想在 Foreach Dictionay 的時候改變數值 #

會跑錯誤呢 因為不能在 Foreach 時改值  
該怎麼做呢  

 1. Clone 一個 Dictionary出來
 2. 或是在使用時加上 Tolist()，原理與1相同但看起來簡潔許多

[Github: Editing dictionary values in a foreach loop](https://github.com/DavidAnson/markdownlint/blob/v0.11.0/doc/Rules.md#md032)  