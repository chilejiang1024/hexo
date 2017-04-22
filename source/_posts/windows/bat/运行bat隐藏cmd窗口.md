---
title: 运行bat隐藏cmd窗口
date: 2017-04-18 16:42:57
tags:
    - windows
    - bat
    - cmd
categories: windows
---


### 在运行bat脚本的时候, 隐藏cmd窗口

```
Set ws = CreateObject("Wscript.Shell")
ws.run "cmd /c start.bat",0
ws.run "cmd /c start.bat",5
```

把以上内容另存为到一个`.vbs`中, 双击该vbs脚本, 可以实现 :

执行start.bat, 而不打开命令行窗口.



