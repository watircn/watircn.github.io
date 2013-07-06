---
layout: post
title: "基本的浏览器认证"
description: "基本的浏览器认证"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
最简单最优雅的处理基本的浏览器验证([basic browser authentication](http://en.wikipedia.org/wiki/Basic_access_authentication))的方法是在url中加入用户名和密码，以绕开验证对话框。

	require 'watir-webdriver'
	b = Watir::Browser.start 'http://admin:password@yourwebsite.com'

