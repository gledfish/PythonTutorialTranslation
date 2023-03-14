**这篇文章翻译自**[https://www.pythontutorial.net/getting-started/python-hello-world/](https://www.pythontutorial.net/getting-started/python-hello-world/)
---
---
**总览**：在这篇教程，你将学习如何使用 Python 开发第一个程序，程序叫做"Hello, World"
> If you can write “hello world” you can change the world.                                          
**Raghu Venkatesh**

# 创建一个新的 Python 项目

首先，创建一个新的项目，命名为<font color=red> helloworld </font>。

其次，启动 VS Code 然后打开 <font color=red> helloworld</font>。

最后，创建一个新的 app.py 文件，然后输入下面的代码并保存文件。

```python
print('Hello, World!')
```

<font color=red> print() </font> 是一个内置的函数，这个函数在屏幕上展示一段信息。在这个例子中，它展示了信息<font color=red> 'Hello, World!</font>。

## 什么是函数

当你对两个数求和，那便是一个函数。当你将两个数想乘，那也是一个函数。

每一个函数接受你的输入，应用一些规则，然后返回一个结果。

在上面的例子中，<font color=red> print() </font> 是一个函数，它接受一个字符串，并将它展示在屏幕上。

Python 有许多像 <font color=red> print() </font>这样的内置函数，他们可以开箱即用。

此外，Python允许你定义自己的函数，这些你后续会学到。

## 执行 Hello World 程序

要执行<font color=red> app.py </font>，首先启动 Windows 的命令提示符或者 Linux / macOS 上的终端。

接着，跳转到<font color=red> helloworld </font>目录。

在那之后，输入下面的命令行来执行<font color=red> app.py </font>

```bash
python app.py
```

如果你使用的是 macOS 或者 Linux，使用 Python3 命令：

```bash
python3 app.py
```

如果一切都正常，你将会在屏幕上看到下面的信息：

```bash
Hello, World!
```

如果你使用 VS Code，你可以在 VS Code 中启动终端：

* 进入功能表 **Terminal > New Terminal

* 或者使用快捷键<font color=red> Ctrl+Shift+`</font>

通常情况下，键盘上(`)位于<font color=red> ESC </font>。

## Python IDLE

Python IDLE 是 Python 发行版默认的 集成开发环境（IDE）。

Python IDLE 也被称为一个交互式解释器。它有许多的特征，例如：

* 带有语法高亮的代码编辑

* 智能缩进

* 和自动补全

简而言之，Python IDLE 帮助你用一种不断尝试和犯错的方法快速的试验 Python。

下面的步骤展示了如何一步一步的启动 Python IDLE 并执行 Python 代码：

首先，启动 Python IDLE 程序：

![Python-Hello-World-Launch-IDLE.png](https://s2.loli.net/2023/03/14/Cbo2OuktywJ8SKN.png)

一个新的 Python Shell 窗口将会像下面这样展示：

![Python-Hello-World-IDLE.png](https://s2.loli.net/2023/03/14/45VHCxscpAT68dm.png)

现在，你可以在 >>> 后面输入 Python 代码然后摁<font color=red> Enter </font> 执行它。

例如：你可以输入代码<font color=red> print('Hello, World!') </font> 然后摁 <font color=red> Enter </font>，你将会看见信息 "Hello, World!" 立即出现在屏幕上：

![Python-Hello-World-Executing-code.png](https://s2.loli.net/2023/03/14/zGTQIgN6ZCcOS5u.png)

## 总结
* 在 Windows 的命令行或者 macOS/Linux 的终端上使用 <font color=red> python app.py </font> 命令执行<font color=red> app.py </font> 文件。

* 使用<font color=red> print() </font>函数在屏幕上展示信息。

* 使用 Python IDLE 输入 Python 代码并立即执行。











(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  

我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
