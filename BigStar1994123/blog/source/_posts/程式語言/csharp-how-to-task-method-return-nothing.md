---
title: Task 方法不回傳任何東西的方法
tags:
  - C#
  - Task
category:
  - 程式語言
date: 2019-01-16 18:17:08
---
# Task Return Nothing #

```C#
Task Method1()
{
  return Task.FromResult(0);
  // or  
  // return Task.FromResult<object>(null);
}
```

```C#
async Task Method1()
{
  // 啥都不用幹
}
```

參考這邊  
[StackOverflow : If my interface must return Task what is the best way to have a no-operation implementation?](https://stackoverflow.com/questions/13127177/if-my-interface-must-return-task-what-is-the-best-way-to-have-a-no-operation-imp)