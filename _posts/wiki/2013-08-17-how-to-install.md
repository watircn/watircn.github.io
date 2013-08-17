---
layout: post
title: "环境部署"
description: "环境部署"
category: wiki 
tags: [wiki]
---
{% include JB/setup %}

本书的所有例子均在windows7下运行，windows xp,linux及mac下可能无暇测试。

安装ruby
---------------------

在windows上配置ruby开发环境其实非常简单。在有网络连接的情况下，你可以直接下载[rails installer](http://railsinstaller.org/)来进行安装。

就像安装普通的windows应用程序一样，直接下一步下一步就可以。

最后railsinstaller会要求我们配置git账户，此时会出现命令行界面，这个我们无需理会，关闭命令行就好。

安装webdriver
-------------

打开windows命令行，一般情况下按__win+R__键后输入__cmd__再按__回车__键就可以进入。

另外在windows7下，请确保你是以管理员身份打开命令行。

输入下面的命令

	gem install selenium-webdriver

你应该可以看到
--------------

	C:\Windows\system32>gem install selenium-webdriver
	Fetching: selenium-webdriver-2.32.1.gem (100%)
	Successfully installed selenium-webdriver-2.32.1
	1 gem installed
	Installing ri documentation for selenium-webdriver-2.32.1...
	Installing RDoc documentation for selenium-webdriver-2.32.1...

如果你得到的结果与我有所不同，别担心，使用下面的命令来测试一下webdriver有没有正确安装。

	gem list selenium

如果你得到下面的结果那就证明一切正常。注意你安装的webdriver版本号可能与下面的有差异，这是正常现象，不用担心。
	
	*** LOCAL GEMS ***

	selenium-webdriver (2.32.1)

如果你出现了问题，那么请从下面几点着手：

* railsinstaller是否正确安装了，安装时请用管理员身份去安装；
* 是不是敲错了命令，因为英文毕竟不是母语，敲错是常有的事情；
* 去网上搜索一下解决方案，或者找一些懂行的人进行求助；

安装IE driver
-------------
	gem install watir-webdriver

	
安装IE driver
-------------

在新版本的webdriver中，只有安装了ie driver使用ie进行测试工作。

ie driver的下载地址在[这里](https://code.google.com/p/selenium/downloads/list)，记得根据自己机器的操作系统版本来下载相应的driver。

下载好ie driver后，记得解压，然后把解压出来的文件放到系统的PATH里去。

一般来说，你可以把ie driver放在ruby/bin目录或者是jdk的bin目录中。


安装Chrome driver
-----------------

chrome driver的下载地址在[这里](https://code.google.com/p/chromedriver/downloads/list)。

安装方式与ie driver相同。

记得配置IE的保护模式
--------------------

如果要使用webdriver启动IE的话，那么就需要配置IE的保护模式了。

把IE里的保护模式都选上或都勾掉就可以了。


