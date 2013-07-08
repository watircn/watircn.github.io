---
layout: post
title: "主页"
description: "主页"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}

Watir WebDriver
---------------
欢迎莅临Watir WebDriver官方中文主页。Watir WebDriver：最优雅的WebDriver ruby实现。

Watir (音同 Water: 是的，我知道这会使人困惑)是Web Application Testing in Ruby这几个英文单词的首字母缩写， 另外WebDriver part stands 当然是代表WebDriver了。

Watir-WebDriver支持哪些浏览器?
==============================
几乎所有的浏览器: 比如Firefox, Chrome 和 IE，Safari现在也支持了。

Watir-WebDriver好用吗?
======================
我可以说Watir-WebDriver好评如潮，这个工具确实很优秀。

快速开始
========
	gem install watir-webdriveror

或者直接将watir-webdriver 添加到你的gemfile文件如果你使用bundler的话 (如果你没有使用bundler，那么我建议你立刻试用)。

Watir-WebDriver 是基于ruby 1.9.3的, 但是其也兼容更老的ruby版本。

那么继续
========
准备好了，那么打开irb。irb是Ruby的解释器，可以逐行解释ruby语句。那么在irb中逐行敲入下面的代码吧，看看接下来会发生什么神奇的事情:

```ruby
	require 'watir-webdriver'
	b = Watir::Browser.new
	b.goto 'bit.ly/watir-webdriver-demo'
	b.text_field(:id => 'entry_0').set 'your name'
	b.select_list(:id => 'entry_1').select 'Ruby'
	b.select_list(:id => 'entry_1').selected? 'Ruby'
	b.div(:class => 'ss-form-entry').button.click
	b.text.include? 'Thank you'
```
看，是不是很简单。你已经不错了，喝杯茶犒劳自己一下吧。

天哪，竟然没有Xpath选择符!
==========================
你可能留意到一件事情，那就是没有出现xpath选择符。其实Watir-WebDriver是支持xpath和css选择符的。你会发现api是很有点麻烦的，让你感到你不需要使用它。当然在特定的情况下，这些选择符还是很有用的。

天哪，竟然不支持录制和回放
==========================
自动化脚本录制工具（比如Selenium IDE）是给傻瓜用的。严肃的说，在irb中解释执行Watir-WebDriver代码比使用那些傻乎乎的录制工具要高效和实用的多。再加上你亲手编写的代码要比录制工具自动生成的代码有更好的可读性和稳定性，想像一下，如果你代码里有自动生成的长达100个字符的css选择符，这样好吗，你懂的。

Ruby的魅力
==========
Ruby是一门很神奇很有趣的语言。每天你都会有新的发现，你对ruby的爱也会与日俱增。相信我， Watir-WebDriver也是如此神奇的。

