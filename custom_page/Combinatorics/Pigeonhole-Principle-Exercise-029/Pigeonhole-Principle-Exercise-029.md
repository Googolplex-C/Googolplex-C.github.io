---
title: Pigeonhole Principle Exercise 029
date: 2019-04-08 12:10:24
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
任意 $2n$ （$n >1$）个人聚在一起，其中任何一个人至少与其他 $n$ 个人相互认识，试证：一定能找到四个人，当他们围坐在一张桌子旁时，每人恰与他两边的人相认识.

<!-- more -->
#### *Proof*
假设任意两人之间都认识，那么命题自然成立.

若存在两个相互不认识的人，记其为甲和乙，他们每人至少各认识 $n$ 个人，而除甲乙二人之外还剩 $2n-2$ 个人，于是由抽屉原理和容斥原理可知，至少存在两个人，不妨记为丙和丁，他们中的任何一位都同时认识甲和乙，于是他们按照 “甲-丙-乙-丁-（甲）” 的顺序围坐，可以使得命题得证.

<p align="right">Q.E.D.</p>
