---
layout: post
title: "在命令提示符显示Git Branch提示"
description: ""
category: "Git"
tags: []
---
{% include JB/setup %}

当一个项目里的 git branch 比较多的时候，下面的代码可以在命令提示符中显示当前工作的 branch 的名字。

	function parse_git_branch () {
		git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
	}
    PS1="${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[0;33m\]\$(parse_git_branch)\[\033[00m\]\$ "

将上面的代码添加到 ` ~/.bashrc ` 或 ` ~/.profile ` 中 ，主要在 PS1 的值中添加 ` $(parse_git_branch) ` ， 结果如：
` payne@debian:~/git_repository/payneseu.github.com (master)$ `


参考： [Show the Current GIT Branch in Your Command Prompt](http://www.developerzen.com/2011/01/10/show-the-current-git-branch-in-your-command-prompt/)

	
