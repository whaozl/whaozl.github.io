---
layout: "post"
title: "markdown完美支持latex"
date: "2016-08-07 12:31"
category: tool
tags: markdown
comments: true
keywords:
description:
---
本博客现在完美支持markdown下的latex公式

## 1.公式标记

### 1.1 行内公式

行内公式(inline)表示公式嵌入到文本段中，用`$...$`书写，**`$`的旁边不能有空格**。**以`\转义的如\alpha`等左右两边要留有空格**，否则无法比解析。

### 1.2 行间公式

行间公式表示公式独立成为一个段落，用`$$...$$`书写。

### 1.3 markdown中嵌入MathJax

在使用MathJax后，可以在渲染完成的公式上方右键点击，唤出右键菜单。在菜单中提供了查看公式的Latex源代码。

```javascript
<!--将该代码放入博客模板的head中即可-->
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
tex2jax: {
  inlineMath: [['$','$'], ['\\(','\\)']],
  processEscapes: true
  }
});
</script>
<!--latex数学显示公式-->
<script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
```

## 2. 常用基础Latex公式

### 2.1 希腊字母

| 中文名称 |      名称  	 |   大写显示  	 |   	 LaTex      |  小写显示      |   LaTex   |
|--------------|--------------|--------------|-------------|--------------|------------|
|   阿尔法    | alpha        | $A$   	   |   	 `$A$`       |   $\alpha$  | `$\alpha$`|
|   贝塔       | beta          | $B$     |   `$B$`   	  |     $\beta$  | `$\beta$`  |
|   伽马       | gamma     | $\Gamma$ |`$\Gamma$`|$\gamma$  |`$\gamma$`|
|   德尔塔    | delta         | $\Delta$	 | 	`$\Delta$`	| 	$\delta$    | `$\delta$`|
|   伊普西隆 | epsilon     | $E$	      | 	`$E$`	    | $\epsilon$   | `$\epsilon$`|
|   泽塔        | zeta          | $Z$	       | 	`$Z$`	     | 	$\zeta$	      | 	`$\zeta$`	|
|   伊塔        | eta           | $H$	       | 	`$H$`	     | 	$\eta$	      | 	`$\eta$`	|
|   西塔       | theta        | $\Theta$   | `$\Theta$`	  | 	$\theta$  | 	`$\theta$`	|
|   约塔       | iota          | $I$     	 | 	`$I$`	       | 	$\iota$	     | 	`$\iota$`	|
|   卡帕       | kappa      | 	$K$     	 | 	`$K$`	      | 	$\kappa$  | 	`$\kappa$`	|
|   兰姆达    | lambda    |$\Lambda$ | `$\Lambda$`| $\lambda$  | 	`$\lambda$`	|
|   缪           | mu          | 	$M$     	 | 	`$M$`	      | 	$\mu$	  | 	`$\mu$`	|
|   纽           | nu           | 	$N$	          | 	`$N$`	    | 	$\nu$	     | 	`$\nu$`	|
|   克西       | xi            | 	$\Xi$	    | 	`$\Xi$`	     | 	$\xi$	         | 	`$\xi$`	|
|   欧米克隆| omicron  | 	$O$     	  | 	`$O$`	   | $\omicron$  | 	`$\omicron$`	|
|   派           | pi            | 	$\Pi$      	   | 	`$\Pi$`	    | 	$\pi$	       | 	`$\pi$`	|
|   柔           | rho         | 	$P$      	  | 	`$P$`	   | 	$\rho$     	| 	`$\rho$`	|
|   西格玛    | sigma     | 	$\Sigma$   | `$\Sigma$` | 	$\sigma$	| 	`$\sigma$`	|
|   陶           | tau         | 	$T$	          | 	`$T$`	   | 	$\tau$	      | 	`$\tau$`	|
|   宇普西隆| upsilon   |$\Upsilon$  | `$\Upsilon$`| 	$\upsilon$	| 	`$\upsilon$`	|
|   弗爱       | phi         | 	$\Phi$     | 	`$\Phi$`	| 	$\phi$      	| 	`$\phi$`	|
|   卡           | chi         | 	$X$	        | 	`$X$`	      | 	$\chi$      	| 	`$\chi$`	|
|   普赛       | psi         | 	$\Psi$	   | 	`$\Psi$`	| 	$\psi$	          | 	`$\psi$`	|


### 2.2 上标和下标

 |      显示        |    	LaTex    |
 |--------------|------------|
 |   $x_i^2$     |   `$x_i^2$` |
 | $10^{10}$   |  `$10^{10}$`|
 | ${x^5}^6$ |  `${x^5}^6$`|


### 2.3 括号

|   	名称         |            表示方法         |       显示          |    	LaTex      |
|---------------|------------------------|----------------|----------------|
|小括号和方括号|  使用原始的(),[]即可   |$(2+3)[4+4]$   |`$(2+3)[4+4]$`|
|大括号   |`\{`、`\}` 或 `\lbrace`、`\rbrace` |   $\{a*b\}$   |`$\{a*b\}$`|
|尖括号            |   `\langle` 、 `\rangle`   | $\langle x \rangle$ | `$\langle x \rangle$` |
|单侧括号     |  左边用. 右边用括号 |  $\left. \right\}$ | `$\left. \right\}$` |
|上取整            |       `\lceil`、`\rceil`      |  $\lceil x \rceil$ | `$\lceil x \rceil$` |
|下取整            |     `\lfloor`、`\rfloor`   |$\lfloor x \rfloor$ | `$\lfloor x \rfloor$` |
|不可见括号      |                           `.`      |          -        |         -         |

【注意】因为大括号`{}`用来在上下标中用来分组,所以需要使用转义来显示

原始符号不会随着公式大小缩放，如`(\frac{1}{2})` ：$\frac{1}{2}$，采用`\left(…\right)`来自适应调整括号大小，即在`左边括号类型`加上`\left`，在`右边括号类型`加上`\right`

$$
\left \lbrace \sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6} \right \rbrace
$$


### 2.4 求和、积分、分式、根式

|   	名称         |            表示方法         |       显示              |    	   LaTex         |
|---------------|------------------------|--------------------|-------------------|
|       求和         |            `\sum`            |    $\sum_1^n$    |   `$\sum_1^n$`    |
|       累乘         |            `\prod`            |    $\prod_1^n$    |   `$\prod_1^n$`    |
|       积分         |            `\int`            |    $\int_1^\infty$    |   `$\int_1^\infty$`    |
|   二重积分      |            `\iint`            |    $\iint_1^\infty$    |   `$\iint_1^\infty$`    |
|       并集         |            `\cup`            |    $A \cup B$    |   `$A\cupB$`    |
|       交集         |            `\cap`            |    $A \cap B$    |   `$A\capB$`    |
|      简单分式   |             `\frac`                |    $\frac{a+1}{b+1}$  |  `$\frac{a+1}{b+1}$` |
|      特殊分式   |             `\over`                |   $a+1 \over b+1 $  | `$a+1 \over b+1 $` |
|     根式          |              `\sqrt`               |     $\sqrt[4]{\frac {x}{y}}$ | `$\sqrt[4]{\frac {x}{y}}$`|

### 2.5 公式内部的空格

在公式中直接敲空格来给公式腾出空间是无效的，另外，**`$`的旁边不能有空格**。如a…b与a…….b（假设.这里表示成空格）都会显示为ab，`a \: bc`：$a \: bc$，`a \quad bc`：$a \quad bc$， `a \qquad bc`：$a \qquad bc$。即`\qquad`空间 > `\quad`空间 > `\:`空间

### 2.6 顶部符号

|   	名称         |      显示              |    	   LaTex         |
|---------------|---------------------|---------------|
| 单字符           | $\hat x$          |  `$\hat x$`  |
| 多字符           | $\widehat xy$ |  `$\widehat xy$` |
| 其他              | $\overline {xyz} \quad \vec  a \quad \overrightarrow {x} \quad \dot x \quad \ddot x$  | `\overline {xyz} \quad \vec  a `<br>`\overrightarrow {x} \quad \dot x \quad \ddot x` |

### 2.7 特殊函数与符号

|   	名称         |      显示              |    	   LaTex        |
|----------------|------------------|-----------------|
| 常见的三角函数  | $\sin x$、$\arctan x$      | `$\sin x$、$\arctan x$` |
| 求极限                | $\lim_{1\to\infty}$          | `$\lim_{1\to\infty}$`      |
| 比较运算符         |$\lt \gt \le \ge \neq \not\lt$     | `\lt \gt \le \ge \neq \not\lt` |
| 操作运算符         | $\times \div \pm \mp x \cdot y$   | `\times \div \pm \mp  x \cdot y`  |
| 省略号                | $a_1+a_2+\cdots+a_n$，$a_1, a_2, \ldots ,a_n$ | `$a_1+a_2+\cdots+a_n$，$a_1, a_2, \ldots ,a_n$`|
| 集合关系与运算  | $\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing$ | `\cup \cap \setminus \subset \subseteq \subsetneq`<br>`\supset \in \notin \emptyset \varnothing`  |
| 排列符号            | ${n+1 \choose 2k}{\binom{n+1}{2k}}$ | `${n+1 \choose 2k}{\binom{n+1}{2k}}$` |
| 箭头                   | $\to \rightarrow \leftarrow \Rightarrow \Leftarrow \mapsto$ | `\to \rightarrow \leftarrow`<br>`\Rightarrow \Leftarrow \mapsto` |
| 逻辑运算符        | $\land \lor \lnot \forall \exists \top \bot \vdash \vDash$ | `\land \lor \lnot \forall`<br>`\exists \top \bot \vdash \vDash` |
| 模运算               | $a\equiv b\pmod n$ | `a\equiv b\pmod n` |
| 等式符号            | $\approx \sim \cong \equiv \prec$ | `\approx \sim \cong \equiv \prec` |
| 点符号               | $\star \ast \oplus \circ \bullet$ | `\star \ast \oplus \circ \bullet` |
|数学特殊符号      | $\infty  \aleph_0 \nabla \partial Im \Re$ | `\infty \aleph_0  \nabla \partial \Im \Re` |
| 常见希腊字母变体形式 | $\epsilon \varepsilon \phi \varphi$ | `\epsilon \varepsilon \phi \varphi` |

## 3. 表格

【书写方式】<code>$$\begin{array}{列样式}  表格内容   \end{array}$$</code>    
【列样式】<code>{c|clr}</code>——共指定4列(第1列和第2列间有一条竖线)，clr分别表示居中center、靠左left、靠右right    
【表格行列间隔】各行使用`\\`分隔，各列使用 `&` 分隔    
【公式中注释】`%`后面紧跟着注释    
【公式常文本】`\text{文本内容}`  其中的文本内容 不会随着公式字体倾斜
【表格水平线和垂直线】垂直线在列样式中用`|`间隔，水平线在行中 用`\hline`指定

```
$$
%指定4列，第1列水平居中，第1列和第2列间垂直线，第2、3、4列分别左靠齐、居中、右靠齐
\begin{array}{c|lcr}
n & \text{Left} & \text{Center} & \text{Right} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i \\
\end{array}
$$
```

效果：

$$
%指定4列，第1列水平居中，第1列和第2列间垂直线，第2、3、4列分别左靠齐、居中、右靠齐
\begin{array}{c|lcr}
n & \text{Left} & \text{Center} & \text{Right} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i \\
\end{array}
$$

## 4. 矩阵

### 4.1 矩阵基本用法

【书写方式】<code>$$\begin{matrix}   矩阵内容   \end{matrix}$$</code>     
【矩阵行列间隔】各行使用`\\`分隔，各列使用 `&` 分隔    

```
$$
        \begin{matrix}
        1 & x & x^2 \\
        1 & y & y^2 \\
        1 & z & z^2 \\
        \end{matrix}
$$
```

效果：    

$$
        \begin{matrix}
        1 & x & x^2 \\
        1 & y & y^2 \\
        1 & z & z^2 \\
        \end{matrix}
$$

### 4.2 矩阵加括号

【书写方式1】采用2.3中做法——使用`\left与\right`配合表示括号符号     
【书写方式2】使用特殊的matrix

|      名称          |   	符号         |      显示              |    	   LaTex        |
|----------------|------------------|-----------------|-----------------|
|   小括号矩阵   |     pmatrix      |    $\begin{pmatrix} 1 & 2 \\ 3 & 4 \\ \end{pmatrix}$        | `\begin{pmatrix}1&2\\3&4\\ \end{pmatrix}` |
|   中括号矩阵   |     bmatrix      |    $\begin{bmatrix} 1 & 2 \\ 3 & 4 \\ \end{bmatrix}$        | `\begin{bmatrix}1&2\\3&4\\ \end{bmatrix}` |
|  大括号矩阵    |     Bmatrix      |    $\begin{Bmatrix} 1 & 2 \\ 3 & 4 \\ \end{Bmatrix}$        | `\begin{Bmatrix}1&2\\3&4\\ \end{Bmatrix}` |
|    行列式        |     vmatrix      |    $\begin{vmatrix} 1 & 2 \\ 3 & 4 \\ \end{vmatrix}$        | `\begin{vmatrix}1&2\\3&4\\ \end{vmatrix}` |
|   矩阵的模     |     Vmatrix      |    $\begin{Vmatrix} 1 & 2 \\ 3 & 4 \\ \end{Vmatrix}$        | `\begin{Vmatrix}1&2\\3&4\\ \end{Vmatrix}` |

### 4.3 矩阵的省略元素

【书写方式】`\cdots` $\cdots$ 、`\ddots` $\ddots$、`\vdots` $\vdots$

$$
\begin{pmatrix}
     1 & a_1 & a_1^2 & \cdots & a_1^n \\
     1 & a_2 & a_2^2 & \cdots & a_2^n \\
     \vdots  & \vdots& \vdots & \ddots & \vdots \\
     1 & a_m & a_m^2 & \cdots & a_m^n    
\end{pmatrix}
$$

### 4.4 增广矩阵

【书写方式】增广矩阵需要使用前面的array来实现

```
$$ \left[
      \begin{array}{cc|c}
        1&2&3\\
        4&5&6
      \end{array}
    \right]
$$
```
结果：

$$ \left[
      \begin{array}{cc|c}
        1&2&3\\
        4&5&6
      \end{array}
    \right]
$$

## 5. 公式对齐

【书写方式】<code>\begin{align}…\end{align}</code>，再使用`&`来指定每行需要对齐的位置

```
$$
\begin{align}
	\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
	& \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}
$$
```

效果：

$$
\begin{align}
	\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
	& \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}
$$

## 6. 分段函数

【书写方式】<code>\begin{cases}…\end{cases}</code>    
【分类和对齐位置】使用\\来分类，使用&指示需要对齐的位置

```
$$
 f(n) =
\begin{cases}
	n/2,  & \text{if $n$ is even} \\
	3n+1, & \text{if $n$ is odd}  \\
\end{cases}
\\%简单的换行
\left.%这个.必须写,这是反括号
\begin{array}{l}
\text{if $n$ is even:}& n/2\\
\text{if $n$ is odd:} & 3n+1
\end{array}
\right\}
=f(n)
$$
```

效果：

$$
 f(n) =
\begin{cases}
	n/2,  & \text{if $n$ is even} \\
	3n+1, & \text{if $n$ is odd}  \\
\end{cases}
\\%简单的换行
\left.%这个.必须写,这是反括号
\begin{array}{l}
\text{if $n$ is even:}& n/2\\
\text{if $n$ is odd:} & 3n+1
\end{array}
\right\}
=f(n)
$$

## 7.公式序号标记

【标记公式书写方式】`\tag{yourtag}`     
【引用上面公式方式】加上`\label{yourlabel}`在`\tag`之后——这个MathJax支持但是Atom的markdown插件markdown-preview-plus暂时不支持

$$
 a := x^2-y^3 \tag{1}\label{1}
$$

为引用公式，可以使用<code>\eqref{rlabel}</code>

$$
	a+y^3 \stackrel{\eqref{1}}= x^2
$$

## 8.公式颜色

【书写方式】`\color{#000}{文本内容}
公式颜色采用RGB表示，这是我最喜欢的    
`\verb+即时显示的文本内容+` 用于在公式中即时显示内容，与`\text{文本内容}`类似

|      名称          |   	符号         |      显示              |    	   LaTex        |
|----------------|------------------|-----------------|-----------------|
|   黑色		|     \verb+#000+      |    $\color{#000}{text}$  | `\color{#000}{text}` |
|   蓝色		|     \verb+#00F+      |    $\color{#00F}{text}$  | `\color{#00F}{text}` |
|   绿色		|     \verb+#0F0+      |    $\color{#0F0}{text}$  | `\color{#0F0}{text}` |
|   红色		|     \verb+#F00+      |    $\color{#F00}{text}$  | `\color{#F00}{text}` |
|   黄色		|     \verb+#FF0+      |    $\color{#FF0}{text}$  | `\color{#FF0}{text}` |
|	紫红色	  |     \verb+#F0F+      |    $\color{#F0F}{text}$  | `\color{#F0F}{text}` |

[w3school颜色参考](http://www.w3school.com.cn/tags/html_ref_colornames.asp)

## 公式排版建议

### 01 不要在再指数或者积分中使用`\frac`

在指数、积分表达式中使用`\frac`会使表达式看起来不清晰，在排版中很少被使用。应使用一个水平的/来代替

$$
\begin{array}{cc}
	\mathrm{不建议使用} & \mathrm{建议使用} \\
	\hline \\
	e^{i\frac{\pi}2} \quad e^{\frac{i\pi}2}& e^{i\pi/2} \\
	\int_{-\frac\pi2}^\frac\pi2 \sin x\,dx & \int_{-\pi/2}^{\pi/2}\sin x\,dx \\
\end{array}
$$

### 02 使用 `\mid` 代替 `|` 作为分隔符

符号`|`作为分隔符时存在排版空间大小的问题

$$
\begin{array}{cc}
	\mathrm{不建议使用} & \mathrm{建议使用} \\
	\hline \\
	\{x|x^2\in\Bbb Z\} & \{x\mid x^2\in\Bbb Z\} \\
\end{array}
$$

### 03 多重积分

对于多重积分，不要使用\int\int此类的表达，应该使用`\iint \iiint`等特殊形式    
同时，在微分前应该使用`\,`来增加些许空间，否则$\TeX$会将微分紧凑地排列在一起

$$
\begin{array}{cc}
	\mathrm{不建议使用} & \mathrm{建议使用} \\
	\hline \\
	\int\int_S f(x)\,dy\,dx & \iint_S f(x)\,dy\,dx \\
	\int\int\int_V f(x)\,dz\,dy\,dx & \iiint_V f(x)\,dz\,dy\,dx \\
	\iiint_V f(x)dz dy dx & \iiint_V f(x)\,dz\,dy\,dx
\end{array}
$$

### 04 连分数

书写连分数表达式时，使用`\cfrac`代替`\frac或者\over`

$$
x = a_0 + \cfrac{1^2}{a_1
          + \cfrac{2^2}{a_2
          + \cfrac{3^2}{a_3 + \cfrac{4^4}{a_4 + \cdots}}}} \tag{\cfrac}
$$
$$
x = a_0 + \frac{1^2}{a_1
          + \frac{2^2}{a_2
          + \frac{3^2}{a_3 + \frac{4^4}{a_4 + \cdots}}}} \tag{\frac}
$$

### 05 方程组

使用<code>\begin{array} ... \end{array}</code>与<code>\left\{ …\right.</code>配合，表示方程组，或者使用<code>\begin{cases}…\end{cases}</code>

$$
\left\{
	\begin{array}{c}
		a_1x+b_1y+c_1z=d_1 \\
		a_2x+b_2y+c_2z=d_2 \\
		a_3x+b_3y+c_3z=d_3
	\end{array}
\right.
\\
\begin{cases}
	a_1x+b_1y+c_1z=d_1 \\
	a_2x+b_2y+c_2z=d_2 \\
	a_3x+b_3y+c_3z=d_3
\end{cases}
$$

对齐方程组中的`=`，使用<code>\being{align} .. \end{align}</code>

$$
\left\{
	\begin{align}
		a_1x+b_1y+c_1z &=d_1+e_1 \\
		a_2x+b_2y &=d_2 \\
		a_3x+b_3y+c_3z &=d_3
	\end{align}
\right.
$$

对齐方程组中的`=`、和项，使用<code>\being{array}{列样式} .. \end{array}</code>

$$
\left\{
	\begin{array}{ll}
		a_1x+b_1y+c_1z &=d_1+e_1 \\
		a_2x+b_2y &=d_2 \\
		a_3x+b_3y+c_3z &=d_3
	\end{array}
\right.
$$

## 参考

> [1] [Mathjax与LaTex公式简介](http://mlworks.cn/posts/introduction-to-mathjax-and-latex-expression/)    
> [2] [Mathjax官网](https://www.mathjax.org/)    
> [3] [markdown语法之如何使用LaTeX语法编写数学公式](http://blog.csdn.net/lanxuezaipiao/article/details/44341645#math)    
> [4] [mathjax-basic-tutorial-and-quick-reference](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)
