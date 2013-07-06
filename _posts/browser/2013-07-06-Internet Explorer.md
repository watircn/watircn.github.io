---
layout: post
title: "Internet Explorer"
description: "IE浏览器"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
Windows上的IE

Internet Explorer只支持Windows操作系统(靠！)，并且只有当你将所有区域的__保护模式__设置成一致时(也就是说保护模式全部是"开启"或"关闭")才能正常运行。

	b = Watir::Browser.new :ie
	Internet Explorer Config

Watir-WebDriver 使用你标准的浏览器配置，所以你可以在运行测试前手动更改这些设置。



