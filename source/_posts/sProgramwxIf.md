---
title: 小程序的wx:if判断
date: 2018-01-16 18:22:22
tags: wx:if 小程序滚动条
---
写这篇文章之前，在想要不要写，后来还是写吧，毕竟是遇到过的问题，经过一番周折才解决掉的，写来就作为提醒吧，
微信小程序判断多个条件可以用wx:if wx:elif wx:else的方法
具体用法上代码
```bash
<view class="small_num"  style="color:green" wx:if="{{dayLtePrateT=='下降'}}">{{dayLtePrateT}}{{dayLtePrate}}</view>
<view class="small_num"  style="color:#999999;box-shadow:0 0 0 1px #d9d9d9 inset" wx:elif="{{dayLtePrateT=='持平'}}">{{dayLtePrateT}}{{dayLtePrate}}</view>
<view class="small_num"  style="color:#f5222d" wx:else>{{dayLtePrateT}}{{dayLtePrate}}</view>
```
这就是在工作中遇到的问题，要根据返回的数据内容是"增加","下降","持平"的不同内容 来确定她们的不同样式，当然这也可通过直接操作数据的形式达到效果,或者通过在dom树上用“三目运算”的方式解决（判断三个条件，用三目运算符的方法好像不好处理）不过自己感觉这个方法简单一点。
``` bash
  小程序滚动条
```
另外多说一句吧，有时候在页面的最外层加了“scroll-view”的标签，页面的底部还会有横向的滚动条,（“scroll-view”的作用是"可滚动视图区域",包括许多属性，包括"scroll-x"和"scroll-y"）解决办法是把"scroll-view"标签，改成"scroll-y"标签，意思是不允许横向滚动，另外去掉纵向的默认的滚动条的方法是在最外层的标签加上样式
``` bash
page::-webkit-scrollbar {
    display: none;
}
```
