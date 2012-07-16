---
layout: page
title: "Questions"
description: ""
tagline: 
---
{% include JB/setup %}

Some questions to be solved

1. Rakefile 创建文件的时候文件名忽略中文

  解决方法：在 Rakefile 开头加上两行：

		require "jcode"
		$KCODE='utf8'

参考 <http://www.cnblogs.com/lizunicon/archive/2011/04/29/2032389.html> 

2. 在 jekyll 里面使用 javascript 和 jquery
