**这篇文章翻译自**[https://www.pythontutorial.net/python-basics/python-iterables/](https://www.pythontutorial.net/python-basics/python-iterables/)
---
---

# Python 可迭代对象

简介：在这篇教程，你将学习 Python 可迭代对象和迭代器

## Python 迭代器简介

在 Python 中，可迭代对象是包含零个、一个或多个元素的对象。可迭代对象能够一次返回一个元素。

由于这个功能，你可以使用<font color=red> for </font> 循环迭代可迭代对象。

事实上，<font color=red> range() </font>函数是一个可迭代对象，因为你可以迭代它的结果：

```python
for index in range(3):
    print(index)
```

输出：

```bash
0

1

2
```

此外，字符串是可迭代的，因为您可以使用 for 循环对其进行迭代：

```python
str = 'Iterables'
for ch in str:
    print(ch)

```

列表和元组也是可迭代对象，因为您可以遍历它们。例如：

```python
ranks = ['high', 'medium', 'low']

for rank in ranks:
    print(rank)
```

根据经验来看，如果你可以循环某个东西，那它就是可迭代的。

## 什么是迭代器

一个可迭代对象可以被迭代。迭代器是执行迭代的代理。

要从可迭代对象中获取迭代器，可以使用<font color=red> iter() </font>函数。例如：

```python
colors = ['red', 'green', 'blue']
colors_iter = iter(colors)
```

一旦有了迭代器，就可以使用 next() 函数从可迭代对象中获取下一个元素：

```python
colors = ['red', 'green', 'blue']
colors_iter = iter(colors)

color = next(colors_iter)
print(color)
```

输出：

```bash
red 
```

每次调用 next() 函数时，它都会返回可迭代对象中的下一个元素。例如：
```python
colors = ['red', 'green', 'blue']
colors_iter = iter(colors)

color = next(colors_iter)
print(color)

color = next(colors_iter)
print(color)

color = next(colors_iter)
print(color)
```

输出：

```bash
red

green

blue
```

调用<font color=red> next() </font>函数时，如果迭代器没有更多元素，你将得到一个异常。

```python
colors = ['red', 'green', 'blue']
colors_iter = iter(colors)

color = next(colors_iter)
print(color)

color = next(colors_iter)
print(color)

color = next(colors_iter)
print(color)

# cause an excpetion
color = next(colors_iter)
print(color)
```

此示例首先显示颜色列表的三个元素，然后发出异常：

```bash
red
green
blue
Traceback (most recent call last):
  File "iterable.py", line 15, in <module>
    color = next(colors_iter)
StopIteration
```
迭代器是状态性的，这意味着一旦你迭代了一个元素，这个元素就从迭代器中消失了。

换句话说，一旦你完成了迭代器的循环，迭代器就变成了空的。如果你再次迭代它，它什么也不会返回。

因为你可以在一个迭代器上进行迭代，所以迭代器也是一个可迭代的对象。这是相当令人困惑的。比如说：

```python
colors = ['red', 'green', 'blue']
iterator = iter(colors)

for color in iterator:
    print(color)
```

输出：

```bash
red

green

blue
```

如果你调用<font color=red> iter() </font>函数并向其传递一个迭代器，它将返回相同的迭代器。

稍后，你将学习如何创建迭代表。

## 总结
* 一个可迭代对象是一个可以被迭代的对象，它能够一次返回其中的一个元素。

* 迭代器是一个执行迭代的代理。它是有状态的。而迭代器也是一个可迭代的对象。

* 使用<font Color=red> iter() </font>函数从一个可迭代对象中获得一个迭代器，使用next()函数从可迭代对象中获得下一个元素。

(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  

我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
