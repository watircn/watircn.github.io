---
layout: post
title: "截屏"
description: "截屏"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
Watir-WebDriver内建的截图功能很赞也很好用。

	browser.driver.save_screenshot 'screenshot.png'

The great thing about this is it gives you a screen shot of the entire page, not just above the fold.
截图功能最棒的地方在于它能捕获到整个页面，而不是屏幕上显示的那部分。

如果你正在使用Cucumber，那么你可以简单的将下面的代码添加到env.rb文件中，这样你可以在html的报告中插入截图：

	After do |scenario|
	  browser.driver.save_screenshot 'screenshot.png'
	  embed 'screenshot.png', 'image/png'
	end


