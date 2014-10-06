image: "http://blog-for-wabzsy.qiniudn.com/images"
date: 2012-08-22 23:00:59
title: "PHP 获取 文件大小,类型,创建/修改时间"
description: " "
categories: "技术日志"
tags:
  - PHP
---

- 常用函数:

``` php
int filesize(string $filename);//取得文件大小
string filetype(string $filename);//取得文件类型
int filemtime(string $filename);//取得文件修改时间
```

- 获取文件大小:

``` php
<?php
    $filename = 'test.txt';
    echo $filename.'文件大小为: '.filesize($filename).' bytes';
?>
```

- 获取文件类型:

``` php
<?php
    $filename = 'test.txt';
    echo filetype($filename);
?>
```

>  __filetype__ 有八种返回结果:

> __fifo__,__char__,__dir__,__block__,__link__,__file__,__unknown__和__false__

> 常见返回结果主要是__file__和__dir__

- 获取文件修改时间:

``` php
<?php
    $filename = "test.txt";
    echo "$filename 修改日期为：",date("Y-m-d H:i:s",filemtime($filename));
?>
```

> __filemtime()__返回值为***UNIX***格式的时间戳,要用__date()__函数来格式化
