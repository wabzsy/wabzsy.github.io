image: "http://blog-for-wabzsy.qiniudn.com/images"
date: 2012-08-22 10:58:03
title: PHP设置时区
description: " "
categories: "技术日志"
tags:
  - PHP
---

> 主要解决国外主机显示时间与国内不一样的问题.

``` php
<?
    date_default_timezone_set('PRC'); //此处PRC代表中国的北京时间
    echo date('Y-m-d H:i:s');
?>
```
> 现在显示的就是北京时间了.
