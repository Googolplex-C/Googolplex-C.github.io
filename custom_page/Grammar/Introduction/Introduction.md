---
title: 英语语法导论
date: 2019-08-04 18 06 04
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

# 什么是语法

## 语言的概念

语言
:    用于交际的，音、 形、义结合的语法和词汇的体系。



## 语言的体系构成

如下图所示，语言的三大框架的是：
- 语义系统
- 结构系统
- 发音/文字系统

```viz{align=center}
graph G{
	graph[rankdir=LR, compound=true]
	
	h[label=语言]

	subgraph H{
		d[label=语义系统]
		e[label=结构系统]
		f[label="发音/文字系统"]

		d -- e
		e -- f	
	}

	subgraph F{
		
		a[label=词汇]
		b[label=语法]
		c[label="语音/文字"]

		a -- b
		b -- c
	}

	
	empty[style=invis]
	empty -- h[style=invis]
	
	edge[constraint=false]
	h -- d
	h -- e
	h -- f
	
	d -- a
	e -- b
	f -- c
}
```

1. 语义系统的具体表现是词汇，它赋予语言以**意义内容**

2. 结构系统的具体表现是语法，它赋予语言以**结构形式**

3. 发音/文字系统的具体表现是语音和文字，它赋予语言以**物质外壳**

其中，语法扮演着一个很重要的角色，在书写时，它是词汇和文字的枢纽；在说话时，它是词汇和语音的枢纽。

## 语法的分类

### 客观世界的语法和语言学家眼中的语法
1. 不可否认，语法是客观存在的。也就是在客观世界中，存在着一套语言的规则，我们称之为客观世界中的语法，如果违背了这套规则，那么多多少少会导致一些交流上的问题

2. 语言学家所说的语法，就是**对客观世界的语法的描述和总结**

这两者在外延上并不完全相等：

1. 首先，人的认识总是有限的

2. 其次，语言本身也是在不断变化中的

可以借助**物理世界规律**和**物理学**的关系理解上面两个概念的关系。

### 理论语法和教学语法
语法学者所研究总结的语法当中，又可以继续进行分类

- 理论语法：系统的语言学理论，不直接为教学服务

- 教学语法：直接服务于教学，内容上来源自理论语法

其实笔者个人认为，语法就是语法，以上的分类只不过相当于“数学专业的数学课程” 和 “非数学专业的数学课程” 的关系罢了，他们本质上并不是两种东西。

### 规范性语法和描述性语法
在教学语法中，仍然可以继续进行分类，如下：

- 规范性语法：语法是一套以明文撰写的规则，所有人必须按照这种规则来，否则就是错的

- 描述性语法：语法和法律并不一样，不具有那么强的强制性，我们只是忠实记录人们是怎么使用某一门语言的。



### 总结

```viz{align=center}
graph G{
	graph[rankdir=LR]
	语法 -- 客观世界的语法
	语法 -- 作为学科的语法

	作为学科的语法 -- 理论语法
	作为学科的语法 -- 教学语法

	教学语法 -- 规范性语法
	教学语法 -- 描述性语法
}
```

## 本书中语法的含义
本书的语法指的是 **教学语法** -- **描述性语法**

# 本书特点
本章节列举的 “特点” 主要指的是与传统语法教材不同或者进行了革新的地方。

有一些地方可能会给出一些语法概念的新定义。

## 层次分析法贯穿始终

### 层次分析法

1. 层次性是语言的基本属性之一：语言是由不同层次的**语言结构**从低到高一层一层构建起来的；

2. 除了最底层和最高层，每一层结构都由更低层的结构构建而成，同时也是其上层结构的构建材料；


### 传统语法突出的问题

传统语法在语法结构上的问题有两个：

1. 不太重视词组结构；

2. 不太重视甚至忽视分句结构；

### 对词组结构深入探讨

1. 尤其对名词词组进行深入探讨

2. 第一点引出了限定词的问题：把传统意义上的某几类词语归为一类新词类即限定词


### 对分句结构进行深入探讨
1. 传统语法对于分句和句子的概念有些纠缠不清；

2. 传统意义上我们所说的 “句子结构” 和 “基本句型” 中的句子在本书体系中指的是独立分句

## 词法与句法的关系

- **以句法为主线，以句法带动词法，并以词法丰富加深句法的内容**

- **句子结构和词汇意义是紧密结合的，特定的句子结构往往要求某种意义的词与之搭配**

## 限定词作为单独的词类

### 限定词概念的内涵

- 位于名词词组中，名词中心词或者名词中心词前的前置修饰语之前；

- 对中心词的意义起特指、类指、定量、不定量等限定作用；

### 限定词和修饰语的主要区别

- 前者只关系到名词中心词的外部关联；

- 后者却描绘名词中心词的内在特征；

### 把限定词作为一类独立词汇的理由

- 某些理论语法研究流派早年已经提出这一观点；

- 越来越多的语法巨著和权威词典接纳了这一分类方法；

- 冠词、形容性物主代词等许多词在语法结构上是类似的

## 两“时”两“体”

### “时” 和 “体” 的区分
1. 时 是表示时间区别的动词形式；

2. 体 是表示动词状态或者其存在方式的动词形式；

### 传统语法学中的观点

1. 受拉丁文的影响，认为英文的时和体是不可分的；

2. 只讲 tense 不讲 aspect，而且认为前者包含后者；

3. 认为存在 “将来时” 和 “过去将来进行时”

4. 多达 16 种分类：

	| - | - | - | - |
	| --- | --- | --- | --- |
	|一般现在时|一般过去时|一般将来时|过去将来时|
	|现在进行时|过去进行时|将来进行时|过去将来进行时|
	|过去完成时|过去完成时|将来完成时|过去将来完成时|
	|现在完成进行时|过去完成进行时|将来完成进行时|过去将来完成进行时|

### 新观点

1. 时和体是独立的语法范畴

	- 尽管它们常常在一起使用，但是它们的表现形式是不一样的：时常用**屈折形式**表示，而体却经**分析形式**表示；

	- 语义上它们也具有高度独立性：

		> He is writing a letter.

		> He has written a letter.

		这两个句子都是对现在的事情的描述：前者是现在正在发生、进行的事情，后者是截至现在已经发生了的事情；但是它们的动词的体是不一样的，前者是未完成状态，后者是已经完成的状态；

		> He was writing a letter.

		> He had written a letter.

		这一组句子和上一组句子的对比非常明显，各自的 aspect 是一样的，但是时间是不一样了，由 “现在” 变成了 “过去”。

	- 时和体的紧密联系，并不代表它们是同一个概念；

	- 进行体和完成体在非限定形式中，可以不和 “时” 结合而单独出现；


2. 不存在将来时和过去将来时

## “将来时间表示法”取代“将来时”

### 时间和语法中的“时”的辨析

1. 时间是一个哲学概念和物理客观存在：全世界的人的时间都是相同的，都存在 过去 现在 将来 之分（别抬杠扯什么相对论）

2. 时(tense) 却是一个语法概念，且不一定和朴素的对于时间的印象完全重合

	- 法语中有过去时，现在时，将来时

	- 现代汉语（作为一门分析语）是靠词汇（尤其是虚词）来区分时间概念的，根本不存在 tense 这种东西；

	- 英语（按照新的语法观点）只有现在时和过去时

### 为什么说不存在 “将来时”
1. 现代英语中不存在专门用来表示将来时的动词形式

	想想的确是这样的，过去时有 "-ed 过去形式"，但是将来时真的没有对应的屈折形式；

2. 传统语法中表示将来时的所谓 “标记”：will/shall 以及 would/should，本身都是情态助动词，其表示的将来含义也可以视作一种情态意义；

### 英语中仍有丰富的用于表达将来时间的表示方法
1. will/shall + 不定式

2. would/should + 不定式

3. be going to + 不定式

4. be to + 不定式

5. be + -ing

6. 一般现在时表示将来

## “假设意义表示法” 取代“虚拟语气”
### 当初为什么要有虚拟语气这种东西

一言以蔽之：用来表示**假设意义以及其他非事实意义**

比如：

> 如果我是钢铁侠就好了，那我就可以天天泡妞吃喝玩乐了

> 你本就不应该生孩子，让他到这个世界上受苦

> 我就是从这里跳下去，死外边，也不吃你们一点东西（真香）

这些句子的前半部分所描叙的事件，都没有真实地发生，只是存在于我们的假设当中。然而在一门语言中，我们仍需要某种方式表达这些“脑海世界” 中的事件，并将其与真实事件陈述相区分，这就有了传统意义上的“虚拟语气”。

### 传统语法在这方面的观点
1. 把所有用以表达假设意义的语法手段都归类到 “虚拟语气” 中；

2. 导致虚拟语气的内容非常驳杂，难以掌握；

### 修正后的观点

1. 原来 “虚拟语气” 所指的概念换个名字，用 “假设意义表示法” 代替

2. 新的 “虚拟语气” 一词专门指代两种语法形式：

	- were -型虚拟语气
	- be -型虚拟语气

3. 其他形式，如一般过去时，过去完成时等也可以用来表示假设意义，但不再称为 “虚拟语气”，而统称为 假设意义表示法



## “-ing 分词”、“-ed 分词” 取代 “动名词“、“现在/过去分词”

### 旧称

在过去，非谓语动词（准确说叫非限定动词，下面会说到）主要用这几种

- 不定式

- 动名词

- 现在分词

- 过去分词

### 新观点的修正
非限定动词的分类为：

- 不定式

- -ing 分词

- -ed 分词

0. 过去分词 和 现在分词 的名字的确可能不太恰当，因为**分词是动词的非限定形式，不存在 tense 的区别**

1. -ing 分词包含了传统意义上的 “动名词” 和 “现在分词”，从此在名称上不再区分这两者

2. 但是 “动名词” 和 “现在分词” 也的确是不一样的呀！ 没关系，它们的不同就被视作是 -ing 分词的两种功能

3. 值得说明的是，从语言发展的历史角度来讲，动名词和现在分词的确不是一个东西：前者原是以 -ing 结尾的**阴性名词**，后者是以 -end 结尾的**形容词**，但是它们最后在形式上表现为一致了（感觉传统语法终于做对了一件事情）

4. 笔者觉得，作者这么划分，是为了一定程度上进行简化，虽然是否真的能如愿还不好说。


## “非限定动词” 取代 “非谓语动词”
这里并没有涉及过多的技术上的细节，只是换了个词而已。但是，笔者认为这一修正非常好，笔者试讲自己的理解归纳如下：


1. 首先，笔者猜想一下，为什么原来的语法体系中要将其翻译为 “非谓语”动词：

	- 因为，non-finite verb 的确不能作其所在的整个主句的谓语，这是千真万确的；

2. 为什么 “非谓语” 这个术语不好；

	- 正如我们所说，传统语法不太重视分句结构；尽管 non-finite verb 没法作为主句的谓语；可是如果把它们所处的从属结构看做一个“分句”，那么**它们自身就是所在的分句的谓语**

	- 这里隐含的逻辑变化是：原来只有主句才是一个句子，主句的谓语才能叫谓语；但是修正后，一个从句也可以是一个“句子”，其也可以有自己的“谓语”

	- 作者也提到了一点（笔者自己未想到）：非谓语动词容易给人一种暗示，仿佛主句中的动词成分就是谓语，但是（根据本书语法体系的定义），这种定义是很成问题的。

3. 为什么 “非限定” 这个术语好：

	- 首先，“非限定” 这一翻译更加忠实了英文原来的术语 "non-finite"

	- 所谓 "non-finite" 就是说其不带 tense 的标记，也不受主语的人称和数的影响——仔细回想一下，这才是 “非谓语动词” 和 “谓语动词” 的**最显著的区别**！！而不是 “能不能作谓语” 这种没有抓住重点的方面；

原作还提到了限定动词和非限定动词，限定动词词组和非限定词组在形式上的区分，以后详述。

## “情态助动词” 取代 “情态动词”

### 为何某些语法书使用 “情态动词”

因为它们认为，助动词一定是无词汇意义的，而情态动词可以表示情态意义，所以不应该归为助动词；

### 修正后的观点

- 区分助动词和主动词的核心准则不在于有没有词汇意义，而在于能否单独作为句子的谓语动词



## ”关系分句“ 取代 “定语从句”

1. 定语从句的叫法是依据其 主要句法功能 而得出的；而 关系从句 这一称法是依据其结构形式来定的——而本书绝大多数术语都是依据其**结构形式**来命名的；

2. 关键在于，同一结构形式可以有不同的句法功能——我们传统上所称的**定语从句**也不例外

3. 定语从句（姑且先这么叫）的首要功能就是作为名词词组的修饰语（定语），但除此之外，还有别的作用（语义上的）

	- 注：不过笔者倒是觉得，如果强行将它们理解成定语也没有问题…………