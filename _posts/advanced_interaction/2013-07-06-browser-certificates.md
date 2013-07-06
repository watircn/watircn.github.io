---
layout: post
title: "证书"
description: "浏览器证书"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
## Firefox

默认情况下，Firefox driver自己会正确的处理不信任的证书。

如有你拥有一个信任的证书，但是仍然提示其他的一些证书错误，比如hostname不匹配(也就是说在测试时使用正式环境的证书)，那么你需要做下面的事情：

	profile = Selenium::WebDriver::Firefox::Profile.new
	profile.assume_untrusted_certificate_issuer = false
	b = Watir::Browser.new :firefox, :profile => profile
	The reason this is needed is explained here.

## Chrome

Chrome上只需要在实例化Browser时传入相应的开关(switch)就可以忽略无效证书了：

	Watir::Browser.new :chrome, :switches => ['--ignore-certificate-errors']


