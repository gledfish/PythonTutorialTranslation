**这篇文章翻译自**[https://www.pythontutorial.net/python-basics/python-map-list/](https://www.pythontutorial.net/python-basics/python-map-list/)
---
---

# 如何使用 map() 函数转换列表对象

**摘要**：在本教程中，你将学习在列表中如何使用map() 函数。

## map() 函数 函数的介绍

当处理一个列表（或元组）时，你经常需要转换列表中的元素，并返回一个包含转换后的元素的新列表。

假设，你想把下面<font color=red> bonuses </font>列表中的每个数字都加倍。

```python
bonuses = [100, 200, 300]
```

要做到这一点，你可以使用for循环来迭代元素，将每个元素加倍，然后像下面这样将其添加到一个新的列表中。

```python
bonuses = [100, 200, 300]

new_bonuses = []

for bonus in bonuses:
    new_bonuses.append(bonus * 2)

print(new_bonuses)
```

输出：

```bash
[200, 400, 600]
```

Python 提供了一种更好的方法来完成这种任务————使用 <font color=red> map() </font> 内置函数。

<font color=red> map() </font>函数遍历一个列表（或一个元组）中的所有元素，对每个元素应用一个函数，并返回一个新的元素的迭代器。

下面是<font color=red> map() </font>函数的基本语法。

```python
iterator = map(fn, list)
```

在这个语法中， <font color=red> fn </font> 是函数的名称，将在列表的每个元素上调用。

事实上，你可以向 <font color=red> map() </font> 函数传递任何可迭代对象，而不仅仅是一个列表或元组。

回到前面的例子，要使用 <font color=red> map() </font> 函数，先定义一个将奖金加倍的函数，然后像下面这样使用map()函数：

```python

def double(bouns):
    return bonus * 2

bonuses = [100, 200, 300]

iterator = map(double, bonuses)
```

或者通过使用像这样的 lambda 表达式使这段代码更加简洁：

```python
bonuses = [100, 200, 300]
iterator = map(lambda bonus: bonus * 2, bonuses)
```

一旦你有了一个迭代器，你就可以用<font color=red> for </font> 循环来迭代新元素。

或者使用<font color=red> list() </font> 函数将一个迭代器转换为一个列表。

```python
bounses = [100, 200, 300]
iterator = map(lambda bonus: bonus*2, bonuses)
print(list(iterator))

```

## 更多关于Python map()函数与列表的例子

让我们再举几个在列表中使用 Python map() 函数的例子。

### 1）对一个字符串列表使用 map() 函数
下面的例子使用 map() 函数来返回一个新的列表，其中每个元素都被转换为适当的情况。
```python
names = ['david', 'peter', 'jenifer']
new_names = map(lambda name: name.capitalize(), names)
print(list(new_names))

```

输出：

```bash
['David', 'Peter', 'Jenifer']
```

### 2) 使用 map() 函数对一个元组列表进行处理

假设你有以下购物清单，表示为一个元组的列表。

```python
carts = [['SmartPhone', 400],
         ['Tablet', 450],
         ['Laptop', 700]]
```

你需要计算每个产品的税额，税额为 10%。此外，你需要将税额添加到列表中每个项目的第三个元素中。

返回列表应该是这样的：
```bash
[['SmartPhone', 400, 40.0],
['Tablet', 450, 45.0],
['Laptop', 700, 70.0]]
```

为了做到这一点，你可以使用map()函数来创建一个新的列表元素，并像这样把新的税额添加到每个元素中：

```python
carts = [['SmartPhone', 400],
         ['Tablet', 450],
         ['Laptop', 700]]

TAX = 0.1
carts = map(lambda item: [item[0], item[1], item[1] * TAX], carts)

print(list(carts))
```

## 总结
* 使用 map() 函数在一个列表的每一个项目上调用一个函数，并返回一个迭代器。



(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  

我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
