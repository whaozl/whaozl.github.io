---
layout: "post"
title: "atom的插件"
date: "2016-08-08 19:28"
category: tool
tags: markdown
comments: true
keywords:
description:
---

## 1.markdown相关插件

### 1.1 markdown-preview-plus

atom内置了markdown-preview插件，这个插件不支持latex显示，因此将其禁用掉(File-Settings)，在Setting->Install中在线搜索插件markdown-preview-plus，将其安装。然后打开一个markdown格式文件(md或markdown)

> 预览——然后点击菜单Package->markdown-preview-plus->toggle-preview(ctr+shift+M)
> latex显示——上一步下的toggle-render-latex(ctr+shift+X)

### 1.2 markdown-scroll-sync

但使用1.1中的插件后，点击md的源文件不会实时滚动预览窗口，安装这个就支持啦

### 1.3 tool-bar-markdown-writer

安装这个插件可以让markdown一些创建脚本和加粗、插入表格的功能显示在**atom的工具栏上方**，这个插件安装之前首先需要安装markdown-writer插件和tool-bar插件。


## 2. git相关插件

要安装git相关插件，首先需要安装github的桌面客户端。可以到这里下载[github3桌面客户端](http://download.csdn.net/detail/zhulinniao/9598402)，官网下载特别慢。

### 2.1 git-plus

安装这个插件之后，直接ctr+shift+p 输入命令 git-plus-commit提交报错，这时需要在git-plus插件的属性下配置git.exe(安装的github桌面端)的位置。

安装的github桌面端在登陆自己账户之后，git.exe位置在C:/Users/aool/AppData/Local/GitHub/PortableGit_c2ba306e536fdf878271f7fe636a147ff37326ad/bin/git.exe下。然后设置这个路径即可(注意：`路径是/`)。

再使用atom的导航 右键 Add Project Folder ——> clone下的github项目(注意：最要用TortoiseGit可以正常提交一次，让其记住用户名和密码)，对该项目进行编辑，进行git正常的提交就行了。

### 2.2 tree-view-git-status

这个插件可以让Atom 的 右边 github项目的 导航栏 显示 文件的git状态

## 3. atom相关插件

### 3.1 pretty-json

json的格式化插件

### 3.2 minimap

可以和subline text一样 在编辑窗口的右边显示的迷你的代码形状

### 3.3 minimap-find-and-replace

可以在编辑窗口的右边的迷你代码形状中 显示 find的 查找的白色点位置

### 3.4 tool-bar

atom必须安装的工具栏插件

### 3.5 flex-tool-bar

将上面的所有功能说对应的插件模块对应自定义配置到工具栏中

当安装好这个插件后，会看到工具栏上显示一个 配置 的图标，点击它会进入 toolbar.cson 文件，以下是我配置的内容。其中icon的查找地址在[github图标官网](https://octicons.github.com)


```json
# This file is used by Flex Tool Bar to create buttons on your Tool Bar.
# For more information how to use this package and create your own buttons,
#   read the documentation on https://atom.io/packages/flex-tool-bar
# callback中 命令callback之间空格替换成-，并且冒号左右不能有空格
[
  {
    type: "button"
    icon: "gear"
    callback: "flex-tool-bar:edit-config-file"
    tooltip: "Edit Tool Bar"
  }
  {
    type: "spacer"
  }
	{
	  type: "button"
	  icon: "markdown"
	  callback: "markdown-preview-plus:toggle"
	  tooltip: "markdown-preview-plus:toggle"
	}
	{
	 type: "button"
	 icon: "mention"
	 callback: "markdown-preview-plus:toggle-render-latex"
	 tooltip: "markdown-preview-plus:toggle-render-latex"
	}
  {
    type: "spacer"
  }
	{
	 type: "button"
	 icon: "git-commit"
	 callback: "git-plus:add-all-commit-and-push"
	 tooltip: "git-plus:add-all-commit-and-push"
	}
	{
	 type: "button"
	 icon: "repo-push"
	 callback: "git-plus:push"
	 tooltip: "git-plus:push"
	}
	{
	 type: "button"
	 icon: "repo-pull"
	 callback: "git-plus:pull"
	 tooltip: "git-plus:pull"
	}
  {
    type: "spacer"
  }
	]
```

### 3.6 sync-settings

该插件可以与github上同步所有的插件。下次重装atom后只需要github的token和github的gist服务id,可以同步Atom的设置文件,自定义快捷键,用户风格,初始化脚本及代码片段,还支持已安装的插件同步.

> (1) 打开自己的github创建一个[a new person access token](https://github.com/settings/tokens/new),复制生成的token序列,粘贴到sync-settings插件的setting里面,如果已经有了之前backup的token，打开原来的token，点击Regenerate Token即可。    
> (2) [再打开github的gist服务](https://gist.github.com/whaozl/155cdb802224eaf2aa5314eb3b71931e)，创建一个gist，并复制生成gist id（注意这个id就是你创建的gist服务对应的URL中除去你的用户名，之后的部分，一串abcd之类），也粘贴到sync-settings插件的setting里面    
> (3) 配置完毕后，你可以在菜单栏中的Packages下看得到。

## 4. 其他插件

### 4.1 atom-html-preview

html预览插件，默认快捷键：CTRL-SHIFT-H

![2016-08-08-tool-atom-plugin](/assets/tool/2016-08-08-tool-atom-plugin.png)

###### 图1 安装之后的效果图

> [markdown插件官网](https://atom.io/packages)    
> [Github开源编辑器Atom常用插件及安装方法](http://blog.csdn.net/mduanfire/article/details/50278591)
