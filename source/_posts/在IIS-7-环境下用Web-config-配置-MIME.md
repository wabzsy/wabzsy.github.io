image: "http://blog-for-wabzsy.qiniudn.com/images"
date: 2012-08-22 10:27:51
title: 在IIS 7 环境下用Web.config 配置 
description: " "
categories: "技术日志"
tags:
  - 服务器配置
  - IIS
  - Web.config
---

> 最新刚买了个Godaddy的主机,

> 服务器用的是IIS7,管理后台不能自己添加MIME所以就想到了用Web.config来配置,

> IIS7是支持Web.config的(不要误以为之后ASP.NET(.aspx)的程序才会用到Web.config)

> 下面是设置代码:

``` xml
<configuration>

    <system.webServer>

        <staticContent>
            <mimeMap fileExtension=".vbox-extpack" mimeType="application/octet-stream" />
     </staticContent>

    </system.webServer>

</configuration>
```

> 其中fileExtension是文件的扩展名,mimeType是文件的类型.
