---
title: Python学习笔记-002
date: 2019-04-11 22:24:06
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

继续学习 Python

<!-- more -->

# Python 内置数据类型
## List
笔者认为类似于线性表，元素是有序的

1. 索引从 0 开始
2. 索引超出范围，会报 IndexError 错误（边界检查）
3. 比较特殊之处：索引是负值，则返回从后往前数的第 i 个元素
4. 综合上面两点，索引值不能超出长度的绝对值（减1）
5. **一个List中的元素数据类型可以不同**

    ```
    >>> fuck=['sdg',3453,True,234.53]
    >>> fuck
    Out: ['sdg', 3453, True, 234.53]
    ```
6. 有效操作：

    1. 获取长度：`len(ListName)`
    2. 末尾追加元素：`ListName.append(ElemName)`
    3. 末尾删除元素：`ListName.pop()`
    4. 插入到指定位置：`ListName.insert(num,ElemName)`，，其中 `num` 是新元素插入后的索引值
    5. 弹出指定位置元素：`ListName.pop(num)`，其中 `num` 是被弹出元素的索引值
    6. 修改某个元素：直接赋值 `ListName[i] = NewElem`

7. List 类型的对象是可以嵌套的（可以方便地表示高维数组）
8. 空的 List 就是一个元素也没有，其长度为 0

## Tuple
与 List 非常类似，但是一旦初始化就不能修改

1. Tuple 在定义时用的是圆括号，而 List 用的是方括号
2. Tuple 没有赋值操作，没有 `insert()`, `append()`, `pop()` 等操作，因为它是不可修改的
3. 定义空的 tuple 如下：`tuplename = ()`
4. 定义只有一个元素的 tuple 时，元素后面必须有一个逗号，不然 python 会把括号视作数学公式中的小括号

    ```
    >>> t1=(2)

    >>> t2=(3,)

    >>> t1
    Out[10]: 2

    >>> t2
    Out[11]: (3,)
    ```

## Dict
在其他语言中也称为 map（笔者觉得有点类似于 Hash 表），存储模式为 key-value，定义格式如下：
```
{key1: value1, key2: value2, key3: value3, ...}
```
特点：

1. 查找速度极快
2. 有效操作：

    1. 初始化（注意此时使用的是花括号`{ }`）
    2. 根据 key 查找 value，若 key 不存在则会报错
    3. 添加数据
    ```
    fuck['sdfsdf']=36346346
    ```
    注意，对于同一个 key 放入多个 value，后面的值会把前面的冲掉
    4. 查找一个 key 是否在 dict 中
    ```
    >>> 'ss' in fuck
    Out[6]: True
    >>> 'rgdfsdf' in fuck
    Out[7]: False
    ```
    5. 删除一个 key：`pop(KEY)`

3. dict 内部存放的数据和 key 放入的数据是没有关系的
4. **dict的 key 必须是不可变对象！例如：字符串、整数、tuple 等，变量、list 这些对象是不能用作 dict 的 key 的**

## Set
笔者觉得它其实就像是数据结构中的 **并查集**

1. set 只存储一组 key
2. set 中的 key 不能重复
3. 有效操作：

    1. 定义/初始化：
         - 可以使用大括号 { } 或者 set() 函数创建集合，但是注意如果创建一个空集合必须用 set() 而不是 { }
         - 另外，set() 函数只能有一个参数，可以是 list、tuple、 字符串等，实际在创建的时候，set 会分割单个的元素


    2. 添加元素：`add()`
    3. 删除元素：`remove()`
    4. 并、交、差操作：
    ```
    >>> x & y         # 交集
    set(['o'])
    >>> x | y         # 并集
    set(['b', 'e', 'g', 'l', 'o', 'n', 'r', 'u'])
    >>> x - y         # 差集
    set(['r', 'b', 'u', 'n'])
    ```
    




# 分支与循环
## 分支
记录一下几个值得注意的地方

1. `if`, `elif`, `else` 该行后面都要有一个 `:`
2. 真假值的判定：非零值、非空字符串、非空list 等之外都为 True

## 循环
1. for 循环

    ```
    for x in [ListName]/[TupleNamr]
        [Do something]
    ```

    将 List 或者 Tuple 的每个元素带入 x，执行循环体的语句

2. while 循环

    ```
    while EXPRESSION
        [Do something]
    ```

# 再议不可变对象
以 字符串 和 list 为例子：
```
>>> a= 'fuck'

>>> a
Out[64]: 'fuck'

>>> a.replace('f','d')
Out[66]: 'duck'

>>> a
Out[67]: 'fuck'
```
我们可以看到，调用了 replace() 方法的确使得输出的结果与原字符串不一样，但是原来的字符串看上去好像并没有发生改变；

原因在于，`a` 是一个变量，而这个变量指向的内容是字符串 `'fuck'`（有点像 Java 的感觉），指向的 字符串的内容是不变的，调用 remove() 方法的时候，会临时创建另一个 字符串 作为修改之后的结果并返回

**对于不变对象来说，调用这个对象的任意方法，也不会改变这个对象自身内容**

# 函数
## 自定义函数
```
def FUNC_NAME(PARA1, PARA2, PARA3, ...) :
    [BODY]
    return ...
```
- 记得不要忘记冒号的存在！
- 也可以定义一个空函数：在函数体使用 `pass` 语句（相当于一个占位符）

## 参数检查
调用函数时，参数的**数目**、**类型**必须正确；

如果个数不对的话，解释器会检查出来；但是如果类型不对的话，可能会出现各种各样的错误（尤其是自定义的函数）——所以在自己编写函数的时候，最好进行参数检查）

## 返回多值
是的，Python 是可以返回 “多个值” 的

```
>>> def func(a):
...    return a-1, a-2

>>> func(5)
Out[72]: (4, 3)
```
但本质上，python 返回的仍是单一值，**只不过使用 tuple 将他们捆绑在一起了**

而 Python 的 “多个返回值” 作为 右值（这里借用一下 C++ 的概念）返回的时候，可以**用多个左值来接收**
```
>>> x,y=func(34)

>>> x,y
Out[74]: (33, 32)
```
## 函数参数
Python 的参数可以分为这几种类型：

- 必选参数
- 默认（值）参数
- 可变参数
- 关键字参数

1. 必选参数就是我们平常所正常使用的最普通的参数
2. 默认参数就是一个带有默认值的形参，在调用时，这个形参可以不传入实参——此时就将默认值作为实参；也可以传入实参，此时这个传入的实参将覆盖掉默认值；

    ```
    >>> def power(x,n=2):
    ...    s=1
    ...    while n >= 1 :
    ...        s=s*x
    ...        n=n-1
    ...    return s

    >>> power(3)
    Out[88]: 9

    >>> power(3,7)
    Out[89]: 2187
    ```

    向默认形参传递实参的时候的顺序问题：
    - 按顺序提供实参：即，提供前面的连续若干个实参，后面的默认参数使用默认值
    - 也可以不按顺序提供实参，这样必定会跳过某些默认参数，所以，后面**不按顺序的部分必须加上参数名**

    ```
    >>> def fuck(name='Jackson', age=0, gender='M', marriage='False'):
    ...     print name
    ...     print age
    ...     print gender
    ...     print marriage
    ...     return

    >>> fuck('Stark',45, marriage='True')
    Stark
    45
    M
    True

    >>> fuck('Rogeers',26, 'G')
    Rogeers
    26
    G
    False

    ```
    默认参数的一个很大的坑：如果默认参数的默认值设为可变对象，比如 list 等，那么每次调用这个函数的时候，此时默认参数的实际值就会跟随这个 list 的内容——因为默认参数也可以看成是一个变量，这个变量本身的指向不变，但指向的内容（list 的内容）会发生改变


    引入一个空的不变对象：`None`


3. 可变参数指的是一组数目不定（0或任意有限个）的参数

    使用朴素的方法实现可变参数可以这样做：
    
    - 定义一个接受 tuple 或者 list 的函数
    - 传实参的时候，先组装好一个 list 或者 tuple 再进行传入

    但是 Python 为我们内置了这种功能，而且更为简洁。

    1. 定义：
    
        ```
        def fuck(*operand):
            sum = 0
            for x in operand:
                sum = sum + x
            return sum
        ```
    2. 解释

        可变（形式）参数的定义就是在参数名称之前加上 `*` 号，那么这一组参数就视作可变参数；

        在函数内部，**该参数将被视作一个 tuple**；如果没有实参传入，那么就得到一个空 tuple

    联系一下我们上面提到的朴素方法，如果我们已经有一个能接收可变参数的函数，以及一个 list 或者 tuple，我们应该如何**传实参**？（别说一个一个传）
    
    答案是把 list 或 tuple 的变量名前面加上一个 `*` 符号作为实参传入：

    ```
    >>> lll
    Out[11]: [1, 424, 2, 252, 44, 1, 5, 1, 14, 62]

    >>> fuck(*lll)
    Out[12]: 806
    ```
4. 关键字参数：和可变参数差不多，只不过关键字参数在函数内部会自动组装成一个 tuple，而关键字参数允许读入数目不定（0或任意有限个）的若干个**带参数名的参数值**（配对的 key-value），并在函数内部组装成一个 dict

- 注意，关键字参数的 keyword 必须是字符串

几种参数的组合问题

1. 可以使用这四种参数，也可以使用其中的若干种——共 $2^4=32$ 种组合
2. 但是定义的顺序必须是：
<p align="middle">必选参数 - 默认参数 - 可变参数 - 关键字参数</p>
3. 任何一个函数，都可以使用 `function(*LIST_NAME, **DICT_NAME)` 的方式来调用，前一个参数是拆分一个 list 或者 tuple，后者是拆分一个 dict——当然，前提是 list/tuple 的长度必须**大于等于**必选形参的个数





        





