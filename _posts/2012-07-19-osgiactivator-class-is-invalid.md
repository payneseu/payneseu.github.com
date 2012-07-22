---
layout: post
title: "OSGI:Activator class is invalid"
description: ""
category: "java"
tags: []
---
{% include JB/setup %}

最近在做 OSGI 的时候，在一个测试的例子中，在别人的环境下好用，但是在自己的环境下，加载 Bundle 的时候就是出现异常，提示说 ”Activator class is invalid“ ，但是 ` MANIFEST.MF ` 的配置都是一样的。那么只能是 run Configure 配置有问题，在 Google 搜索下。终于找到了解决办法
> Hey folks: Here is My solution to the problem (I am developing Bundles for Eclipse Equinox(the OSGi implementation)) :
>
>AND THE SOLUTION is V-E-R-Y simple -> just add -dev bin to your Program Arguments under (Run->Run Configurations->”Your_Loader”->Tab “Arguments”)
>
>Cheer

参考：<http://blog.chris-alex-thomas.com/2007/07/17/eclipse-activator-class-is-invalid/>
