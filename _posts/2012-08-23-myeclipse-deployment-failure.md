---
layout: post
title: "Myeclipse deployment failure"
description: ""
category: "others"
tags: []
---
{% include JB/setup %}

在使用Myeclipse 和 tomcat 的时候经常出现 "deployment failure on tomcat ... could not copy all resources to ... " 的错误。 
在我的环境中，这种情况经常出现在新建 project 然后把其他的project添加进来的时候出错。这个错误一般是由于project中有其他的jar，这个时候需要重新添加一下这些jar库。具体操作 "configure build path" 重新添加jar库
