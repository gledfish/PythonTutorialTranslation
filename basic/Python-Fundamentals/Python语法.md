**这篇文章翻译自**[https://www.pythontutorial.net/python-basics/python-syntax/](https://www.pythontutorial.net/python-basics/python-syntax/)
---
---
# Python语法

**总览**：在这篇教程，你将学习基础的 Python 语法，这样就能快速上手 Python 语言。

## 空格和缩进

如果你已经使用过别的编程语言，像 Java，C#，或者 C/C++，你知道这些语言使用（;）来分开语句。

然而，Python 使用空格和缩进来构建代码结构。

下面展示了 Python 代码的语法：

# 定义 main 函数打印一些东西

```python
def main():
    i = 1
    max = 10
    while( i < max):
        print(i)
        i = i + 1

# 调用 main 函数
```

代码的含义现在对你不重要，请关注代码结构。

在每一行的末尾，你没有看见任何结束语句的分号。并且 Python 使用缩进来格式化代码。

通过使用缩进和空格来组织代码，Python 代码获得了下面的优势：

* 首先，你不会错过代码块的开始和结束，像别的编程语言（ 如 Java 或者 C# ）那样。

* 其次，代码风格极其统一，如果你想要维护别的开发者的代码，代码看起来就跟你的一样。

* 最后，与其他语言相比，Python 代码更为可读且清晰。

## 注释

代码注释和代码一样重要，因为它们描述了一段代码为什么被写。

当 Python 解释器执行代码时，它会忽略注释。

在 Python 中，一个单行注释以一个（#）开头，后面紧跟一句注释。例如

```python
# This is a single line comment in Python
```

Python 也支持其他类型的代码。

## 连续的语句

Python 使用一个换行符来分开语句，它将每一条语句放在一行。

然而，一条长语句可以使用反斜杠（\）涵盖多行。

下面的例子展示了如何使用反斜杠（\）在第二行延续一条语句。

```python
if (a == True) and (b == False) and \
   (c == True):
    print("Continuation of statements")
```

## 标识符

标识符是一些名称，用来标识变量，函数，模组，类和 Python 中的其他对象。

标识符需要以字母或者下划线开始。后面的字符可以是字母，数字，下划线。

Python 标识符是区分大小写的。例如，<font color=red> counter </font> 和 <font color=red> Counter </font>是不同的标识符。

除此之外，你不能使用 Python 的关键字来明名标识符。

## 关键字

一些单词在 Python 中有特殊的意义。他们被称为关键字。

下面展示了一系列 Python 的关键字：

```python
False      class      finally    is         return
None       continue   for        lambda     try
True       def        from       nonlocal   while
and        del        global     not        with
as         elif       if         or         yield
assert     else       import     pass
break      except     in         raise
```

Python 是一个不断发展和进步的语言。所以它的关键字会不断增加和改变。

Python提供了一个特殊的模块————keyword，列出了它的关键字。

要找出当前的关键字列表，你可以使用下面的代码：

```python
import keyword

print(keyword.kwlist)
```

## 字符串常量

Python 使用单引号（'），双引号（"），三个单引号（'''）和三双引号来表示一个字符串常量。

字符串常量需要被相同类型的引号包裹起来。例如，如果你使用一个单引号开始一个字符串常量，你需要使用相同的单引号来结束它。

下面展示了一些字符串常量的例子：

```python
s = 'This is a string'
print(s)
s = "Another string using double quotes"
print(s)
s = ''' string can span
        multiple line '''
print(s)
```

## 总结

* 一个 Python 语句以一个换行符结尾。

* Python使用空格和缩进来组织它的代码结构。

* 标识符是一些名称，用来标识变量，函数，模组，类和 Python 中的其他对象。

* 代码注释描述了代码为什么工作，他们被 Python 解释器忽略。

* 使用单引号，双引号，三个引号，或者三个双引号来表示字符串。

















(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  

我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
