---
layout: "post"
title: "git的图形化工具Tortoise"
date: "2016-08-09 14:47"
category: tool
tags: [markdown,git]
comments: true
keywords:
description:
---

1、首先，安装Git_V2.5.1_64_bit_setup.1441791170.exe    

2、然后，安装TortoiseGit-1.8.15.0-64bit.msi    

3、自己可安装TortoiseGit-1.8.15.0-32bit.64bit中文语言包.zip    

4、在github上，锁定一个httpurl――是github某项目本身中间有一个    

   ZIP HTTP Git Read-Only后面就是跟着url地址(Read Access)(为提高下载速度,可将https换成http)    

   在自己任何一个文件夹中，右键选择Git Clone，填写刚才那个url地址，然后就下载了。    


【git使用】

01、重定位新链接    
	假设git克隆库目录：whaozl    
        进入其目录，空白处右键，选择 Git Bash Here    
        敲入如下命令：    
         git remote set-url origin https://10.10.40.244/whaozl.git    
	http://10.10.40.244/whaozl.git为您的url新地址    

02、git记住推送账号和密码(Git Bash运行该命令，推送只要输入一次账号和密码即可)    
	git config credential.helper store    

03、执行Git命令时出现各种 SSL certificate problem 的解决办法    
	方法1：执行命令window下：set GIT_SSL_NO_VERIFY=true git clone    
			linux下：env GIT_SSL_NO_VERIFY=true git push    
	方法2：git config --global http.sslVerify false    
