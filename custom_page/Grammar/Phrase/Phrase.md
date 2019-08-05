---
title: 语言层级：词组
date: 2019-08-05 21:56:29
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

# 词组的定义

略，单独地陈述其定义没有多大的意义，这种体系内的层级概念一定要结合体系本身来理解，而之前已经介绍

# 词组的分类

1. **名词词组**

2. **动词词组**

3. **形容词词组**

4. **副词词组**

5. **介词词组**


**注意到了吗：这里出现的 词 的类别比英语中实际的词类少了很多，如前所述，有一部分词是辅助性的，它们不能作为一个词组的 “中心” 出现**

# 各类词组的定义

`...` 词词组
:    以 `...` 词为中心词的词组

这里的 `...` 可以代入以上五种词类中心词。

## 名词词组

其形式以后介绍

## 动词词组

0. 定义

动词词组比较特殊，其定义是 **“以主动词为中心词的词组”**，而不仅是 “以动词为中心词的词组”！

1. 形式

    ```viz{align=center}
    graph G{
        "(若干个) 助动词 + 主动词，附带修饰语"[shape=none]
    }

    其中，主动词是必须的，其他两者都是可选的

2. 按照动词形式分类：限定动词词组 / 非限定动词词组

请参见[概念梳理：动词，词组，分句的限定 / 非限定形式](../Finite_and_non_Finite/Finite_and_non_Finite.html)

// TODO

## 形容词词组

1. 形式

    ```viz{align=center}
    graph G{
        "修饰语 + 形容词 + 后置修饰语（补足成分）"[shape=none]
    }

## 副词词组

1. 形式

    ```viz{align=center}
    graph G{
        "修饰语 + 副词 + 后置修饰语（补足成分）"[shape=none]
    }

## 介词词组

1. 形式

    ```viz{align=center}
    graph G{
        "修饰语 + 介词 + 介词补足成分（介词“宾语”）"[shape=none]
    }

2. 介词补足成分

    1. 一般而言，是一个名词词组或者相当于名词词组的成分

        ```
        I feel sorry for his parent.

        He worked all day without ever complaining.

        He was shocked for what he saw.
        ```

    2. 也可以是形容词或者副词，这种情况常出现在某些固定搭配中

        ```
        from here / there

        in there / here

        before long 
    
        until now

        at last 

        since then

        at once

        at worst
        ```

        **这是一种我们经常会见到，但是进行语法分析时时难以定性的一种情况**

    3. 介词词组本身也可以作为介词补足成分，从而最终在具体的 语言项实现 中呈现为 **两个连续出现的介词**

        ```
        He picked up the gun from under the table.

        He suddenly appear from behind the door.

        We didn't meet until after the show.

        Food has been scarce since before the war.

        The weather has been fine except in the north.
        ```

        **这是一种偶尔会见到的用法，而且感觉很新奇，一般都不好把握其语法性质**

3. 修饰成分

    这是可选的成分，用来表示程度，范围等含义

    ```
    I left it just inside the garage,

    He had wandered right off the path.

    There was rubber all over the place.

    They followed right behind us.

    The dog was lying right in the middle of the frozen lake.
    ```
## 修饰成分

**修饰成分可以出现在以上所有类别的词组中，而且都是可选的。**