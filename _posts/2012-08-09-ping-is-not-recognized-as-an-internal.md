---
layout: post
title: "ping is not recognized as an internal.."
description: ""
category: "other"
tags: []
---
{% include JB/setup %}

在Win7 系统中，可能是上次装JDK的时候，把系统的环境变量改变了，使用ping命令的时候出现错误 "ping is not recognized as an internal or externa" , 但是使用绝对路径 "C:\Windows\System32\ping.exe" 的时候是好的，搜索找到是环境变量 %PATH% 的设置有问题，在 PATH 的值前面加上 `%SystemRoot%\system32;%SystemRoot%;` 就可以解决。  
参考: <http://blog.sina.com.cn/s/blog_631361ac0100klsv.html>
