---
title: css中position的用法
date: 2018-11-19 21:25:42
tags: css position
---

## position的用法

提起css中的position的值，想必应该都知道，如absolute,relative,fixed,static,


值|描述
--|--
absolute|生成绝对定位，相对于static定位以外的第一个父元素进行定位。
relative|生成相对定位，相对于正常位值进行定位。
fixed|生成固定定位，相对于浏览器窗口进行定位。
static|默认值。没有定位，元素出现在正常的流中。
不过现在要说的不是要说这些，因为之前切页面的时候遇到过关于position的文档流的问题，所以现在梳理一下，做下记录。
其中 ***absolute*** 和 ***fixed*** 是**脱离文档流**的，另absolute和float虽然都脱离了文档流，在float脱离文档流的时候虽然其他盒子无视他，但是盒子中的文本围绕他，而absolute脱离文档流会造成其他盒子和盒子的文本无视他。


 