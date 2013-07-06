---
layout: post
title: "浏览器新窗口"
description: "浏览器新窗口"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
当一个新的浏览器窗口打开时，你可以使用'use'方法来处理这个新窗口。

	browser.window(:title => "annoying popup").use do
	  browser.button(:id => "close").click
	end

更多的例子请参考[这里](https://github.com/watir/watirspec/blob/master/window_switching_spec.rb)

