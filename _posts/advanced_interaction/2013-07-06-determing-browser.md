---
layout: post
title: "是哪种浏览器呢"
description: "是哪种浏览器呢"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
你可能会想在代码里控制使用哪种浏览器进行测试，这是很简单的：

	require 'watir-webdriver'
	b = Watir::Browser.new :chrome
	browser.driver.browser #=> :chrome

