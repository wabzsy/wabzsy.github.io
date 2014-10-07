image: "http://blog-for-wabzsy.qiniudn.com/images/在MaxOSX中修改文件扩展名时不再显示警告框"
title: 在MaxOSX中修改文件扩展名时不再显示警告框
description: " "
categories: 技术日志
tags:
  - MacOSX
date: 2014-10-07 23:08:05
---
每当在我修改文件扩展名时,Mac总会弹出这样一个提示框:

![]({{image}}/1.png)

怎么将它去掉呢?其实很简单,只要打开__`终端`__,在里面输入如下命令:

``` bash
defaults write com.apple.finder FXEnableExtensionChangeWarning -bool false
```

然后回车,再输入:

``` bash
killall Finder
```

这样这个警告框就被禁用了~

如果想恢复这个提示框,可以用这个命令:

``` bash
defaults write com.apple.finder FXEnableExtensionChangeWarning -bool true
```

回车,再输入:

``` bash
killall Finder
```

就这样~

