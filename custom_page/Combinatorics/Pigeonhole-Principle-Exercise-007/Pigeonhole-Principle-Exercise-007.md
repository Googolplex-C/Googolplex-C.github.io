---
title: Pigeonhole Principle Exercise 007
date: 2019-02-01 21:34:39
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

任意选取 $5$ 个正整数，能否保证其中任意 $3$ 个数之和都为素数？

<!-- more -->

#### *Solution*

不能. 

设这 $5$ 个数模 $3$ 的简化剩余系为 $\{R_0,R_1,R_2\}$ ，针对 “$R_0$, $R_1$, $R_2$ 是否同时非空” 进行讨论：

1. 同时非空  
    则三个剩余类中各选一个数，其和刚好满足 $(0+1+2)\mod 3 = 0$ . 
2. 不全非空  
    也即：至多只有两个剩余类非空.  
    于是由抽屉原理可知，在某个剩余类中，存在至少三个数，而由浅显的初等数论知识可知，这三个模 $3$ 同余的数之和亦是 $3​$ 的倍数.  

于是，无论如何，存在三个数，使得其和能被 $3$ 整除；另外，由于原来的五个数是正的，因此，这个构造得到的和必不为 $0​$，从而其为合数. 命题得证. 

<p align="right">Q.E.D.</p>

