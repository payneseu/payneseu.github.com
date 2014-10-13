---
layout: post
title: "pkg config and glib"
description: ""
category: "others"
tags: []
---
{% include JB/setup %}

pkg-config and glib circular denpendency

when configure pkg-config, it says error

	checking if internal glib should be used... no
	checking for pkg-config... no
	checking for GLIB... no
	configure: error: Either a previously installed pkg-config or "glib-2.0 >= 2.16" could not be found. Please set GLIB_CFLAGS and GLIB_LIBS to the correct values or pass --with-internal-glib to configure to use the bundled copy.

<https://mail.gnome.org/archives/gtk-devel-list/2011-September/msg00215.html>
<http://dossy.org/2008/03/pkgconfig-and-glib-chicken-and-egg-same-thing/>

