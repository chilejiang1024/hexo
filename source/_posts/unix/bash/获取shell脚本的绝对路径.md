---
title: 获取shell脚本的绝对路径
date: 2017-04-18 04:32:55
tags:
    - unix
    - bash
categories: unix
---


```
#获取当前脚本所在绝对路径，需在脚本文件里方能执行
cur_dir=$(cd "$(dirname "$0")"; pwd)
```
