---
layout: post
title: "所见即所得编辑器"
description: "富文本编辑器"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
有两种方法可以通过Watir-WebDriver向所见即所得编辑器(应该指的是富文本编辑器)中输入文字：

* 定位编辑器所在的iFrame，然后使用.send_keys方法(缺点是浏览器必须在前台运行)
* 在浏览器上执行javascript,通过js脚本去设置编辑器的值

## CKEditor

	require 'watir-webdriver'
	b = Watir::Browser.new :firefox
	b.goto 'http://ckeditor.com/demo'
	b.execute_script("CKEDITOR.instances['editor1'].setData('hello world');")
	b.frame(:title => 'Rich text editor, editor1, press ALT 0 for help.').send_keys 'hello world again'

## TinyMCE Editor

	require 'watir-webdriver'
	b = Watir::Browser.new
	b.goto 'http://tinymce.moxiecode.com/tryit/full.php'
	b.execute_script("tinyMCE.get('content').execCommand('mceSetContent',false, 'hello world' );")
	b.frame(:id => "content_ifr").send_keys 'hello world again'



