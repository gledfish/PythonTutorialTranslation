**这篇文章翻译自**[https://www.pythontutorial.net/python-basics/python-pass/](https://www.pythontutorial.net/python-basics/python-pass/)
---
---

# Python pass

**总览**：在本教程中，你将学习如何使用 Python <font> pass </font>语句作为占位符。

## Python pass 语句介绍

假设你有以下 <font color=blue> if...else </font>语句：

```python

counter = 1
max = 10
if counter <= max:
    counter += 1
else:
    # 后面执行的语句
```

在 <font color=red> else </font>子句中，你还没有任何代码。但是稍后你将为该<font  color=red> else </font>子句编写代码。

在这种情况下，如果你运行代码，你将收到一个语法错误 ( <font color=red> SyntaxError </font>)。

这便是 Python<font color=red> pass </font>语句起作用的地方：

```python
counter = 1
max = 10
if counter <= max:
    counter += 1
else:
    pass
```

该pass语句什么也没做。它仅仅是你将来写的代码的占位符。

当您运行包含<font color=red> pass </font>语句的代码时，Python 解释器会将<font color=red> pass </font>语句视为单个语句。因此，它不会发出语法错误。

实际上，您可以在 Python 的许多语句中使用<font color=red> pass </font>语句。

让我们举一些使用<font color=red> pass </font>语句的例子。

## 1）在 if 语句中使用 pass 语句的例子

下面展示了如何在<font color=red> if </font>语句中使用<font color=red> pass </font>语句：
```python

if condition:
    pass

```

## 2）在 for 语句中使用 pass 语句

这个例子展示了如何在<font color=blue> for </font>循环中使用<font color=red> pass </font>语句：
```python
for i in range(1,100):
    pass

```

## 3）在 while 语句中使用 pass 语句

下面的例子展示了如何在<font color=blue> while </font>循环中使用<font color=red> pass </font>语句：
```python

while condition:
    pass
```

## 4）在函数和类中使用 pass 语句
在后面的章节中，您将学习如何定义<font color=blue> 函数 </font>：

```python
def fn():
    pass

```

和一个类：
```python
class Stream:
    pass

```

在这些例子中，您使用<font color=red> pass </font>语句将函数和类的内容标记为空。

## 总结

* 使用<font color=red> pass </font>语句为稍后要完成的代码创建一个占位符。

(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  

我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
