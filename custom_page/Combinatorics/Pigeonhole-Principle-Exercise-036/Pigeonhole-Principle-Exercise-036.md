---
title: Pigeonhole Principle Exercise 036
date: 2019-08-13 14:49:21
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

试证：任意 $52$ 个整数中，必定可以找到两个数，它们的和或者差能被 $100$ 整除。

#### *Proof*

考虑模 $100$ 的简单剩余系 $[100]$，将其进行如下分划：

$$
\{0\}, \{1,99\}, \{2, 98\}, \dots, \{49,51\},\{50\}
$$

共 $51$ 个等价类，由于我们有 $52$ 个整数，因此由抽屉原理可知，必定存在 $2$ 个整数，它们同属于一个等价类中，于是它们的和或者差必定有一者能被 $100$ 整除。

<p align="right">Q.E.D.</p>
