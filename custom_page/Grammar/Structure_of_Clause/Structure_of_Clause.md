---
title: 分句结构与成分
date: 2019-08-06 20:26:34
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

# 说在前面：讨论主题和范畴

由前面的笔记我们可以得知，从分句到句子这一步，主要是通过从属和并列两种手段得到的，而对一个复杂的句子进行递进地剖析还原后，我们不难发现，最终构成句子的基石的仍是简单句。

因此我们平时所说的 “句子结构” 实际上是 “分句结构”，而且准确地说，是**作为简单句的独立分句结构**。

# 分句的核心：主语 + 谓语

## 概念内涵

**主语的意义**

1. 是沟通的话题或主题，作为**信息传递的出发点和中心**

2. **隐含一种 “静态” 的指称含义**，指称的对象可以是物理世界的事物，可以是思维世界的概念；

3. 通常由 名词词组 或者相当于名词词组的语法结构担任；

**谓语的意义**

1. 沟通话题的具体内容，是**信息传递过程所表达的新信息**；

2. **隐含一种 “动态” 的述说含义**，围绕着主语发挥如下功能

    - 叙述**事实和关系**

    - 判定**性质或是非**

    - 传达**态度与意向**

    - ......

3. 英语的谓语是动词性的，也即**谓语以动词为中心**，动词必须存在（无动词分句只是省略了动词）

示例：

|主语|谓语|
|---|---|
|China|is a great country|
|Marxism|is a universally applicable truth|
|None of the girls|like football|

# 术语辨析：谓语、动词、谓语动词

本节主要辨析一下这几个术语在本书和传统语法中的不同含义

||本书的语法体系|传统语法|
|---|---|---|
|动词|特指动词这种词类|
|谓语|一个完整的分句中，除去主语的部分|本书语法体系中的“谓语动词”|
|谓语动词|谓语中表示核心述说含义的那部分动词词组|主句中构成谓语（传统意义下的）的动词|

## 解释

这其实是个悠久的历史问题，涉及到语法学术语的翻译问题

1. "verb"

    动词，作为一种词类来看待，英文中称为 

2. "predicate"

    一个完整的分句中，除去主语的部分

    有些语法书将其翻译为 “谓语”——本书就是这样做的；而有些语法书将其翻译为 “谓语部分”，或者其他的别的术语；

3. "predicate verb / predicator / verb"

    本书将其翻译为 谓语动词，**需要注意的是：这不是一个“词”的类别，而是句子/分句的功能成分**！有些书也称其为 谓词；

    而传统语法体系里面，这个术语被翻译成 “谓语”

4. 谓语动词

    传统语法学里面，把构成限定分句的 predicator 部分的动词成为 谓语动词——因为在传统语法体系中，非限定形式的动词不能称之为 “谓语”

## 例子

传统语法体系的划分如下：

```viz{align=center}
graph G{
    graph[rankdir=TB]
    node[shape=none]

    subgraph A{
        rank = same
        a -- b -- c -- d -- e[style=invis]
        a[label="Having finished"]
        b[label="his mission,"]
        c[label="the solider"]
        d[label="would lean"]
        e[label="on the tree."]
    }

    V[label=谓语动词]
    P[label=谓语]
    N[label=非谓语动词]

    splines=false
    N -- a
    V -- d:ne
    d -- P
}
```

新语法体系的划分如下：

```viz{align=center}
graph G{
    graph[rankdir=TB]
    node[shape=none]

    subgraph A{
        rank = same
        a -- b -- c -- d -- e[style=invis]
        a[label="Having finished"]
        b[label="his mission,"]
        c[label="the solider"]
        d[label="would lean"]
        e[label="on the tree."]
    }

    V[label=谓语动词]
    P[label=谓语]
    N[label=非限定动词]
    P2[label=分句谓语]
    F[label=限定形式动词]

    splines=false
    N -- a
    a:sw,b:se -- P2
    F -- d:nw
    d -- V
    d:s,e:se -- P
}
```

# 主语的结构形式

```viz{align=center}
graph G{
    
    graph[rankdir=LR,splines=true]
    
    a:e -- b:w,c:w,d:w,e:w
    b -- c[constraint=false,style=dashed]
    a[label=主语]
    b[label=名词词组或者相当于名词词组的语法结构（如代词）]
    c[label=前者经过并列后形成的并列结构]
    d[label=非指代性it]
    e[label=存在性引导词there]
}

```

1. 其中前两者是有实际指代含义的；

2. 后两者没有实际的指代，仅用以赋予分句形式上的 “中心”

3. 非指代性 it 具体而言大概有这么几项

    - it is amazing that he finished all his job. (形式主语，没有任何实际意义)

    - it is warm today (指代天气)

    - it is ten o'clock (指代时间)

    - it would be ten miles from there. (指代距离)

    - it is very quiet in the meeting room. (指代环境)

    - ...

    除了第一项外，其它都是对时间、距离、环境、天气等事物的**泛指**

# 谓语的结构形式

## 谓语形式

### 第一种剖析方式

总得来说，谓语的形式一般可以宽泛地总结为：
<p align="center">谓语动词 + 补足成分</p>

而更进一步地说，补足成分的具体类别就是：宾语、补语、状语等；

1. 谓语动词：

    谓语动词由**动词词组**构成，因此谓语动词的形式其实就是动词词组的形式：

    <p align="center">[助动词1 + 助动词2 + ... ] + 主动词 </p>

    前面的助动词出现与否，以及出现的具体数量并不是固定的。根据助动词出现与否，我们可以继续对谓语动词进行分类：

    - 简单动词词组：没有助动词，只有主动词

    - 复杂动词词组：有助动词和主动词

2. 补足成分：

    - 宾语

    - 补语

    - 状语

再次重申，定语属于修饰语，是词组的构成成分，不是分句的成分。


### 第二种剖析方式

<p align="center">操作词 + 述谓成分</p>

1. 操作词：

    - 对于复杂动词词组而言，操作词就是**第一个主动词**

    - 对于绝大多数简单动词词组而言，操作词是隐式的，即助动词 do （具体形态取决于动词的 tense）

    - 若 have 和 be 作为简单动词词组中的主动词，那么它们本身就作为操作词存在

2. 从操作词的作用我们可以感性地把控其语言意义：

    - 协助主动词构成**否定结构**和**疑问结构**

    - 体现 tense 的特征；

    - 体现情态意义

    - 体现主语的 “人称” 和 “数”

笔者的感受：操作词给人一种动词词组的 **“聚焦点”** 的感觉，因为我们进行否定或者疑问，以及限定形式的体现都是针对操作词来进行的，这个概念提出得非常好！

3. 述谓成分：除了操作词外，谓语中剩下的部分，也即 “主动词 + 补足成分”

## 特殊谓语：双重谓语

双重谓语
:    // TODO

## 谓语动词决定谓语的架构

如前所述，谓语动词中的助动词担任许多语法层面上的功能，而主动词也同样在语法层面上具有非同一般的 “话语权”。

<p align=center><b>谓语动词中的主动词决定了谓语中是否带有补足成分，以及具体带有什么补足成分，从而决定了谓语的布局架构。</b></p>

根据这一准则，谓语的架构有如下几种：

1. 动宾结构：及物动词 + 宾语

2. 系补结构：系动词 + 补足语

3. 动状结构：不及物动词 + 义务状语（该术语以后解释）

4. 不及物结构： 不及物动词

5. 双宾语结构：双宾及物动词 + 直接宾语 & 间接宾语

6. 复宾语结构：复宾及物动词 + 宾语 & 宾语补足语

7. 动宾状结构：及物动词 + 宾语 + 义务状语

这七项结构其实已经非常接近我们平常所说的 “基本句型” 了，后者只是在前者的基础上加上主语而已。

# 基本句型

具有不同架构的谓语都可以和主语结合，从而形成不同架构的分句；从架构的角度来看，“谓语架构” 上升到了 “分句句型” 的概念。

如前所述，谓语架构有七种，从而分句架构也有七种；在其中，有五种认为是基本的分句句型，另外的两种相对而言稍微罕见一些。

## 七种基本句型

### SVC 结构

即

```viz{align=center}
graph G{
    node[shape=none]
    "主语 + 谓语动词 + 补足语（更准确地说，是主语补足语）"
}
```

1. 这种句型中的谓语动词绝大多数情况下是系动词

2. 可以作为主语补足语的，一般有

    - 名词词组

    - 介词词组

    - 形容词词组 

    - 副词词组

    - 非限定动词词组

    - 相当于名词结构的从属分句

**注意**：我们来考虑一类句子

```
The suitcase weights 10 kilos.

Blue Whale, the largest animal ever lived on earth, can weight up to 180 tonnes.

The room measures 30 feet long.

My hat costs 20 pounds.

His debt total $100,000.
```

这类句子的主要内容都是在陈述一件事物在某个可计量维度上的度量或数值，包括且不限于：

- 重量

- 长度

- 体积

- 数量

- 金额

- ......

**问题来了**：句中的谓语动词 `weight`, `measure`, `cost`, `total` 等属于什么类型的动词？这些句子的句型结构是哪一种？

1. 观点一：认为它们是 “主谓宾” 结构：

    支持者认为：

    - 这个观点看上去貌似是非常符合直觉的；

    - 如果把后面的计量尺度扇区，句子就会变得不完整；

    - 这类句子可以用 what 来进行提问：`What does it cost?`, `What does it weight?`

2. 观点一的缺陷：

    - 这类句子没有被动结构，我们不能说 `30 feet long is measured by the room.`

    - 这类句子中有些谓语动词属于不及物动词

3. 观点二：它们是 “主谓状” 结构：

4. 观点二的缺陷：这里的谓语动词并非全都是不及物动词；

5. 观点三：它们是 “主谓补” 结构：

    - 前提是示例中的词需要看作或定义为系动词；

    - 把述谓成分看作补语，也可以用 what 来进行提问；

    - 主系补结构一般没有被动结构，也正好印证这一点；

    - 可计量范畴内的数值或者度量严格来说并不是一个实体，更像是一种抽象层面上的 “性质”，就好比我们无法定义某个实物作为 “红色” 的本体；

    - 因此它们可以看作是对主语属性的说明

6. 观点三的缺陷：

    - cost 解释为及物动词，后面接一个宾语其实严格来说也能让人信服

**总结**：自然语言的模糊性是其本质属性之一，我们没有必要像研究数学一样对其严格化；以上三种说法，观点三值得我们重视，笔者也倾向观点三的看法。




### SVO 结构

即

```viz{align=center}
graph G{
    node[shape=none]
    "主语 + 谓语动词 + 宾语"
}
```
### SV 结构 

即

```viz{align=center}
graph G{
    node[shape=none]
    "主语 + 谓语动词"
}
```
### SVOo 结构
即 

```viz{align=center}
graph G{
    node[shape=none]
    "主语 + 谓语动词 + 直接宾语 & 间接宾语"
}
```

这种句型中的谓语动词的主动词一般成为双宾及物动词，直接宾语一般指代 物，间接宾语一般指代 人。

### SVOC 结构
即

```viz{align=center}
graph G{
    node[shape=none]
    "主语 + 谓语动词 + 宾语 & 宾语补足语"
}
```

这种句型中的谓语动词的主动词一般成为复宾及物动词。

宾语补足语可以由以下单位充当：

- 名词词组

- 介词词组

- 形容词词组

- 副词词组

- 非限定动词词组

### SVA 结构 与 SVOA 结构

这两者可以视作 SV 与 SVO 结构的一个扩展；

此处的 状语 被称为 **义务性状语**[^1]，之所以需要加上它是因为如果没有这个状语，句子会变得极为别扭，甚至语义不完整。

SVA 示例：

```
He lives in London.

The war lasted for eight years.

The plane took off at 8:30.
```

SVOA 示例：

```
I'll drive you to the station.

The old man treated me kindly.
```

**说说笔者个人的看法**

其实，这两种句型感觉没有之前的基本句型那么独一无二，在语义上还是有一定的模糊的余地的；

同时 义务性状语 的存在也并没有其他成分那么 “绝对必要”

**比如**，在书中，有一些句子被认为是 SVOA，但是笔者却不这么认为：

```
I put my hand on his shoulder.

Jackson brought his case upstairs.

They have put man on the moon.
```

这些句子宾语后面的部分，无一例外都与宾语本身形成 “主谓意义”，用以说明宾语自身的性质或者当前状态，因此把它们看作宾语补足语也未尝不可。

再说了，书上本来就说宾语补足语可以由副词短语、介词词组担任，为什么却强行把他们看作状语呢？？

[^1]:这是笔者自己起的名字哈哈哈

## 基本句型的扩增

三种手段：

1. 不断增加修饰语（比如定语）

2. 包孕（从属）现象

3. 并列现象


---

# 语义角度考察分句成分

**分割线以上的部分主要是从语法与形式的角度来考察分局的成分，而接下来主要从语义与功能的形式来对它们进行研究。**

严格来说，前面所述的分句成分，也就是主谓宾状补，是分句的中心成分，因为他们在构成分句时不可或缺。除此之外，还有一些处于分句结构的边缘地位的成分——我们称之为边缘性成分。

需要注意的是，状语由于其形式和功能的灵活性，它相比于主谓宾补处于更加边缘的地位，可以视为从中心到边缘的过渡成分。

另外，状语自身也可以进行分类：
1. 修饰性状语

2. 评注性状语

3. 连接性状语

# 分句中心成分

## 主语
从语义角度对主语进行分类：

1. 施动主语和受动主语：说明谓语表示的动作和行为的**施行者以及承受者**

    ```
    The farmer killed a snake.

    The farmer was killed by a snake.
    ```

    值得注意的是，有些情况下，语义上的受动并不需要通过被动语态来表示：

    ```
    This material feels nice.

    The matches won't strike.

    The zip doesn't close properly.
    ```

2. 地点主语和时间主语：并不是动作与行为的施动者和承受者，而只是用以表示时间或者地点

    ```
    The bedroom sleeps six students.

    Tomorrow will be a good day.

    Last night was very cold.
    ```


3. 事件主语：表示某一事件（通常是叙述其发生的时间或者地点）

    ```
    The meeting is on the next Sunday.

    The exam will take place tomorrow.
    ```

## 谓语

略。

## 宾语
从语义角度进行分类，宾语可以分为以下几类：

1. 受动宾语：行为或动作的承受者，或者受到行为或者动作的影响

    ```
    She lowered her head and sai nothing.
    ```

    这是宾语最常见、最基本的语义。

2. 结果宾语：表示动作产生的结果

    ```
    He dig a hole.

    We painted a flower on the wall.

    He asked many questions.
    ```


3. 转喻宾语：这种宾语表示的是动作对象有关的事物

    ```
    He wiped off the table (wiped off something off the table).

    They have hatched chickens. (have hatched eggs).
    ```

4. 使役宾语：表示动作的使役对象

    ```
    He stood the little child against the wall.

    She danced the baby on her knees.
    ```

5. 同源宾语：大多用在不及物动词之后，以名词形式重复动词的动作概念，且其往往具有修饰语

    ```
    He slept a peaceful sleep.

    He died a heroic death.
    ```

    若充当这个同源宾语的名词词组的前置修饰语有最高级形容词或者相当于最高级形容词的结构，那么名词中心词可以省略。

    ```
    He shouted his loudest.

    He breathed his last.
    ```

6. 其他

## 补语

### 补语的分类

1. 主语补语：也就是我们平时说的表语

2. 宾语补语

### 补语的语义

从一般的意义上说，主语和主语补语的关系是这样的，后者用于说明前者的：

- 身份

- 属性

- 状态

当然，宾语和宾语补语的关系可能会更加广泛一些：它们更像是 主语与谓语 的关系

## 状语：修饰性状语

作为分句中心结构的状语指的主要是修饰性状语，**它修饰的对象是谓语动词 + 其他补足成分**，不单单是谓语动词

修饰性状语又称为 **附加状语**

### 时间状语

语义上继续细分类可以分为：

- 表示具体时间的

- 表示时间频度的

- 表示时间长度的

如果这三类同时出现在句尾的时候，排列顺序应该是：

长度 -> 频度 -> 具体时间

```
He stayed in the country for a day or two / every month / in those years.

I want to see him very often when I was in Shanghai.
```

### 地点状语

语义上继续细分：

- 表示事情发生的空间位置

- 表示动作行为的方向

关于位置：

1. 地点状语的位置一般不固定，一般位于句首，有时也位于句尾。

2. 两个或以上的地点状语连用，一般小地点在前，大地点在后。

3. 可以把较大地点移到句首，但是不能将小地点状语移到句首

4. 地点状语与时间状语连用时，地点状语一般在前面

### 方式状语
可充当方式状语的语法单位：

1. 副词词组

2. 介词词组 

3. 名词词组

4. -ing分词分句

5. 限定分句

**注意**：不定式分句不能充当方式状语

**顺序**：方式状语 -> 地点状语 -> 时间状语

### 目的状语
可以充当目的状语的语法单位：

1. 不定式分句

2. 介词词组


### 原因状语
可以充当原因状语的语法单位：

1. 介词词组

2. 不定式分句

3. -ing分词分句

4. -ed分词分句

5. 由某些连词，如 because、as、since、for 等引导的限定分句


### 结果状语
可以充当结果状语的语法单位：

1. 不定式分句：通常位于句尾，表示发生在谓语动词的行为之后，形成一定的因果关系，可以选择用（或者）不用逗号隔开；

2. -ing 分词分句：

3. 一部分介词词组


### 条件状语
可以充当条件状语的语法单位：
1. 条件状语从句（最常见的）

2. 介词词组：

3. 非限定分句

### 让步状语
可以充当让步状语的语法单位：
1. 限定分句

2. 介词词组

3. 非限定分句



### 伴随状语

通常由 -ing 分词分句或者 -ed 分词分句充当，经常带有自身的逻辑主语，也时常会加上介词 with；

多数位于句尾（句首也可以），用逗号和主句隔开

用于说明谓语动词发生时伴随的情形和事态。

# 分句外围成分

## 评注性状语

评注性状语，又称为**分离性状语**或者**外加状语**

可以从两个方面来把握其含义：

1. 它不像修饰性状语那样，仅仅围绕修饰谓语；相反，评注性状语是对其所在的整个句子进行说明或者解释；而且从语义和语气上看，这种说明和解释仿佛是脱离句子其他部分的内容，站在某个 “上帝视角” 来叙述的。

2. 从结构上，它与被评说的句子结合得非常松散，双方常用逗号隔开

可以充当评注性状语的语法单位：

1. 副词词组

2. 介词词组

3. 非限定分句

4. 无动词分句

5. 偶尔也有限定分句

## 连接性状语

连接状语，又称为 **联加状语**

可以充当连接性状语的语法单位：
1. 副词词组

2. 介词词组

**联加状语**的含义：

1. 首先它不对句子的内容进行修饰或者评注，所以它不同于修饰性状语，也不同于评注性状语

2. 它引导的分句不能算是从句；从句这个概念是在一个句子内讨论的，而联加状语一般是在**句子之间**引导关联关系；

3. 它也不能算并列连词，因为它本身就可以和后者一起使用

从语义角度，联加状语可以分为

1. 列举和顺序：

    ```
    firstly, secondly, thirdly， ...
    one, two, three, ...
    for one thing...for another
    for a start
    to begin with
    in the first place, in the second place, ...
    next, then
    finally, last, lastly
    ```

2. 意义增补和引申

    ```
    also, besides, furthermore, moreover, then, in addition, above all, what is more
    ```

3. 同位关系

    ```
    namely
    for example, for instance
    that is, that is to say
    ```

4. 结果

    ```
    consequently, hence, so, therefore, thus, as a result
    ```

5. 意义等同

    ```
    equally, likewise, similarly, in the same way
    ```

6. 推论

    ```
    or else, otherwise, therefore, then, in that case
    ```

7. 表示换个说法

    ```
    alternatively
    rather
    in other words
    ```

8. 意义转折

    ```
    instead
    on the contrary
    in contrast
    by comparison
    (on the one hand), on the other hand
    ```

9. 让步

    ```
    however
    anyhow, anyway
    nevertheless
    still
    though
    yet
    in any case
    at any rate
    in spite of that
    after all
    all the same
    ```

10. 时间过渡

    ```
    meanwhile
    in the meanwhile
    meantime
    ```

11. 改变话题

    ```
    by the way
    incidentally
    ```

12. 概括或者总结

    ```
    in conclusion
    in a word
    to sum up
    in all
    ```

## 插入语

插入语
:    与谈论话题没有直接关系的部分，表示语义和话锋的显著转折

插入语一般用逗号和句子分开，也可以使用破折号与句子分开，有时也使用括号分隔。

## 呼唤语

呼唤语
:    顾名思义，是用来 “呼唤” 某些对象的，因此一般是事物、人称，甚至是抽象概念的指称，以及专门的称呼

具体对其外延分一下类如下：

1. 家庭成员名称：father, mom, honey, granny etc.

2. 用于称呼的一般性用语：Miss, Mr, Mrs, Ms, Sir, Madame

3. 亲昵称呼：dear, baby, darling

4. 表示职业的称呼：Professor, Doctor, Senatoe

    请注意，某些地位不太高的职业，如driver、waitor等直接称呼职业会略显不礼貌

5. 有时候就是名词词组或者名词性分句

    ```
    Avengers, assemble!

    Workers of the world, unite!

    Whoever wants to stay here a little longer, please stand up.
    ```


## 感叹语

感叹语
:    用于表示各种强烈情感的词语

如何使用？？

1. 可以单独成一个句子，即感叹句，需用感叹号

2. 感叹语依附与一个句子，用逗号和句子隔开，句子末尾使用感叹号；如果要强烈表示语气，则感叹语和句子末尾都加感叹号

3. 感叹语通常由感叹词表示

感叹词的分类
1. 情感感叹词：只表示说话人情感（大多数感叹词属于此类)

2. 祈使感叹词：促使对方行动，也附带较为强烈的语气

3. 其他词类转换而来的感叹词

    - Why
    - What
    - Well
    - Now
    - Look
    - Here
    - My


## 句首肯定/否定词

无非 Yes / No 及其变体，全世界都知道，写到这里太累不写了。