**这篇文章翻译自**[https://www.pythontutorial.net/python-basics/python-__name__/](https://www.pythontutorial.net/python-basics/python-__name__/)
---
---
# Python ```__name__```

**摘要**：在本教程中，你将学习Python的```__name__```变量，以及如何在模块中有效地使用它。

## 什么是Python ```__name__``` ?

如果你阅读过Python代码，你很可能见过下面这样的 ```__name__``` 变量。

```python
if __name__ == '__main__':
    main()
```

你可能想知道 ```__name__``` 这个变量是什么。
 
由于 ```__name__``` 变量两边都有双下划线，所以它被称为 **dunder** 命名 。dunder代表的是双下划线。

```__name__``` 是 Python 中的一个特殊变量。它的特殊之处在于，Python 根据其包含的脚本的执行方式，给它分配了不同的值。

当你导入一个模块时，Python 会执行与该模块相关的文件。

通常，你想写一个可以直接执行的脚本，或者作为一个模块导入。 ```__name__``` 变量允许你这样做。

当你直接运行脚本时，Python将 `__name__` 变量设置为 `'__main__'` 。

然而，如果你把一个文件作为模块导入，Python 会把模块名称设置为 `__name__` 变量。

## Python `__name__` 变量示例

首先，创建一个名为 **billing** 的新模块，有两个函数。 此外，添加一条语句，将 __name__ 变量打印到屏幕上。

```python
def calculate_tax(price, tax):
    return price * tax


def print_billing_doc():
    tax_rate = 0.1
    products = [{'name': 'Book',  'price': 30},
                {'name': 'Pen', 'price': 5}]

    # print billing header
    print(f'Name\tPrice\tTax')

    # print the billing item
    for product in products:
        tax = calculate_tax(product['price'], tax_rate)
        print(f"{product['name']}\t{product['price']}\t{tax}")


print(__name__)
```

然后创建一个名为 app.py 的新文件并导入 billing 模块。
```python
import billing
```

当你执行<font color=red> appp.py </font>：
```bash
> python app.py
```

`__name__` 变量显示以下数值。
```bash 
billing
```
这意味着当你把 billing 模块导入到 <font color=red> app.py </font> 文件时，Python 确实执行了 <font color=red> billing.py </font>文件。

在 <font color=red> app.py </font> 中的 `__name__` 变量设置为模块名称，即<font color=red> billing </font>。

如果你直接将<font color=red> billing.py </font>作为脚本执行。
```bash
python billing.py
```

...你会看到以下输出。
```bash
__main__
```

在这种情况下， `__name__` 变量的值在<font color=red> billing.py </font>里面是 `'__main__'` 。

![Python-__name__.png](https://s2.loli.net/2023/03/20/F7DZV3dW6awcpN5.png)

因此， `__name__` 变量允许你检查文件是直接执行还是作为模块导入。

例如，为了在<font color=red> billing.py </font>直接作为脚本执行时执行<font color=red> print_billing_doc() </font>函数，你可以在<font color=red> billing.py </font>模块中加入以下语句。
```python
if __name__ == '__main__':
    print_billing_doc()
```

第三，以脚本的形式执行 <font color=red> billing.py </font> ，你会看到以下输出。
```bash
Name    Price   Tax
Book    30      3.0
Pen     5       0.5
```

然而，当你执行<font color=red> app.py </font>时，你不会看到<font color=red> if </font>代码块被执行，因为 `__name__` 变量没有设置为 `'__main__'` ，而是<font color=red> 'billing' </font> 。

## 总结

当你直接运行 Python 脚本时，Python 将 `'__main__'` 赋值给 `__name__` 变量，如果你将脚本作为模块导入，则 Python 将模块名称赋值给 `__name__`变量。
(全文完)

部分图片来自于源网站，侵删。

鉴于本人才疏学浅，翻译难免有所疏漏，如果有任何问题欢迎随时联系我进行批评指正：2076577077@qq.com  


我是gled fish, [点击这里来到我的博客网站：](https://gledfish.netlify.app/)
---
---
转载请注明译者和原出处，请勿用于任何商业用途。
