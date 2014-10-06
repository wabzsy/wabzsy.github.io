image: "http://blog-for-wabzsy.qiniudn.com/images"
date: 2012-08-22 16:00:27
title: ASP.NET的MD5加密方式
description: " "
categories: "技术日志"
tags:
  - ASP.NET
  - C#
  - md5加密
---

添加命名空间:

``` csharp
using System.Security.Cryptography;
using System.Text;
```

自己写了个方法:

``` csharp
public class Safe
{
    public static string Md5(string str)
    {
        try
        {
            byte[] hashvalue = (new MD5CryptoServiceProvider()).ComputeHash(Encoding.UTF8.GetBytes(str));
            return BitConverter.ToString(hashvalue);
        }
        catch
        {
            return String.Empty;
        }
    }
}
```

然后调用时使用:

``` csharp
string password = Safe.Md5(&quot;Your Password&quot;);
```
就可以实现Md5加密了..

ASP.NET(C#)的md5比较特殊,是47位:00-11-22-33-44-55-66-77-88-99-AA-BB-CC-DD-EE-FF这种形式的,

所以在数据库里添加字段时不要建成常规的32位,要不然会出现&#8221;将截断字符串或二进制数据&#8221;这种错误.
