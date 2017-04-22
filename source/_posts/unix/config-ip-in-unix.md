---
title: config ip in unix
date: 2017-03-31 01:47:57
tags:
categories: unix
---


- 1 ifconfig命令
 
第一种使用ifconfig命令配置网卡的ip地址。此命令通常用来零时的测试用，计算机启动后ip地址的配置将自动失效。

具体用法如下: 

```hash
Ipconfig   ethx  ipadd   netmask  x.x.x.x
```

其中ethx中的x代表第几快以太网卡，默认第一块为0.ipadd代表ip地址。x.x.x..x为子网掩码。

例如给网卡eth0配置的ip地址为192.168.1.1 子网掩码为 255.255.255.0

```hash
ifconfig eth0 192.168.1.1 netmask 255.255.255.0
```

PS. 此方法配置的ip地址后计算机从新启动将会失效



- 2 vi  /etc/sysconfig/network-scripts/ifcfg-ethx

```hash
vi /etc/sysconfig/network-scripts/ifcfg-ethx
service network restart
```
