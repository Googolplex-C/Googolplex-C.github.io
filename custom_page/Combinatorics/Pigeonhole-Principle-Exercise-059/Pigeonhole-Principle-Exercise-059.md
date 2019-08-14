---
title: Pigeonhole Principle Exercise 059
date: 2019-08-14 15:11:02
author: Googolplex-C
url: 
img: 
top: 
cover: 
coverImg: 
password: 
toc: 
mathjax: 
summary: <!--TODO-->
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
设等差数列 $a_1$, $a_2$, $\dots$, $a_p$ 的各项都与 $p$ 互素，试证：等差数列的公差 $d$ 不与 $p$ 互素。

#### *Proof*

由题设以及互素的定义可知道，$a_1$, $a_2$, $\dots$, $a_p$ 模 $p$ 的余都不为零，于是这 $p$ 项在模 $p$ 意义下的余数的取值范围为 $[p-1]$ 共 $p-1$ 个数。

应用抽屉原理可知，存在两项 $a_i$, $a_j$，其中 $1 \leq i < j \leq p$, 使得 $(a_j-a_i) \equiv 0 \mod p$, 也即是

$$
(j-i)d \equiv 0 \mod p
$$

注意，$0 < (j-i) < p$，所以若假设 $p$ 和 $d$ 互素，那么就会推出 $(j-i) \equiv 0 \mod p$ 的结论，显然矛盾。

因此假设不成立，命题得证。

<p align="right">Q.E.D.</p>

#### Corollary

本问题的逆否命题叙述如下：

**若一个等差序列的公差 $d$ 和 某一正整数 $p$ 互素，那么这个等差数列的前 $p$ 项必定遍历模 $p$ 意义下的完全剩余系。**

这在涉及到整除概念或者初等数论相关的问题中，是一个经常用到的、使用频率很高的结论！

