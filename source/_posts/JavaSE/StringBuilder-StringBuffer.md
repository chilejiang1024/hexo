---
title: StringBuilder & StringBuffer
date: 2017-04-18 05:13:44
tags:
    - JavaSE
categories: JavaSE
---


### StringBuilder & StringBuffer

#### 1 简介

String类是不可变类, 任何对String的改变都会引发新的String对象的生成.

StringBuffer则是可变类, 并且是**线程安全的**, 任何对它所指代的字符串的改变都不会产生新的对象.

StringBuilder类**不是线程安全的**, 但其在单线程中的**性能比StringBuffer高**.

#### 2 使用

向下面这么用是不推荐的 :

```
String str = "start";
for(int i = 0; i < 100; i++) {
    str = str + "hello";
}
```

应该这样

```
StringBuilder strBuilder = new StringBuilder("start");
for(int i = 0; i < 100; i++) {
    strBuilder.append("hello");
}
String result = strBuilder.toString();
```

