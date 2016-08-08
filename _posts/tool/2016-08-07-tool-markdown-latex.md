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

|      名称  	 |   大写显示  	 |   	 LaTex      |  小写显示      |   LaTex   |
|--------------|--------------|-------------|--------------|------------|
| alpha        | $A$   	   |   	 `$A$`       |   $\alpha$  | `$\alpha$`|
| beta          | $B$     |   `$B$`   	  |     $\beta$  | `$\beta$`  |
| gamma     | $\Gamma$ |`$\Gamma$`|$\gamma$  |`$\gamma$`|
| delta         | $\Delta$	 | 	`$\Delta$`	| 	$\delta$    | `$\delta$`|
| epsilon     | $E$	      | 	`$E$`	    | $\epsilon$   | `$\epsilon$`|
| zeta          | $Z$	       | 	`$Z$`	     | 	$\zeta$	      | 	`$\zeta$`	|
| eta           | $H$	       | 	`$H$`	     | 	$\eta$	      | 	`$\eta$`	|
| theta        | $\Theta$   | `$\Theta$`	  | 	$\theta$  | 	`$\theta$`	|
| iota          | $I$     	 | 	`$I$`	       | 	$\iota$	     | 	`$\iota$`	|
| kappa      | 	$K$     	 | 	`$K$`	      | 	$\kappa$  | 	`$\kappa$`	|
| lambda    |$\Lambda$ | `$\Lambda$`| $\lambda$  | 	`$\lambda$`	|
| mu          | 	$M$     	 | 	`$M$`	      | 	$\mu$	  | 	`$\mu$`	|
| nu           | 	$N$	          | 	`$N$`	    | 	$\nu$	     | 	`$\nu$`	|
| xi            | 	$\Xi$	    | 	`$\Xi$`	     | 	$\xi$	         | 	`$\xi$`	|
| omicron  | 	$O$     	  | 	`$O$`	   | $\omicron$  | 	`$\omicron$`	|
| pi            | 	$\Pi$      	   | 	`$\Pi$`	    | 	$\pi$	       | 	`$\pi$`	|
| rho         | 	$P$      	  | 	`$P$`	   | 	$\rho$     	| 	`$\rho$`	|
| sigma     | 	$\Sigma$   | `$\Sigma$` | 	$\sigma$	| 	`$\sigma$`	|
| tau         | 	$T$	          | 	`$T$`	   | 	$\tau$	      | 	`$\tau$`	|
| upsilon   |$\Upsilon$  | `$\Upsilon$`| 	$\upsilon$	| 	`$\upsilon$`	|
| phi         | 	$\Phi$     | 	`$\Phi$`	| 	$\phi$      	| 	`$\phi$`	|
| chi         | 	$X$	        | 	`$X$`	      | 	$\chi$      	| 	`$\chi$`	|
| psi         | 	$\Psi$	   | 	`$\Psi$`	| 	$\psi$	          | 	`$\psi$`	|
| omega  |$\Omega$ |	`$\Omega$`| 	$\omega$	| 	`$\omega$`	|

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
|上取整            |       `\lceil`、`\rceil`      |  $\lceil x \rceil$ | `$\lceil x \rceil$` |
|下取整            |     `\lfloor`、`\rfloor`   |$\lfloor x \rfloor$ | `$\lfloor x \rfloor$` |
|不可见括号      |                           `.`      |          -        |         -         |

【注意】因为大括号`{}`用来在上下标中用来分组,所以需要使用转义来显示

原始符号不会随着公式大小缩放，如`(\frac{1}{2})` ：$\frac{1}{2}$，采用`\left(…\right)`来自适应调整括号大小，即在`左边括号类型`加上`\left`，在`右边括号类型`加上`\right`

$$
\left \lbrace \sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6} \right\rbrace
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



## 4. 矩阵



## 5. 公式对齐



## 6. 分段函数



## 7. 连分数



## 8.方程组



## 9.公式颜色



## 10.公式序号标记



## 11. 公式排版建议



## 参考



> [1] [Mathjax与LaTex公式简介](http://mlworks.cn/posts/introduction-to-mathjax-and-latex-expression/)    
> [2] [Mathjax官网](https://www.mathjax.org/)    
