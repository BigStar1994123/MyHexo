---
title: Git Authentication Fail 不給輸入帳號密碼
tags:
  - 工作
  - Git
category:
  - 工作日誌
  - 2019
  - 1月
date: 2019-01-22 10:25:30
---
# Git Push 上雲端有時出現 Authentication fail 的問題 然後又不給你輸入帳號密碼 #

## 解決方法1 ##

```Cmd
git config --system --unset credential.helper
```

## 解決方法2 ##

我個人是用這招  
因為方法1無效  

刪除 .gitconfig [credential]部分  

```
[user]
    name = luozheng
    email = qssq666@foxmail.com
[credential]
    helper = manager
```

改成  

```
[user]
    name = luozheng
    email = qssq666@foxmail.com
```

## 參考資料 ##

[fatal: Authentication failed for又不弹出用户名和密码 解决办法](https://www.jianshu.com/p/8a7f257e07b8)