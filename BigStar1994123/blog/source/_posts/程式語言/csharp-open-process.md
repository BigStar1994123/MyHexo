---
title: C# 程式碼中開啟其他程式
date: 2018-12-14 16:13:06
tags:
  - C#
  - CMD
category:
  - 程式語言
---
# C# with Open Something #

要打開一些玩意兒  
比如說要用 nodepad 打開  
就可以用以下語法  

```C#
Process.Start("notepad.exe", fileName);
```

也可以用 CMD 開  

```CMD
var proc = Process.Start(@"cmd.exe ",@"/c C:\Users\user2\Desktop\XXXX.reg")
```

最後我使用  

```
  var process = new Process
  {
      StartInfo = new ProcessStartInfo
      {
          WindowStyle = System.Diagnostics.ProcessWindowStyle.Hidden,
          FileName = "python.exe",
          Arguments = $"openWindow.py {loginInfo.CompanyId} {loginInfo.EmpId} {DecryptString(loginInfo.Pwd, _encryptKey)}"
      }
  };
  process.Start();

```
