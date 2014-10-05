title: "PHP 获取 文件大小,类型,创建/修改时间"
tags:
  - PHP
  - 程序生涯
date: 2012-08-22 23:00:59
---

<pre class="brush: php; gutter: true">int filesize(string $filename);//取得文件大小
string filetype(string $filename);//取得文件类型
int filemtime(string $filename);//取得文件修改时间</pre>

&nbsp;

获取文件大小:

<pre class="brush: php; gutter: true">&lt;?php
    $filename = &#039;test.txt&#039;;
    echo $filename.&#039;文件大小为: &#039;.filesize($filename).&#039; bytes&#039;;
?&gt;</pre>

&nbsp;

获取文件类型:

<pre class="brush: php; gutter: true">&lt;?php
    $filename = &#039;test.txt&#039;;
    echo filetype($filename);
?&gt;</pre>

filetype 有八种返回结果:

fifo,char,dir,block,link,file,unknown和false

常见返回结果主要是file和dir

&nbsp;

获取文件修改时间:

<pre class="brush: php; gutter: true">&lt;?php
    $filename = &quot;test.txt&quot;;
    echo &quot;$filename 修改日期为：&quot;,date(&quot;Y-m-d H:i:s&quot;,filemtime($filename));
?&gt;</pre>

filemtime返回值为UNIX格式的时间戳,要用date()函数来格式化

&nbsp;