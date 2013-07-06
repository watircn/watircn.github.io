---
layout: post
title: "浏览器代理"
description: "浏览器代理"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
## 实例: 在Firefox中使用代理

	profile = Selenium::WebDriver::Firefox::Profile.new
	profile.proxy = Selenium::WebDriver::Proxy.new :http => 'my.proxy.com:8080', :ssl => 'my.proxy.com:8080'
	browser = Watir::Browser.new :chrome, :profile => profile

## 实例: 在Chrome中使用代理

	switches = '--proxy-server=my.proxy.com:8080'
	browser = Watir::Browser.new :chrome, :switches => switches


