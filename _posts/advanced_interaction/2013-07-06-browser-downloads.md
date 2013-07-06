---
layout: post
title: "文件的下载"
description: "文件的下载"
category: watir-webdriver
tags: [watir-webdriver]
---
{% include JB/setup %}
最简单最好的处理文件下载对话框的方式就是完全的避免对话框弹出。

可以在代码里告诉浏览器自动的将文件下载到指定目录，然后在测试用例中访问该目录进行验证。

## Firefox

	download_directory = "#{Dir.pwd}/downloads"
	download_directory.gsub!("/", "\\") if Selenium::WebDriver::Platform.windows?
	 
	profile = Selenium::WebDriver::Firefox::Profile.new
	profile['browser.download.folderList'] = 2 # custom location
	profile['browser.download.dir'] = download_directory
	profile['browser.helperApps.neverAsk.saveToDisk'] = "text/csv,application/pdf"
	 
	b = Watir::Browser.new :firefox, :profile => profile

关于Firefox的所有配置项可以通过在地址栏中输入'about:config'进行查看。

If you want to know a way to work out the file types (eg. application/pdf) then you can read the following blog post for an step by step guide.
如果你想知道如何处理特定类型的文件，请阅读[这篇](http://watirmelon.com/2011/09/07/determining-file-mime-types-to-autosave-using-firefox-watir-webdriver/)博文。

## Chrome

	download_directory = "#{Dir.pwd}/downloads"
	download_directory.gsub!("/", "\\") if  Selenium::WebDriver::Platform.windows?
	 
	profile = Selenium::WebDriver::Chrome::Profile.new
	profile['download.prompt_for_download'] = false
	profile['download.default_directory'] = download_directory
	 
	b = Watir::Browser.new :chrome, :profile => profile


