---
title: ASP.NET Core C# 模擬輸入密碼
tags:
  - 工作
  - ASP.NET Core
  - C#
category:
  - 工作日誌
  - 2018
  - 12月
date: 2018-12-05 12:15:57
---
# C# Console 不顯示密碼 #

[StackOverflow: C# Console - hide the input from console window while typing](https://stackoverflow.com/questions/23433980/c-sharp-console-hide-the-input-from-console-window-while-typing)  

這個解答更棒  
[StackOverflow: Password masking console application](https://stackoverflow.com/questions/3404421/password-masking-console-application)  

```
string pass = "";
do
{
    ConsoleKeyInfo key = Console.ReadKey(true);
    // Backspace Should Not Work
    if (key.Key != ConsoleKey.Backspace && key.Key != ConsoleKey.Enter)
    {
        pass += key.KeyChar;
        Console.Write("*");
    }
    else
    {
        if (key.Key == ConsoleKey.Backspace && pass.Length > 0)
        {
            pass = pass.Substring(0, (pass.Length - 1));
            Console.Write("\b \b");
        }
        else if(key.Key == ConsoleKey.Enter)
        {
            break;
        }
    }
} while (true);
```