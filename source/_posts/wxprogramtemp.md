---
title: 小程序的组件数据
date: 2018-02-07 18:56:59
tags: 小程序 组件
---
``` bash
  使用小程序组件的数据获取
```
使用小程序组件的时候，有时候需要获取组件中的数据，在获取数据的时候需要在template标签里面通过data来写入，如图所示

![logo](wxprogramtemp/pic1.jpg)
注意data这里等于的后面要加引号

![logo](wxprogramtemp/pic2.jpg)

![logo](wxprogramtemp/pic3.jpg)

另外通过getStorage获取的数据的等，要比在其外面的数据晚执行