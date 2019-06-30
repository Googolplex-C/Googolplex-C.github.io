---
title: Combinatorics Exercise 017
date: 2019-02-24 12:53:33
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

对于正整数 $a_1$ , $a_2$ , $a_3$ , … , $a_n$（ $n \geq 4$），试证：存在整数 $x_1$ , $x_2$ , $x_3$ , … , $x_n$ ，满足 $x_i^2$ 等于 $0$ 或 $1$，且 $n^2\mid (a_1x_1+a_2x_2+\cdots +a_nx_n)$ .

<!-- more -->

#### *Proof*

构造一个 $n$ - 元组 $(y_i)^n_{i=1}$，使得 $y_i=1$ 或 $y_i=0$ . 于是这个 $n$ - 元组的可选取值数目为 $2^n$. 

定义 $f(y_1,y_2, \cdots, y_n) = a_1y_1+a_2y_2+\cdots +a_ny_n$，并考虑其模 $n^2$ 的余：因为当 $n \geq 4$ 时，$2^n \geq n^2$，我们进行如下讨论：

1. 若存在 $n$ - 元组 $y_1,y_2, \cdots, y_n$ 使得 $f(y_1,y_2, \cdots, y_n)$ 模 $n^2$ 成立：

   则令题目中的 $n$ - 元组 $(x_i)^n_{i=1} = (y_i)^n_{i=1}$，则命题自然成立；

2. 若不存在 $n$ - 元组 $y_1,y_2, \cdots, y_n$ 使得 $f(y_1,y_2, \cdots, y_n)$ 模 $n^2$ 成立：

   于是 $f$ 模 $n^2$ 的余数的可选数目为 $n^2-1 <2^n$，由抽屉原理可知，必定存在至少两个不同的 $n$ - 元组 $(y_i')^n_{i=1}$ 和 $(y_i^{''})^n_{i=1}$ ，使得 $f(y_1',y_2', \cdots, y_n')$ 和 $f(y_1^{''},y_2^{''}, \cdots, y_n^{''})$ 模 $n^2$ 同余.

   令 $(x_i)^n_{i=1} = (y_i')^n_{i=1}-(y_i^{''})^n_{i=1}$，可使欲证命题成立.

综合 1，2 可知，命题得证.

<p align="right">Q.E.D.</p>

#### Note

本问题可以认为是 [Combinatorics Exercise 016](https://googolplex-c.github.io/2019/02/23/Combinatorics-Exercise-016/) 的推广与变形，思路大致相同，只是对于条件 “ $x_i^2$ 等于 $0$ 或 $1$ ” 需要稍加留意，构造 $(y_i)^n_{i=1}$ 的时候取值范围应该缩窄，而不是套条件中的 $\{-1,0,1\}$.