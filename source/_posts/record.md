---
title: 工作杂结
date: 2019-03-31 19:18:26
tags: 样式 兼容
---

#### 这里是工作中遇到的一些问题，记录下来，以便用时参考

##### pc端input标签的type为number时候去掉右侧加减按钮的方法
```
/*谷歌*/
input::-webket-outer-spin-button,
input::-webket-inner-spin-button {
    -webket-appearance: none;
    appearance:none;
    margin:0;
}
/*火狐*/
input {
    -moz-appearance:textfield;
}
```
##### 手机端页面点击按钮时去掉其黑边阴影的方法

```
标签添加样式
{-webkit-tap-highlight-color: transparent;}
//去掉button默认的样式
button {botder:0;background-color:transparent}
//去掉input的默认样式
input{background:none;-webkit-appearance:none};
```
##### 改变input挂光标的颜色
```
 改变input的鼠标的光标颜色input{caret-color:'颜色值'}
```
##### 移动端去掉alert弹框头部的默认网址
```
//js里面添加代码
window.alert = function(name){
	var iframe = document.createElement("IFRAME");
	iframe.style.display="none";
	iframe.setAttribute("src", 'data:text/plain,');
	document.documentElement.appendChild(iframe);
	window.frames[0].window.alert(name);
	iframe.parentNode.removeChild(iframe);
}
```
##### css3的transform不兼容ie9，解决办法是在其前面加前缀 -ms-
##### ie9下渐变色不兼容，解决办法是见传送门：https://www.jb51.net/css/173486.html
##### 小程序tabbar中间图标突出的实现方式见传送门： https://www.jianshu.com/p/ce1c3c25527c
##### 小程序获取城市地理位置的传送门： https://blog.csdn.net/weixin_42262436/article/details/80458430
##### setInterval和setTimeout的区别
```
setInterval（定时器）：规定多长时间执行一次，可执行多次；
setTimeout（延时调用）: 再过多久执行一次，且只执行一次；
```