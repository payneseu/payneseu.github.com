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

5. linux tcp/ip 命令 netcat

6. htop 类似于 top

7. 命令 cut & paste


8. 禁止访问 某个ip 的端口。 iptables
	iptables -A OUTPUT  -d 10.94.xx.xx  -p tcp --dport 33133 -j REJECt
	iptables -F 清除所有规则
	iptables -L 列出所有规

	多个端口 -m --dports
	反转匹配 !

9. 查看开启的端口
	netstats -tulp
	nmap

10. 获取 ipv4 地址 
	
	ip addr show eth0 | awk '/inet / {FS = "/"; $0 = $2; print $1}'

11. 删除结尾换行回车符

	tr -d '\n'


