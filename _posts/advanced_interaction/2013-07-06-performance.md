---
layout: post
title: "页面性能"
description: "页面性能"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}

[Watir-WebDriver-Performance gem](http://rubygems.org/gems/watir-webdriver-performance) 提供在访问页面的同时进行页面性能度量的功能，其使用的是[W3C页面性能度量指标](http://w3c-test.org/webperf/specs/NavigationTiming/)。这是一个完美的捕获响应性能指标的解决方案，其使用方法非常直观和简单，不过目前只支持Chrome和IE9l浏览器。

	require 'watir-webdriver'
	require 'watir-webdriver-performance'
	 
	b = Watir::Browser.new :chrome
	 
	10.times do
	  b.goto 'http://17test.info'
	  load_secs = b.performance.summary[:response_time]/1000
	  puts "Load Time: #{load_secs} seconds."
	end 

其统计结果如下：

	Load Time: 3.701 seconds.
	Load Time: 0.694 seconds.
	Load Time: 1.874 seconds.
	Load Time: 1.721 seconds.
	Load Time: 2.096 seconds.
	Load Time: 0.823 seconds.
	Load Time: 2.362 seconds.
	Load Time: 1.008 seconds.
	Load Time: 1.761 seconds.
	Load Time: 2.066 seconds.

支持的性能指标：

* :summary
* :navigation
* :memory
* :timing

