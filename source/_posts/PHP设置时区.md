title: PHP设置时区
tags:
  - PHP
  - 程序生涯
date: 2012-08-22 10:58:03
---

主要解决国外主机显示时间与国内不一样的问题.

<pre class="brush: php; gutter: true">&lt;?php
    date_default_timezone_set(&#039;PRC&#039;);//此处PRC代表中国的北京时间
    echo date(&#039;Y-m-d H:i:s&#039;);
?&gt;</pre>

现在显示的就是北京时间了.