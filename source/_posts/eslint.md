---
title: eslint的语法以及错误提示
date: 2018-03-22 17:51:12
tags: eslint
---
ESLint总是推荐用ES6的Template String来拼接字符串，而不能用+号，这个比较烦，毕竟残留代码比较多，所以，禁止掉！
eslint不能用+号做拼接符的报错内容为"Unexpected string concatenation"
禁止掉的方法为，在文件根目录下的eslintrc关掉他的规则
```bash
  {
    'rules': {
      'prefer-template': 'off'
    }
  }
```
另外附上一份eslint的错误提示，传送门:http://www.cnblogs.com/lcddjm/p/6595007.html
一份eslint的规则说明，传送门:http://blog.csdn.net/helpzp2008/article/details/51507428
至于eslint的具体规则可以查询官网http://eslint.cn/
