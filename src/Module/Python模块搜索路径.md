**这篇文章翻译自**[https://www.pythontutorial.net/python-basics/python-module-search-path/](https://www.pythontutorial.net/python-basics/python-module-search-path/)
---
---
# Python 模块搜索路径

**摘要**：在本教程中，你将学习当你在 Python 程序中导入一个模块时，模块搜索路径是怎样的。

## Python模块搜索路径的介绍

当你在一个程序中导入一个模块时：

```python
import module
```

Python将从以下来源搜索<font color=red> module.py </font> 文件。

* 被执行程序所在的文件夹。

* 在 PYTHONPATH 环境变量中指定的文件夹列表（如果你之前设置了它）

* 你在安装 Python 时配置的安装依赖（installation-dependen）文件夹列表

Python将产生的搜索路径存储在来自 <font color=red> sys </font> 模块的<font color=red> sys.path </font>变量中。

下面的程序显示了当前的模块搜索路径。

```python
import sys

for path in sys.path:
    print(path)

```

下面是在 Windows 上的输出样例。

```bash
D:\Python\
C:\Program Files\Python38\python38.zip
C:\Program Files\Python38\DLLs
C:\Program Files\Python38\lib
C:\Program Files\Python38
C:\Users\PythonTutorial\AppData\Roaming\Python\Python38\site-packages
C:\Program Files\Python38\lib\site-packages 
```

以下是 Linux 上的输出样例。

```bash
/Library/Frameworks/Python.framework/Versions/3.8/bin
/Library/Frameworks/Python.framework/Versions/3.8/lib/python38.zip 
/Library/Frameworks/Python.framework/Versions/3.8/lib/python3.8
/Library/Frameworks/Python.framework/Versions/3.8/lib/python3.8/lib-dynload
/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.8/site-packages
```

为了确保Python能够找到<font color=red> module.py </font>，你需要：

* 将 <font color=red> module.py </font> 放在被执行程序的文件夹中。
  
* 在<font color=red> PYTHONPATH </font>环境变量中包括包含 <font color=red> module.py </font> 的文件夹。或者你可以把 <font color=red> module.py </font> 放在包含在<font color=red> PYTHONPATH </font>变量中的一个文件夹中。

* 将 <font color=red> module.py </font> 放入一个依赖安装的文件夹中。

## 在运行时修改Python模块的搜索路径

Python 允许你在运行时通过修改 <font color=red> sys.path </font> 变量来修改模块搜索路径。这允许你将模块文件存储在你选择的任何文件夹中。

由于 <font color=red> sys.path </font> 是一个列表，你可以在它后面附加一个搜索路径。

下面的例子将<font color=red> d:\modules </font>添加到搜索路径，并使用存储在该文件夹中的<font color=red> recruitment </font> 模块。

```python
>>> import sys
>>> sys.path.append('d:\\modules\\')
>>> import recruitment
>>> recruitment.hire()
Hire a new employee...
```

## 总结

* 当你导入一个模块时，Python 将从 <font color=red> sys.path </font> 变量中指定的文件夹中搜索模块文件。
  
* Python 允许你通过改变、增加和删除 <font color=red> sys.path </font>变量中的元素来修改模块搜索路径。
(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  

我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
