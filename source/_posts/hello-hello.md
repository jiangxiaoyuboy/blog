---
title: 移动端适配方案 flexible.js
toc: true
date: 2017-10-28 16:10:59
tags: 移动适配
---
``` bash
  $flexible.js 有什么用
```
正如文章标题所写的那样，它就是一个终端设备适配的解决方案。也就是说它可以让你在不同的终端设备中实现页面适配。
``` bash
  $flexible.js 怎么用
```
 ##flexible.js 的用法非常的简单，在页面的<head></head>中引入 flexible_css.js,flexible.js文件：
 // 加载阿里CDN的文件
 ``` bash
  <script src="http://g.tbcdn.cn/mtb/lib-flexible/0.3.4/??flexible_css.js,flexible.js"></script>
```
除了上面这种方式外，你还可以把这两个文件下载到自己的项目中，然后再引入，效果是一样的。
事实上 flexible.js 做了下面三件事：
	1、动态改写标签
	2、给<html>元素添加data-dpr属性，并且动态改写data-dpr的值
	3、给<html>元素添加font-size属性，并且动态改写font-size的值
说得简单点就是 rem 相当于我们平常用的百分比，只不过 rem 是相对根元素的。而我们的根元素是根据终端屏幕大小来动态设置的，所以不管是 iphone 6 plus 还是 iphone6，或者是其它任何终端设备都可以很完美地还原设计稿。

还有一个关于 px 转 rem 的，你也不用自己一个一个手动去换算，这里有一个插件你可以安装下，它会自动地帮你把 px 换算成 rem 。

传送门：https://github.com/flashlizi/cssrem