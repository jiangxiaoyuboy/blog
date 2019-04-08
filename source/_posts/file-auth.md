---
title: 如何删除需要管理员权限才能删除的文件夹
date: 2017-12-28 11:22:39
tags:
---
在Windows 7系统运行中。往往会遇到想要删除某个文件夹时，系统提示：文件夹访问被拒绝 你需要权限来执行此操作，如何才能删除此类文件夹呢？
删除需要管理员权限才能删除的文件夹的方法
方法一：制作一个管理员授权的文件，把这个文件加入注册表
步骤：
开始 - 运行（输入notepad）- 确定或者回车,打开记事本（出可以从：开始-所有程序-附件-记事本）；
在打开的记事本中复制下列文件：
Windows Registry Editor Version 5.00 
[HKEY_CLASSES_ROOT\*\shell\runas] 
@="管理员授权" 
 "NoWorkingDirectory"=""  
[HKEY_CLASSES_ROOT\*\shell\runas\command] 
 @="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant administrators:F" 
 "IsolatedCommand"="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant
 administrators:F"  
[HKEY_CLASSES_ROOT\exefile\shell\runas2] 
@="管理员授权" 
 "NoWorkingDirectory"=""  
[HKEY_CLASSES_ROOT\exefile\shell\runas2\command] 
 @="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant administrators:F" 
 "IsolatedCommand"="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant 
administrators:F"  
[HKEY_CLASSES_ROOT\Directory\shell\runas]
 @="管理员授权"  
"NoWorkingDirectory"=""  
[HKEY_CLASSES_ROOT\Directory\shell\runas\command] 
 @="cmd.exe /c takeown /f \"%1\" /r /d y && icacls \"%1\" /grant administrators:F /t"
 "IsolatedCommand"="cmd.exe /c takeown /f \"%1\" /r /d y && icacls \"%1\" /grant
 administrators:F /t" 

 点记事本左上角的“文件” - 另存为 ，在另存为窗口下面的：文件名（N）中输入：管理员授权.reg ，再点：保存；

 这时桌面上会有一个：管理员授权.reg的注册表文件，

我们左键双击：管理员授权.reg文件，在弹出的：注册表编辑器窗口点：是（Y）；

在点是以后弹出的窗口中点：确定，我们右键单击一个文件夹，会看到右键菜单中有：管理员授权的菜单。

如果我们要删除文件夹，则右键该文件夹 - 运行管理员授权，再删除该文件夹就可以顺利地删除了。
