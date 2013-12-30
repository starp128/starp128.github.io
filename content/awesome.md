title:awesome使用总结
date:2013-12-08
tags:linux
status:hidden

##introduction
官方的介绍：
>[awesome](http://awesome.naquadah.org "http://awesome.naquadah.org")is highly configurable,next generation framework window manager for X.it is very fast,extensible and licensed under the GNU GPLv2 licence.

***
###自动运行
awful.util.spawn_with_shell("google-chrome")

###查找窗口的类型
	xprop
光标变为"+"时选中窗口，这时就会看到WM_CLASS 和WM_NAME
这时在rule中加入
	-- Set Google-chrome to always map on tags number 3 of screen 1.
	{ rule = { class = "Google-chrome" },
	properties = { tag = tags[1][3] } },
在任何时候人一个tag中打开google都会出现在第三个tag上

***
参考[awesome wiki http://awesome.naquadah.org/wiki/Main_page
