---
title: Discussion on difference of two powers
date: 2019-09-13 23:03:03
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

Before we get started, I have to say this is the first article written in English. I used to feel proud of my English skill for getting fairly good scores in exam. And the fact is, examinations in middle school can only reflect a limited part of the learner's skill, and after all these years I became no one but an ignoramus. 

Shame on myself.

However, the best thing out of the worst was that I started to realize in these days how arrogant and naive I was, and I don't take it as an option to give up. As a language, English is charming, also quite very useful. How could I just drop it and act like having never been an English learner?!

To some extent, that's why I decided not to write this arcticle in Chinese. It is thought to be the crucial key in language learning to seize every oppotunity of practise, and be exposed to English-speaking environment. Since I found it not very easy in China to exposed myself to such environment, writing could be a complementary way.

What's more, I hope my thoughts can be recorded and conveyed in another way. That might be cool.

---

##### Statement 
In elementary algebra and some other cases in mathematics, a formula might show up very frequently, stated as follows:

Difference of two squares
:    $$x^2-y^2=(x-y)(x+y)$$

<p align="right">□</p>

It is named as " 平方差公式 " in Chinese. Actually, it can be generalized to a more complicated form below.

Difference of two powers
:    $$
    x^n-y^n=(x-y)(x_{}^{n-1}+x_{}^{n-2}y+\cdots+xy_{}^{n-2}+y_{}^{n-1}) \qquad \qquad n \in \mathbb{N}^+
    $$

<p align="right">□</p>

It's called " $n$ 次方差公式 " in Chinese. Here $x$ and $y$ belong to some field $K$. 

Polynomial $x_{}^{n-1}+x_{}^{n-2}y+\cdots+xy_{}^{n-2}+y_{}^{n-1}$ in the RHS resembles binomial expansion in combinatorics. However, binomial coefficients don't ever appear.

Now we are going to make a agreement. In this article, "*dp*-$2$ formula" is used for reference to the first formula, and "*dp*-$n$ formula" for the latter one. 

Let $n$ be a positive odd integer. And if we substitude $-k$ for $y$, a new formula will be derived from *dp*-$n$ directly:

$$
x^n+k^n=(x+k)(x^{n-1}-x^{n-2}k+ \cdots - xk^{n-2} + k^{n-1})
$$

Since the notation in formula doesn't really matter, we can also rewrite it as follows.

Sum of two powers
:   $$x^n+y^n=(x+y)(x^{n-1}-x^{n-2}y+ \cdots - xy^{n-2} + y^{n-1}) \qquad \qquad n=2k+1,\ k \in \mathbb{N}$$

<p align="right">□</p>

Formula of sum of two powers differs mainly in signs of terms, compared with the origin *dp*-$n$. We have $x+y$ instead of $x-y$ as a factor in the RHS, and signs of all terms in the second factor shift alternatively between $+1$ and $-1$.

Notice that symmetry is reflected within this equation. Supposed we interchange $x$ and $y$, then the LHS turns into $y^n+x^n$, which makes no difference at all. Thus, the RHS should remain unchanged with $x$ and $y$ interchanged. To be specific, a pair of mirrored terms $x^{n-1-i}y^i$ and $x^iy^{n-1-i}$ is supposed to possess the same sign.

##### Proof
Proof of the formula is not difficult actually, yet some middle students would regard it as an extraordinary skill. But that's just because this formula does not appear as a theorem explicitly in their textbook. 

Various versions of proof are given below.

###### Version 1

The simplest way to prove formula *dp*-$n$ is to directly compute and simplify its RHS with algebraic method. 


$$
\begin{aligned}
\mathrm{RHS}&=(x-y)\sum_{i=0}^{n-1}x_{}^{i}y_{}^{n-1-i} \\
&= x\sum_{i=0}^{n-1}x_{}^{i}y_{}^{n-1-i} - y\sum_{i=0}^{n-1}x_{}^{i}y_{}^{n-1-i} \\
&= x^n + \sum_{i=1}^{n-1}x^iy^{n-i} - (y^n + \sum_{i=1}^{n-1}x^iy^{n-i})\\
&=x^n-y^n \\
\end{aligned}
$$

<p align="right">Q.E.D.</p>

###### Version 2

1. Supposing $y=0$

    Formula *dp*-$n$ is obviously satisfied.

2. Supposing $y \neq 0$

    We have $x^n-y^n = y^n((\frac{x}{y})^n -1)$.

    According to the conclusion on Sum of Geometric Progression $\sum_{i=0}^{n-1}x^i  = \frac{x^n-1}{x-1}$, we have 

    $$
    \begin{aligned}
    (\frac{x}{y})^n -1 &= (\frac{x}{y}-1)\sum_{i=0}^{n-1}(\frac{x}{y})^i \\
    &= (\frac{x}{y}-1)((\frac{x}{y})^{n-1} + (\frac{x}{y})^{n-2} + \cdots + (\frac{x}{y})^1 + 1) \\
    &= (\frac{x-y}{y})((\frac{x}{y})^{n-1} + (\frac{x}{y})^{n-2} + \cdots + (\frac{x}{y})^1 + 1) \\
    \therefore x^n-y^n &= (x-y)(x_{}^{n-1}+x_{}^{n-2}y+\cdots+xy_{}^{n-2}+y_{}^{n-1}) \\
    \end{aligned}
    $$
    
That's all.
<p align="right">Q.E.D.</p>

###### Version 3: Combinatorial Proof
I love Combinatorial proofs! It is thought to be a most intuitive way to understand one theorem or statement. Anyway, there is a trade-off between intuition and generality. And in this Combinatorial version proof, $x$ and $y$ are restricted within the scope of $\mathbb{N}^+$. 

Suppose that we have got $n$ balls arranging in a line. Each one should be painted with exactly one of the $x$ types of color, among which we choose $y$ types as "bad" colors. Thus, the other $(x-y)$ types of color are treated as "good" colors. Our task is to calculate the amounts of ways to get all $n$ balls painted with at least one ball painted with good color. 

Remember the essence of Combinatorial proof: to count a set of objects using different ways. Since the amount of infinite set always remain unchanged, we are able to prove that these two different counting method involved was actully equvalent.

According to the famous Principle of Substraction in Combinatorial, we know that the amount of ways to get each ball painted and at least one painted with good color can be given by the formula below:

$$
x^n-y^n
$$

Consider it from another perspective. Since at least one ball should be painted with good color, we are always able to find the FIRST ball painted with one of the $x-y$ types of good colors. For convinence, we call this ball "header".

The location of header does matter. If header is located the $i$ th ball, ways of painting balls before it sum up to $y^{i-1}$, which can only be painted with one of the $b$ types of bad. Such restriction no more go into effect for all those balls lying behind the header, thus ways of getting them painted sum up to $x^{n-i}$. According to Principle of Multiplication, we've got $x^{n-i}y^{i-1}$ ways to color all balls but the header.

Note that any one of these $n$ balls could be the header. That is to say, variable $i$ traverses from $1$ to $n$. From Principle of Addition we know the total ways of coloring all the other balls except header add up to

$$
\sum_{i=1}^{n}x_{}^{n-i}y_{}^{i-1} = \sum_{i=0}^{n-1}x_{}^{i}y_{}^{n-1-i}
$$

Finally from Principle of Multiplication we know that 

$$
x^n-y^n= (x-y)\sum_{i=0}^{n-1}x_{}^{i}y_{}^{n-1-i}
$$

<p align="right">Q.E.D.</p>







