---
title: Pigeonhole Principle Exercise 039
date: 2019-08-13 16:01:14
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

给定 $n$ 个素数，将它们任意相乘（每个素数可以出现任意次）已构造 $n+1$ 个正整数，试证：这 $n+1$ 个正整数中必定可以抽出若干个数，这些数的乘积是完全平方数。

#### *Proof*

不妨记这 $n$ 个素数为

$$
p_1,p_2,\cdots, p_n
$$

于是由它们构造的 $n+1$ 个正整数中的任意一个可以写成

$$
p_{1}^{k_1}p_{2}^{k_2}\cdots p_{n}^{k_n} \qquad k_{i}^{} \in \mathbb{N}
$$

的形式。

因为素因子 $p_i$ 是固定的，因此有序序列 $k_1k_2\dots k_n$ 就可以唯一地确定一个积；并且这个积是完全平方数，当且仅当 $k_i$ 全是偶数。

注意到序列 $k_1k_2\dots k_n$ 的奇偶排布的数目为 $2^n$（也就是长为 $n$ 的 0-1序列的数目），而我们从 $n+1$ 个正整数中抽取若干个数的方式数目为 $2^{n+1}-1 > 2^n$，从而我们可以由抽屉原理得知，这 $n+1$ 个整数的集合存在两个子集，记这两个子集中整数的各自的**乘积**分别为

$$
p_{1}^{k'_1}p_{2}^{k'_2}\cdots p_{n}^{k'_n} \qquad k_{i}^{'} \in \mathbb{N}
$$

和

$$
p_{1}^{k_{1}^{''}}p_{2}^{k_{2}^{''}}\cdots p_{n}^{k_{n}^{''}} \qquad k_{i}^{''} \in \mathbb{N}
$$

并满足

$$
\forall i \in [n], \ k_{i}^{'} \equiv k_{i}^{''} \mod 2
$$

于是，自然地，我们有

$$
\forall i \in [n], \ (k_{i}^{'} + k_{i}^{''}) \equiv 0 \mod 2
$$

也即是说，这两个子集共同的乘积

$$
p_{1}^{k_{1}^{'}+k_{1}^{''}}p_{2}^{k_{2}^{'}+k_{2}^{''}}\cdots p_{n}^{k_{n}^{'}+k_{n}^{''}}
$$

是完全平方数，命题得证。

<p align="right">Q.E.D.</p>

