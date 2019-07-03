---
title: Pigeonhole Principle Exercise 008
date: 2019-02-01 22:13:59
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

某地区网球俱乐部的 $20$ 名成员举行 $14$ 场单打比赛，每人至少上场一次. 试证：必有六场比赛，其 $12$ 个参赛者互不相同. 

<!-- more -->

#### *Proof*

注意到两个事实：

1. 每个人都和其他人不相同，且不考虑平行宇宙或者克隆技术；
2. 一个人不可能与自己对战；

于是，若在若干场比赛中，出现了相同的参赛者，则必定是**某个成员多次参赛**所致. 

由题意可知，$14$ 场比赛共有 $28$ 个参赛席位，且 $20$ 名成员每人至少参赛一次.  
不妨将每个参赛者第一次参赛的场次席位 “染” 上白色，其余席次染上黑色，于是恰有 $20$ 个席次为白色，剩下的 $8$ 个席次为黑色. 

而这 $8$ 个黑色席次最多只能出现在 $8$ 场比赛中. 那么，至少存在 $6$ 场比赛，其 $12$ 个席次都是白色的，即：参加这六场比赛的全部 $12$ 名选手都是第一次出场，从而这 $12$ 名参赛者必定互不相同. 命题得证. 

<p align="right">Q.E.D.</p>

