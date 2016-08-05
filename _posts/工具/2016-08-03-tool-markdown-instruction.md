---
layout: post
title: markdown基本教程
category: 工具
tags: markdown
comments: true
keywords:
description:
---
markdown语法主要包1括：**标题、段落，区块引用，代码区块，强调，列表，分割线，链接，图片，反斜杠\，特别符号**

## 1. 标题
两种形式：  
### 1.1 使用`=`和`-`标记一级和二级标题
> 一级标题
> `=========`   
> 二级标题
> `---------`

效果：
> 一级标题
> =========
> 二级标题
> ---------

### 1.2 使用`#`可表示1-6级标题
**注意** ： `#`与后面的标题之间须**存在一个空行**。
> \# 一级标题
> \## 二级标题
> \### 三级标题
> \#### 四级标题
> \##### 五级标题
> \###### 六级标题    
效果：
> # 一级标题
> ## 二级标题
> ### 三级标题
> #### 四级标题
> ##### 五级标题
> ###### 六级标题

## 2.段落
**段落的前后要有空行**，所谓的空行是指没有文字内容。若想在**段内强制换行**的方式是使用**两个以上空格加上回车**（引用中换行省略回车）。

## 3.区块引用
在段落的每行或者只在第一行使用符号`>`,还可使用多个嵌套引用，如：
> \> 区块引用
> \>> 嵌套引用

效果：
> 区块引用
>> 嵌套引用

## 4.代码区块
代码区块的建立是在每行加上4个空格或者一个制表符（如同写代码一样）。如    
普通段落：
void main()
{    
    printf("Hello, Markdown.");    
}    
代码区块：

    void main()
    {
        printf("Hello, Markdown.");
    }

或者

```java
	public ByteArrayInputStream(byte buf[]){
		this.buf = buf;
		this.pos = 0;
		this.count = buf.length;
	}
```

**注意**:需要和普通段落之间**存在空行**。

## 5.强调
在强调内容两侧分别加上`*`或者`_`，如：
> \*斜体\*，\_斜体\_
> \*\*粗体\*\*，\_\_粗体\_\_

效果：
> *斜体*，_斜体_
> **粗体**，__粗体__

## 6.列表
使用`·`、`+`、或`-`标记无序列表，如：
> \-（+\*） 第一项
> \-（+\*） 第二项
> \- （+\*）第三项

**注意**：标记后面最少有一个_空格_或_制表符_。若不在引用区块中，必须和前方段落之间存在空行。

效果：
> + 第一项
> + 第二项
> + 第三项

有序列表的标记方式是将上述的符号换成数字,并辅以`.`，如：
> 1 . 第一项
> 2 . 第二项
> 3 . 第三项

效果：
> 1. 第一项
> 2. 第二项
> 3. 第三项

## 7.分割线
分割线最常使用就是三个或以上`*`，还可以使用`-`和`_`。

## 8.链接
链接可以由两种形式生成：**行内式**和**参考式**。
**行内式**：
> \[younghz的Markdown库\]\(https:://github.com/younghz/Markdown "Markdown"\)。

效果：
> [younghz的Markdown库](https:://github.com/younghz/Markdown "Markdown")。

**参考式**：
> \[younghz的Markdown库1\]\[1\]
> \[younghz的Markdown库2\]\[2\]
> \[1\]:https:://github.com/younghz/Markdown "Markdown"
> \[2\]:https:://github.com/younghz/Markdown "Markdown"

效果：
> [younghz的Markdown库1][1]
> [younghz的Markdown库2][2]
[1]: https:://github.com/younghz/Markdown "Markdown"
[2]: https:://github.com/younghz/Markdown "Markdown"

**注意**：上述的`[1]:https:://github.com/younghz/Markdown "Markdown"`不出现在区块中。

## 9.图片
添加图片的形式和链接相似，只需在链接的基础上前方加一个`！`。

## 10.反斜杠`\`
相当于**反转义**作用。使符号成为普通符号。
## 11.符号`
起到标记作用。如：
>\`ctrl+a\`

效果：
>`ctrl+a`

## 12.表格


## 13.公式

$ \frac{1}{2} $

$$
\frac{-b\pm\sqrt{b^2-4ac}}{2a}
$$


## 感觉有意思？趁热打铁，推荐几个_工具_
+ **Chrome**下的stackedit插件可以离线使用，很爽。也不用担心平台受限。
在线的dillinger.io算是评价好的了，可是不能离线使用。   
+ **Windowns**下的MarkdownPad也用过，不过免费版的体验不是很好。
+ **Mac**下的Mou是国人贡献的，口碑很好。推荐。
+ **Linux**下的ReText不错。
