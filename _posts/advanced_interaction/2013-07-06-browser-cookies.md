---
layout: post
title: "浏览器Cookie"
description: "Cookie"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
Watir-WebDriver 0.5.2后提供了处理cookie的API,使用起来非常简单。

	require 'watir-webdriver'
	browser = Watir::Browser.new
	browser.cookies.clear
	browser.cookies.add 'foo', 'bar', :path => "/", :expires => 10.days.from_now, :secure => true
	browser.cookies.delete 'foo'
	browser.cookies.to_hash

