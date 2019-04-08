---
title: Windows下如何查看某个端口被谁占用
date: 2017-11-05 21:10:57
tags: 端口占用
---
这里我们以4000端口为例
1、按下win+R调出命令行窗口，输入netstat -aon|findstr "4000" ，找到指定的一列数字，这里是"9136"

![logo](tool/port.png)

2、输入tasklist|findstr "9136"，发现是
![logo](tool/port1.png)
3、再次输入taskkill /f /t /im node.exe结束该进程