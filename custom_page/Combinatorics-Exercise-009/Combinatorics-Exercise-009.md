---
title: Combinatorics Exercise 009
date: 2019-02-02 17:20:07
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

某次会议有 $n$ 名代表出席，已知：任意四名代表中都有一人与其余的三个人握过手，试证：任意四名代表中，都有一人与其他 $n-1$ 名代表握过手. 

<!-- more -->

#### *Proof*

约定在这 $n​$ 名代表中，任选 $4​$ 名代表组成的集合称为 *quad-team*，且若某人在其所处的任意一个 *quad-team* 中与其他三人都握过手，那么称他为该 *quad-team* 中的 *p-person*.

注意到以下事实：

1. 握手是一种双向关系，即若 $A$ 和 $B$ 握手，亦即意为着 $B$ 和 $A$ 握手；
2. 在同一 *quad-team* 中，若某两个人之间没有握过手，则根据定义，此二人都不可能是该 *quad-team* 的 *p-person*

在 $n$ 名代表中任选一个 *quad-team* ，记为 $T=\{A,B,C,D\}$ ，进行讨论如下：

1. 若 $T$ 中存在两名代表，他们之间没有握过手：

    不失其一般性，假设这两位代表为 $B$ 和 $C$，根据 *p-person* 的定义，$B$ 和 $C$ 都不是 *p-person*. 那么，不妨假设 $A$ 是 $T$ 中的 *p-person*.  
    进而，在除了 $T$ 之外的 $n-4$ 名代表中，任意选取一名新代表 $E$ ，并考虑其与 $A$ , $B$ , $C$ 组成的新的 *quad-team* ，记为 $T'$，此时由题意可知，$A$ 或者 $E$ 中至少有一位是 *p-person*：

    1. 若 $A$ 是 *p-person*，则 $A$ 和 $E$ 握过手；
    2. 若 $E$ 是 *p-person*，则 $A$ 和 $E$ 握过手；

    于是，无论如何  $A$ 和 $E$ 一定握过手——注意 $E$ 是在集合 $T$ 之外**任意选取**的一名代表，所以照此推断，我们可以得知 $A$ 与集合 $T$ 之外的任何一人都握过手，同时 $A$ 又是 *quad-team* 的 *p-person*，所以 $A$ 与除自己外的所有 $n-1$ 人都握过手. 

2. 若 $T$ 中任意两位代表之间都握过手：
    
    于是 $T$ 中 $A$ , $B$ , $C$ , $D$ 都是该 *quad-team* 的 *p-person*.   
    不失一般性，考虑一下代表 $D$ （这里选谁都没问题，最多只是换个名字而已），若 $D$ 与除 $T$ 外的所有人都握过手，那么 $D$ 显然就与其他 $n-1$ 个人握过手；  
    若存在某个不属于 $T$ 的代表，不妨记作 $F$ ，他与 $D$ 没有握过手，于是我们构造一个新的 *quad-team* ，记作 $T^{''} = \{A,B,D,F\}$，此时就回到了 case 1 的情形——我们可以对 $T^{''}$ 直接套用 case 1 的推断过程得出结论，$A$ 与除自己外的所有 $n-1$ 人都握过手.

综合以上讨论，在 $T$ 中，总能找到一个与除自己外所有人都握过手的人，而 $T$ 本身是任意选取的，因此命题得证. 

<p align="right">Q.E.D.</p>