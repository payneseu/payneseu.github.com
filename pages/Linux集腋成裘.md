---
layout: page
title: "Linux集腋成裘"
description: ""
group: navigation
---
{% include JB/setup %}

这个 page 记录了Linux的点点滴滴。以便日后整理

1. 在 debian 中，脚本运行出现错误 "can't shift many" ，应该是 /bin/sh 的指向 dash 的错误，可以在 dpkg-reconfig dash 设置为指向 bash

2. 一个命令完成压缩 `tar cvf - aaa/ | gzip -qc > aaa.tar.gz` 打包压缩 `aaa/` 或者，`tar -c dir/ | bzip2 > dir.tar.bz2` 在 bash 总的 `-` 例如： `vim -` ， `tar cvf - aaa` ， `gzip -`

3. `$_` bash 中的特殊参数， 保存前一个执行命令的最后一个参数。例如：`mkdir aaa/bbb/ccc && cp xx.c $_`

4. linux 查找命令  `apropos`  等同于 `man -k`
