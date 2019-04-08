---
title: react的UI库antd
date: 2018-01-11 11:32:54
tags: antd
---
官网antd：https://ant.design/docs/react/introduce-cn
antd的依赖安装
``` bash
  npm install antd --save
```
UI库的引入组件按需加载，安装依赖
``` bash
  npm install babel-plugin-import --save-dev
```
到这里还没有完，还需要做一些配置，在“.babelrc”文件夹下，添加如下配置

"plugins": [

    ["import", {libraryName: "antd", style: "css"}] // import js and css modularly (css built files)

  ]
 另外注意react的.js代码里的字符串要用单引号，注意空格问题



