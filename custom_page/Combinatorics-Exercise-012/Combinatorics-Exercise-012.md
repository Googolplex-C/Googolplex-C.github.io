---
title: Combinatorics Exercise 012
date: 2019-02-14 22:10:30
author: Googolplex-C
img: 
top: 
cover: 
coverImg: 
password: 
toc: 
mathjax: 
summary: 
categories: 
tags:

export_on_save:
  html: true
html:
  embed_local_images: false
  embed_svg: true
  offline: false
  toc: true
---

#### Title

设 $x$ 是无理数，试证：存在某个不大于 $n-1$ 的正整数 $p$ ，使得 $px$ 与离其最近的整数的距离小于 $\frac{1}{n}$.

<!-- more -->

#### *Proof*

将区间 $(0,1)$ 划分如下：
$$
(0,\frac{1}{n}),\ (\frac{1}{n},\frac{2}{n}),\ \cdots,\ (\frac{n-1}{n},1)
$$
并考虑如下 $n-1$ 个乘积：$x$ , $2x$ , $3x$ , …… , $(n-1)x$（注意到 $x$ 是无理数，因而 $x$ 与整数相乘之积也是无理数）：

1. 若存在某个数 $p \in [n-1]$，使得乘积 $px$ 的小数部分位于 $(0,\frac{1}{n})$ 或者 $(\frac{n-1}{n},1)$ 中，则显然 $p$ 是使得命题成立的正整数；

2. 若 case 1 不成立：  
   则 $n-1$ 个乘积都将各自分布在于 $(\frac{1}{n},\frac{2}{n}),\ \cdots,\ (\frac{n-2}{n},\frac{n-1}{n})$ 这 $n-2$ 个区间中，由抽屉原理可知，存在至少两个不同的正整数，记作 $i$ , $j$ ，使得 $ix$ 和$jx$ 位于同一个区间中，那么有
   $$
   \lvert ix-jx \rvert = \lvert(i-j)x \rvert < \frac1n
   $$
   令正整数 $p=\lvert i-j \rvert$ ，则命题得证.

综上所述，命题成立.

<p align="right">Q.E.D.</p>

#### Note

1. 当时在做这个问题的时候，陷入了定势，卡了很久，后来用 $\pi$ 带入 $x$ 作为例子之后，很快解决此问题（因为只需算多几个数就马上发现思路）——特殊值带入举例的方法有时候真的有助于抓住问题的实质，理清并指明做题的方向，依稀记得 Tao 也在他的博客中说过类似的体会；
2. 该问题在许多初等数论的教材中会作为丢番图逼近的基础内容出现，实际上，本问题所述命题也是一个初等数论中的结论，并且由此出发好像可以引出许多更为深刻的内容，若条件允许，笔者以后也许会继续往下学习.