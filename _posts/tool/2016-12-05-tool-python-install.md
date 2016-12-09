---
layout: "post"
title: "win10下安装Python和Python版本切换"
date: "2016-10-26 12:31"
category: tool
tags: python,win10
comments: true
keywords:
description:
---

## 1.Python基本安装

python27win64安装：https://www.python.org/downloads/  安装中一路下一步即可

【配置python系统环境变量】

> 新建： PYTHON_HOME值为： C:\python27    
> Path 前面加上  %PYTHON_HOME%;%PYTHON_HOME%\Scripts


## 2.升级pip

python自带pip版本过久，需要升级安装：参考http://blog.sina.com.cn/s/blog_76cb58fb0102vfs0.html

【最新pip下载地址】https://pypi.python.org/pypi/pip

> (1) 下载那个.tar.gz压缩包，解压，在解压目录的当前文件夹下(f: 然后cd 路径)  打开DOS命令运行：python setup.py install    
> (2) 添加环境变量C:\Python27\Scripts(因为pip在该文件中，安装py27时已配置)    
> (3) 然后切换到包含当前whl文件的文件处用命令行打开，然后输入 pip install ×××.whl    
> (4) 卸载模块：pip uninstall PackageName    
> (5) 升级模块：pip install --upgrade 库名    
> (6) 列出所有安装库： pip list    
>      列出所有安装库(按照指定格式)：pip list --format=columns    
>  (7) 列出所有过期的库： pip list --outdated    
> 【pip升级自己】pip install --upgrade pip

## 3.安装whl库

【python各种库(whl格式)】下载地址：    
 	http://www.lfd.uci.edu/~gohlke/pythonlibs/    
	https://pypi.python.org/pypi?%3Aaction=index
网速慢，请自己下载whl.    
网速快，直接敲 pip install 库名  就行了(按照优先顺序)    
【python基础库】six  cycler pyparsing pytz setuptools dask decorator  networkx python_dateutil    
【矩阵库】numpy  patsy (在none中，先要安装numpy)    
【excel读写】xlrd xlwt    
【矩阵强化计算】scipy    
【画图工具】matplotlib    
【机器学习和nlp】scikit_learn PyYAML nltk    
【数据面板库】pandas    
【读图片】Pillow   scikit-image    
protobuf    
【最好办法】直接装anaconda,以上全部给装好了,记得下载python2.7的 地址 https://www.continuum.io/downloads#windows    
【但是最好办法一般不是最聪明的做法，因为这个anaconda体积太大了】    

【注意】python3用 pip3

【在window下只需要修改环境变量PYTHON_HOME的值即可】我写了个程序，直接程序以管理员身份运行即可随意切换版本(其实就是通过脚本来修改PYTHON_HOME的对应PYTHON路径值(如C:\Python27)

【注意】python除了numpy外，其他都可以通过pip install 库名去翻墙的互联网去下载并安装，但是numpy 请自己手动去http://www.lfd.uci.edu/~gohlke/pythonlibs下载(或者使用我下载好的cp27或cp35下的，因为发现64位python通过互联网下载的numpy安装不上，会报错)。然后进入下载的目录，执行：    
pip install numpy-1.11.2+mkl-cp27-cp27m-win_amd64.whl

### 4.安装jupyter

> pip install jupyter#安装notebook    
> pip install jupyterlab#安装lab    
> jupyter serverextension enable --py jupyterlab --sys-prefix    
> jupyter lab#启动lab    
> jupyter notebook#启动notebook    

### 4.Python2个版本切换工具

【工具下载地址】[PYTHON系统环境变量PYTHON_HOME脚本修改程序](http://download.csdn.net/download/zhulinniao/9702476)

【注意】两个版本要分别安装和升级pip，以及分别切换到各自下去安装依赖库

> [http://www.cnblogs.com/luckjun/p/4958338.html](http://www.cnblogs.com/luckjun/p/4958338.html)
