# 什么是数据科学

    数据科学是关于通过探索，预测和推论从大量且多样的数据中得出有用的结论

    探索：发现信息中的模式

    预测：使用已知信息去作出有根据的猜测

    推论：包括量化确认度：我们的预测有多精确、我们在数据中发现的模式是否也会出现在新观察中？

    工具

- 对于探索，有描述性统计学、可视化

- 对于预测，有机器学习与优化

- 对于推论，有统计测试和模型

## 运算工具

    本书采用python3及其一些数据可视化工具

## 统计技术

    统计的最重要贡献之一是描述观察和结论之间关系的一致且精确的词汇。

    本文涉及到以下问题：测试假设，估计置信度和预测未知数量等

# 因果和实验

## 概念

实验和结果之间的任何关系被称为**关联**。如果实验导致结果发生，那么这个关联是**因果关系**。

## 实验组和对照组

科学家使用比较来确定实验与结果之间的关联，即实验和结果之间存在联系。他们比较了一组接受实验的个体（**实验组**）的结果，和一组没有接受实验的个体的结果（**对照组**）。

## 混淆

在一项观察研究中，如果实验组和对照组在实验以外的方面有所不同，则很难对因果关系作出结论。 两组之间在**实验以外**的根本区别被称为**混淆因素**，因为当你试图得出结论时，它可能会混淆你。

## 随机化

**避免混淆**的一个很好的方法是，将个体随机分配到实验和对照组，然后将实验给予分配到实验组的人。随机化使两组除了实验之外都相似。如果你能够将个体随机分为实验组和对照组，则你正在进行一项**随机对照试验**（RCT）

有时候，人们在实验中的反应会受到他们知道他们在哪个群体的影响。所以你可能希望进行**盲法实验**，其中个体不知道他们是在实验组还是对照组。为了使它有效，你必须把安慰剂给控制组，这是一种和实验看起来完全一样的东西，但实际上没有效果。

在某些情况下，即使目标是调查因果关系，也不可能进行随机对照实验。

随机化的优点是

- 它使我们能够以数学方式，计算随机化产生实验和对照组的可能性。

- 它使我们能够对实验组和对照组之间的差异作出**精确的数学表述**。这反过来帮助我们对实验是否有效作出正确的结论。

## 因果关系

因果关系的建立往往分两个阶段进行。首先，观察一个关联。接下来，更仔细的分析是否存在因果关系。

## 总结

在本课程中，你将学习如何进行和分析你自己的随机实验。这将涉及比本节更多的细节。

**目前，只需关注主要思想：尝试建立因果关系，如果可能，进行随机对照实验。**

注意：如果你正在进行一项观察研究，你可能能够建立联系而不是因果关系。在根据观察研究得出因果关系的结论之前，要非常小心混淆因素。

    

# Python编程

## 运算符

| 表达式类型 | 运算符     | 示例         | 值       |
|:-----:|:-------:|:----------:|:-------:|
| 加法    | `+`     | `2 + 3`    | 5       |
| 减法    | `-`     | `2 - 3`    | -1      |
| 乘法    | `*`     | `2 * 3`    | 6       |
| 除法    | `/`     | `7 / 3`    | 2.66667 |
| 取余    | `%`     | `7 % 3`    | 1       |
| 指数    | `**`    | `2 ** 0.5` | 1.41421 |
| 括号    | （）[] {} |            |         |

## 数值

整数在 Python 语言中称为`int`值。 它们只能表示没有小数部分的整数（负数，零或正数）

实数在 Python 语言中被称为`float`值（或浮点值）。 他们可以表示全部或部分数字，但有一些限制。

当一个`float`值和一个`int`值，通过算术运算符组合在一起时，结果总是一个`float`值。

在大多数情况下，两个整数的组合形成另一个整数，但任何数字（`int`或`float`）除以另一个将是一个`float`值。

浮点数只能表示任何数字的 15 或 16 位有效数字；剩下的精度就会丢失。 如果一个计算的结果是一个非常大的数字，那么它被表示为无限大。 如果结果是非常小的数字，则表示为零。

## 名称

名称通过赋值语句在 Python 中得到一个值。 在赋值中，名称后面是`=`，再后面是任何表达式。 `=`右边的表达式的值被赋给名称。

名称必须以字母开头，但可以包含字母和数字。 名称不能包含空格；相反，通常使用下划线字符`_`来替换每个空格

## 函数

一些函数默认是可用的，比如`abs`和`round`，但是大部分内置于 Python 语言的函数都存储在一个称为模块的函数集合中。**导入语句用于访问模块**，如`math`或`operator`。

```py
import math
import operator
math.sqrt(operator.add(4, 5))
3.0
```

## 类型

每个值都有一个类型，内建的`type`函数返回任何表达式的结果的类型

## 字符串

单引号和双引号都可以用来创建字符串：`'hi'`和`"hi"`是相同的表达式。 双引号通常是首选，因为它们允许在字符串中包含单引号。

字符串也有一些方法，例如replace、upper

```py
"loud".upper()
'LOUD'
'hitchhiker'.replace('hi', 'ma')
'matchmaker'
s = "train"
t = s.replace('t', 'ing')
u = t.replace('in', 'de')
u
'degrade'
```

## 比较运算符

一个表达式可以包含多个比较

| 比较   | 运算符  | True 示例  | False 示例 |
| ---- | ---- | -------- | -------- |
| 小于   | `<`  | `2 < 3`  | `<`      |
| 大于   | `>`  | `3 > 2`  | `>`      |
| 小于等于 | `<=` | `<=`     | `3 <= 2` |
| 大于等于 | `>=` | `>=`     | `2 >= 3` |
| 等于   | `==` | `==`     | `3 == 2` |
| 不等于  | `!=` | `3 != 2` | `!=`     |

## 集合

Python 中有很多种类的集合，我们在这门课中主要使用数组。

在几个值上调用`make_array`函数，将它们放到一个数组中，这是一种顺序集合。

集合允许我们使用单个名称，将多个值传递给一个函数。 例如，`sum`函数计算集合中所有值的和，`len`函数计算其长度。

## 数组

`make_array`函数可以用来创建数值的数组。

数组也可以包含字符串或其他类型的值，但是**单个数组只能包含单一类型的数据。**

```py
english_parts_of_speech = make_array("noun", "pronoun", "verb", "adverb", "adjective", "conjunction", "preposition", "interjection")
```

数组可以用在算术表达式中来计算其内容。 当数组与单个数组合时，该数与数组的每个元素组合。

```py
(9/5) * highs + 32
array([ 56.48  ,  57.8966,  58.253 ,  59.2952])
```

数组也有方法，这些方法是操作数组值的函数。

```py
highs.size
4
highs.sum()
57.736000000000004
highs.mean()
14.434000000000001
```

## 数组上的函数

`numpy`包，在程序中缩写为`np`，为 Python 程序员提供了创建和操作数组的，方便而强大的函数。

```py
import numpy as np
```

每个这些函数接受数组作为参数，并返回单个值。

| 函数                 | 描述                    |
| ------------------ | --------------------- |
| `np.prod`          | 将所有元素相乘               |
| `np.sum`           | 将所有元素相加               |
| `np.all`           | 测试是否所有元素是真值 （非零数值是真值） |
| `np.any`           | 测试是否任意元素是真值（非零数值是真值）  |
| `np.count_nonzero` | 计算非零元素的数量             |

每个这些函数接受字符串数组作为参数，并返回数组。

| 函数                  | 描述                    |
| ------------------- | --------------------- |
| `np.char.lower`     | 将每个元素变成小写             |
| `np.char.upper`     | 将每个元素变成大写             |
| `np.char.strip`     | 移除每个元素开头或末尾的空格        |
| `np.char.isalpha`   | 每个元素是否只含有字母（没有数字或者符号） |
| `np.char.isnumeric` | 每个元素是否只含有数字（没有字母）     |

每个这些函数接受字符串数组和一个搜索字符串。

| 函数                 | 描述                    |
| ------------------ | --------------------- |
| np.char.count      | 在数组的元素中，计算搜索字符串的出现次数  |
| np.char.find       | 在每个元素中，搜索字符串的首次出现位置   |
| np.char.rfind      | 在每个元素中，搜索字符串的最后一次出现位置 |
| np.char.startswith | 每个字符串是否以搜索字符串起始       |

## 范围

范围是一个数组，按照递增或递减的顺序排列，每个元素按照一定的间隔分开。

范围使用`np.arange`函数来定义，该函数接受一个，两个或三个参数：起始值，终止值和“步长”。

如果将一个参数传递给`np.arange`，那么它将成为终止值，其中`start = 0`，`step = 1`。 两个参数提供了起始值和终止值，`step = 1`。 三个参数明确地提供了起始值，终止值和步长。

**范围始终包含其`start`值，但不包括其`end`值。 它按照`step`计数，并在到达`end`之前停止。**

```py
np.arange(5)
array([0, 1, 2, 3, 4])

np.arange(3, 9)
array([3, 4, 5, 6, 7, 8])

np.arange(3, 30, 5)
array([ 3,  8, 13, 18, 23, 28])


np.arange(1.5, -2, -0.5)
array([ 1.5,  1. ,  0.5,  0. , -0.5, -1. , -1.5])
```

# 表格

## 模块导入

```py
from datascience import *
```

## 创建表格

创建一个新的空表格

```py
Table()
```

`with_columns`方法将新列添加到表中

```py
Table().with_columns('XXX', make_array(8, 34, 5))

Table().with_columns(
    'Number of petals', make_array(8, 34, 5),
    'Name', make_array('lotus', 'sunflower', 'rose'))

flowers = Table().with_columns(
    'Number of petals', make_array(8, 34, 5),
    'Name', make_array('lotus', 'sunflower', 'rose')
)

flowers.with_columns(
    'Color', make_array('pink', 'yellow', 'red')
)
```

通过使用`Table`的`read_table`方法读入CSV文件创建表格

```python
minard = Table.read_table('minard.csv')
minard
```

## 列的选取

`show`展示行，允许我们指定行数，缺省值（没有指定）是表的所有行。

```py
nba_salaries.show(3)
```

通过使用`relabeled`修改列标签。这会创建新的表格，并保留原表格不变。 

```python
minard.relabeled('City', 'City Name')
```

查看表格中列的数量、行的数量

```py
minard.num_columns
5
minard.num_rows
8
```

访问表格中某一列数组，参数为列名或列下标

列下标从0开始

```py
minard.column('Survivors')
array([145000, 140000, 127100, 100000,  55000,  24000,  20000,  12000])

minard.column(4)
array([145000, 140000, 127100, 100000,  55000,  24000,  20000,  12000])
```

访问列的某一条目

```py
minard.column(4).item(0)
145000
minard.column(4).item(5)
24000
```

用选项`PercentFormatter`调用`set_format`方法，使得列中的比例显示为百分比

```py
minard.set_format('Percent Surviving', PercentFormatter)
```

`select`方法创建一个新表，仅仅包含指定的列

```py
minard.select('Longitude', 'Latitude')
minard.select(0, 1)
```

另一种创建新表，包含列集合的方式，是`drop`你不想要的列。

```py
minard.drop('Longitude', 'Latitude', 'Direction')
```

## 行的选取

take()方法指定行，可以传入单个索引，也可以传入一系列索引

```py
nba.take(0)
nba.take(np.arange(3, 6)) //选取第4、5、6行
```

where选取具有指定特征的行，特征由are指定

`where`的第一个参数是列标签，`where`的第二个参数是用于指定特征的方式。

它的输出是一个表格，列与原始表格相同，但只有特征出现的行。

通过重复使用`where`，你可以访问具有多个指定特征的行

```py
original_table_name.where(column_label_string, are.condition)

nba.where('POSITION', 'PG').where('SALARY', are.above(15))
```

这里有一些谓词，你可能会觉得有用。 请注意，`x`和`y`是数字，`STRING`是一个字符串，`Z`是数字或字符串；你必须指定这些，取决于你想要的特征

| 谓词                              | 描述              |
| ------------------------------- | --------------- |
| `are.equal_to(Z)`               | 等于`Z`           |
| `are.above(x)`                  | 大于`x`           |
| `are.above_or_equal_to(x)`      | 大于等于`x`         |
| `are.below(x)`                  | 小于`x`           |
| `are.below_or_equal_to(x)`      | 小于等于`x`         |
| `are.between(x, y)`             | 大于等于`x`，小于`y`   |
| `are.strictly_between(x, y)`    | 大于`x`，小于`y`     |
| `are.between_or_equal_to(x, y)` | 大于等于`x`，小于等于`y` |
| `are.containing(S)`             | 包含字符串`S`        |

| 谓词                    | 描述     |
| --------------------- | ------ |
| `are.not_equal_to(Z)` | 不等于`Z` |
| `are.not_above(x)`    | 不大于`x` |

## 对行排序

`sort`的参数是列标签或索引，默认升序

参数descending=True表示降序

```py
nba_salaries.sort('PLAYER')
nba.sort('SALARY', descending=True)
```

# 可视化

定量：拥有数值的变量，也称数值变量

## 散点图

散点图展示两个数值变量之间的关系

`Table`的`scatter`方法绘制一个散点图，由表格的每一行组成。它的第一个参数是要在横轴上绘制的列标签，第二个参数是纵轴上的列标签。

```py
actors.scatter('Number of Movies', 'Total Gross')


no_outlier = actors.where('Number of Movies', are.above(10))
no_outlier.scatter('Number of Movies', 'Average per Movie')
```

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-10-27.png)

## 线形图

线形图是最常见的可视化图形之一，通常用于研究时序型的趋势和模式。

`Table`的`plot`方法产生线形图。 它的两个参数与散点图相同：首先是横轴上的列，然后是纵轴上的列

```python
century_21.plot('Year', 'Number of Movies')
```

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-14-05.png)

## 分布表

 分布表，列包括分布变量、每个变量的频率

| Flavor     | Number of Cartons |
| ---------- | ----------------- |
| Chocolate  | 16                |
| Strawberry | 5                 |
| Vanilla    | 9                 |

分类变量“口味”的值是巧克力，草莓和香草。 表格显示了每种口味的纸盒数量。

如何生成分布表？`Table`的`group`方法为我们计算分布变量不同的值出现在表中的频率，生成分布表

```py
movies_and_studios.group('Studio')
```

## 条形图

分布表，列包括分布变量、每个变量的频率

| Flavor     | Number of Cartons |
| ---------- | ----------------- |
| Chocolate  | 16                |
| Strawberry | 5                 |
| Vanilla    | 9                 |

分类变量“口味”的值是巧克力，草莓和香草。 表格显示了每种口味的纸盒数量。

条形图是可视化类别分布的熟悉方式。 它为每个类别显示一个条形。 条形的间隔相等，宽度相同。 每个条形的长度与相应类别的频率成正比。

我们使用横条绘制条形图，因为这样更容易标注条形图。 所以`Table`的方法称为`barh`。 它有两个参数：第一个是类别的列标签，第二个是频率的列标签。

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-17-37.png)

除了纯粹的视觉差异之外，条形图和我们在前面章节中看到的两个图表之间还有一个重要的区别。 它们是散点图和线图，两者都显示两个数值变量 - 两个轴上的变量都是数值型的。 相比之下，条形图的一个轴上是类别，在另一个轴上具有数值型频率，这对图表有影响。

## 频率分布直方图

在直角坐标系中，用横轴表示随机变量的取值，横轴上的每个小区间对应一个组的组距，作为小矩形的底边；纵轴表示频率(组频数/总频数=频率)，并用它作小矩形的高，以这种小矩形构成的一组图称为频率直方图。

在直角坐标系中，用横轴表示随机变量的取值，横轴上的每个小区间对应一个组的组距，作为小矩形的底边；纵轴表示频率密度(频率/组距)，并用它作小矩形的高，以这种小矩形构成的一组图称为频率分布直方图（hist）。

在频率分布直方图中，每个小矩形的面积等于相应桶中数值数量占总数量的百分比。所有小矩形的面积“总计为 1”。

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-44-57.png)

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-45-17.png)

hist方法生成列中值的直方图。 可选的单位参数用于两个轴上的标签。 直方图显示数值的分布

将横轴划分成了若干个区间，每个区间称为“bin”，也称为桶。`bin`包含左端点的数据，但不包含右端点的数据。我们使用符号`[a, b)`表示从`a`开始并在`b`结束但不包括`b`的桶。

```py
millions.hist('Adjusted Gross', unit="Million Dollars")
```

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-27-44.png)

可选参数`bins`可以与`hist`一起使用来指定桶的端点。它必须由一系列数字组成，这些数字以第一个桶的左端开始，以最后一个桶的右端结束。我们首先将桶中的数字设置为`300,400,500`等等，以`2000`结尾。

```py
millions.hist('Adjusted Gross', bins=np.arange(300,2001,100), unit="Million Dollars")
```

可以使用`bin`方法从一个表格中计算出桶中的值的数量，该方法接受列标签或索引，以及可选的序列或桶的数量。

```py
bin_counts = millions.bin('Adjusted Gross', bins=np.arange(300,2001,100))
```

| bin  | Adjusted Gross count |
| ---- | -------------------- |
| 300  | 81                   |
| 400  | 52                   |
| 500  | 28                   |
| 600  | 16                   |
| 700  | 7                    |
| 800  | 5                    |
| 900  | 3                    |
| 1000 | 1                    |
| 1100 | 3                    |
| 1200 | 2                    |
| 1300 | 0                    |
| 1400 | 0                    |
| 1500 | 1                    |
| 1600 | 0                    |
| 1700 | 1                    |
| 1800 | 0                    |
| 1900 | 0                    |
| 2000 | 0                    |

## **直方图使用频率密度作为纵轴的好处**

当桶长度不等时，采用频率作为纵轴的直方图看过去很容易造成误导，无法突出显示数值的密集程度，而使用频率密度作为纵轴的直方图可以突出显示数值的密集程度

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-50-33.png)

上图是采用频数作为纵轴的直方图（但是总频数相等，因此其实 这个图和采用频率作为纵轴的直方图差不多）

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_21-54-52.png)

上图是采用频率密度作为纵轴的直方图。虽然范围`[300,400)`和`[400,600)`具有几乎相同的计数，但前者的高度是后者的两倍，因为它只有一半的宽度。 `[300,400)`中的值的密度是`[400,600)`中的密度的两倍。

**频率分布直方图（hist）帮助我们可视化数轴上数据最集中的地方，特别是当桶不均匀的时候。**

## 条形图和直方图的区别

- 条形图为每个类别展示一个数量。 它们通常用于显示**类别变量**的分布。 直方图显示**数值变量**的分布。
- 条形图中的所有条形都具有相同的宽度，相邻的条形之间有相等的间距。 直方图的条形可以具有**不同的宽度**，并且是连续的。
- 条形图中条形的**长度**（或高度，如果垂直绘制）与每个类别的值成正比。 直方图中条形的高度是密度的度量；直方图中的条形的**面积**与桶中的条目数量成正比。

## 重叠的图表

在这一章中，我们学习了如何通过绘制图表来显示数据。 这种可视化的常见用法是比较两个数据集。 在本节中，我们将看到如何叠加绘图，即将它们绘制在单个图形中，拥有同一对坐标轴

为了使重叠有意义，重叠的图必须表示相同的变量并以相同的单位进行测量。

**为了绘制重叠图，可以用相同的方法调用`scatter`，`plot`和`barh`方法。 对于`scatter`和`plot`，一列必须作为所有叠加图的公共横轴。 对于`barh`，一列必须作为一组类别的公共轴。 一般的调用看起来像这样：**

```py
name_of_table.method(column_label_of_common_axis, array_of_labels_of_variables_to_plot)
```

更常见的是，我们首先仅仅选取图表所需的列。之后通过指定共同轴上的变量来调用方法。

```py
name_of_table.method(column_label_of_common_axis)
```

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_22-09-41.png)
![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_22-09-47.png)
![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-19_22-10-21.png)

# 函数和表格

## 定义函数

我们通过编写`def`来开始定义任何函数。

一个函数可以有多个参数

 文档字符串通常在开始和结束处使用三个引号来定义，这允许字符串跨越多行。 第一行通常是函数的完整但简短的描述，而下面的行则为将来的用户提供了进一步的指导。

函数通过将参数表达式放入函数名称后面的括号来调用。 任何独立定义的函数都是这样调用的。 你也看到了方法的例子，这些方法就像函数一样，但是用点符号来调用

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/d3dbf73cbcc6c06d81d679245441855c_566x429.jpg)

```py
# Our first function definition

def double(x):
    """ Double x """
    return 2*x
```

```py
any_name = 42
double(any_name)
84


double(make_array(3, 4, 5))
array([ 6,  8, 10])
```

## 在列上应用函数

`apply`方法在列的每个元素上调用一个函数，返回函数调用完后的新数组。输入值的列的名称必须是字符串，仍然出现在引号内

```py
def cut_off_at_100(x):
    """The smaller of x and 100"""
    return min(x, 100)

//ages是一张表，’Age‘是列名
ages.apply(cut_off_at_100, 'Age')
array([ 17, 100,  52, 100,   6, 100])
```

## 引用函数

我们可以引用任何函数，通过写下它的名字，而没有实际调用它

```py
cut_off_at_100
<function __main__.cut_off_at_100>
```

我们可以为函数定义新名称。

```py
cut_off = cut_off_at_100
```

## 变量分类下聚合函数的使用

    使用group按分类变量对表格进行分组，统计每组内数值个数

    第一个参数为列标签，若干列作为分类变量

    第二个可选参数为函数，用于聚合组内的值，就像sql里的聚合函数

- sum

- max

- ……

```py
cones.group('Flavor', max)
cones.group('Flavor', sum)
more_cones.group(['Flavor', 'Color'])
more_cones.group(['Flavor', 'Color'], sum)
```

| Flavor     | Color       | Price sum |
| ---------- | ----------- | --------- |
| bubblegum  | pink        | 4.75      |
| chocolate  | dark brown  | 10.5      |
| chocolate  | light brown | 4.75      |
| strawberry | pink        | 8.8       |

| Flavor     | count |
| ---------- | ----- |
| bubblegum  | 1     |
| chocolate  | 3     |
| strawberry | 2     |

## 数据透视表

两个分类变量，列是分类变量的值，行是另一分类变量的值，形成了一个网格，由两个分类变量定位一个位置，该位置的值表示该组下的行个数

采用pivot方法生成数据透视表，`pivot`的第一个参数是列标签，包含的值将用于在结果中形成新的列。第二个参数是用于行的列标签。结果提供了原始表的所有行的计数

像`group`一样，`pivot`可以和其他参数一同使用，来发现每个类别组合的特征。名为`values`的第三个可选参数表示一列值，它们替换网格的每个单元格中的计数。所有这些值将不会显示，但是；第四个参数`collect`表示如何将它们全部汇总到一个聚合值中，来显示在单元格中。

由`pivot`生成的表格更易于阅读，因而更易于分析。 透视表的优点是它将分组的值放到相邻的列中，以便它们可以进行组合和比较。

```py
more_cones.pivot('Flavor', 'Color')
```

| Color       | bubblegum | chocolate | strawberry |
| ----------- | --------- | --------- | ---------- |
| dark brown  | 0         | 2         | 0          |
| light brown | 0         | 1         | 0          |
| pink        | 1         | 0         | 2          |

```py
more_cones.pivot('Flavor', 'Color', values='Price', collect=sum)
```

| Color       | bubblegum | chocolate | strawberry |
| ----------- | --------- | --------- | ---------- |
| dark brown  | 0         | 10.5      | 0          |
| light brown | 0         | 4.75      | 0          |
| pink        | 4.75      | 0         | 8.8        |

| Personal Income     | Bachelor's degree or higher | College, less than 4-yr degree | High school or equivalent | No high school diploma |
| ------------------- | --------------------------- | ------------------------------ | ------------------------- | ---------------------- |
| A: 0 to 4,999       | 6.75                        | 12.67                          | 18.46                     | 28.29                  |
| B: 5,000 to 9,999   | 3.82                        | 10.43                          | 9.95                      | 14.02                  |
| C: 10,000 to 14,999 | 5.31                        | 10.27                          | 11                        | 15.61                  |
| D: 15,000 to 24,999 | 9.07                        | 17.3                           | 19.9                      | 20.56                  |
| E: 25,000 to 34,999 | 8.14                        | 14.04                          | 14.76                     | 10.91                  |
| F: 35,000 to 49,999 | 13.17                       | 14.31                          | 12.44                     | 6.12                   |
| G: 50,000 to 74,999 | 18.7                        | 11.37                          | 8.35                      | 3.11                   |
| H: 75,000 and over  | 35.03                       | 9.62                           | 5.13                      | 1.38                   |

## 按列连接表

join方法连接两个表

```py
table1.join(table1_column_for_joining, table2, table2_column_for_joining)
```

| Flavor     | Price |
| ---------- | ----- |
| strawberry | 3.55  |
| vanilla    | 4.75  |
| chocolate  | 6.55  |
| strawberry | 5.25  |
| chocolate  | 5.75  |

| Kind       | Stars |
| ---------- | ----- |
| strawberry | 2.5   |
| chocolate  | 3.5   |
| vanilla    | 4     |

```py
rated = 表1.join('Flavor', 表2, 'Kind')
rated
```

| Flavor     | Price | Stars |
| ---------- | ----- | ----- |
| chocolate  | 6.55  | 3.5   |
| chocolate  | 5.75  | 3.5   |
| strawberry | 3.55  | 2.5   |
| strawberry | 5.25  | 2.5   |
| vanilla    | 4.75  | 4     |

**注意**，由于`join`中的第二个表用于扩充第一个表，所以重要的是，第一个表中的每一行在第二个表中只有一个匹配的行。如果第一个表中的某一行在第二个表中没有匹配项，则信息可能丢失。如果第一个表中的某一行在第二个表中有多个匹配项，那么`join`将只选择表2中匹配的第一行，这也是一种信息丢失

## 绘制地图

我们可以使用`Marker.map_table`来绘制地图。 该函数在一个表格上进行操作，该表格的列依次是纬度，经度以及每个点的可选标识符。

| station_id | name                              | lat     | long     | dockcount | landmark | installation |
| ---------- | --------------------------------- | ------- | -------- | --------- | -------- | ------------ |
| 2          | San Jose Diridon Caltrain Station | 37.3297 | -121.902 | 27        | San Jose | 8/6/2013     |
| 3          | San Jose Civic Center             | 37.3307 | -121.889 | 15        | San Jose | 8/5/2013     |
| 4          | Santa Clara at Almaden            | 37.334  | -121.895 | 11        | San Jose | 8/6/2013     |
| 5          | Adobe on Almaden                  | 37.3314 | -121.893 | 19        | San Jose | 8/5/2013     |
| 6          | San Pedro Square                  | 37.3367 | -121.894 | 15        | San Jose | 8/7/2013     |
| 7          | Paseo de San Antonio              | 37.3338 | -121.887 | 15        | San Jose | 8/7/2013     |
| 8          | San Salvador at 1st               | 37.3302 | -121.886 | 15        | San Jose | 8/5/2013     |
| 9          | Japantown                         | 37.3487 | -121.895 | 15        | San Jose | 8/5/2013     |
| 10         | San Jose City Hall                | 37.3374 | -121.887 | 15        | San Jose | 8/6/2013     |
| 11         | MLK Library                       | 37.3359 | -121.886 | 19        | San Jose | 8/6/2013     |

```py
Marker.map_table(stations.select('lat', 'long', 'name'))
```

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed/Snipaste_2023-01-20_21-52-38.png)

# 随机性

## python用于随机选择的模块

 在`numpy`中有一个叫做`random`的子模块，它包含许多涉及随机选择的函数。 其中一个函数称为`choice`。 它从一个数组中随机选取一个项目，选择任何项目都是等可能的。 函数调用是`np.random.choice(array_name)`，其中`array_name`是要从中进行选择的数组的名称。

```py
two_groups = make_array('treatment', 'control')
np.random.choice(two_groups)
'treatment'
```

可以通过提供第二个参数来重复np.random.choice这个过程，它是重复这个过程的次数。

```py
np.random.choice(two_groups, 10)
array(['treatment', 'control', 'treatment', 'control', 'control',
       'treatment', 'treatment', 'control', 'control', 'control'], 
      dtype='<U9')
```

## 比较数组和值

如果我们比较一个数组和一个值，则数组的每个元素都与该值进行比较，并将比较结果求值为布尔值数组。

```py
tosses = make_array('Tails', 'Heads', 'Tails', 'Heads', 'Heads')
tosses == 'Heads'
array([False,  True, False,  True,  True], dtype=bool)
```

`numpy`方法`count_nonzero`计算数组的非零（即`True`）元素的数量。

```py
np.count_nonzero(tosses == 'Heads')
3
```

## 条件语句

```py
if <if expression>:
    <if body>
elif <elif expression 0>:
    <elif body 0>
elif <elif expression 1>:
    <elif body 1>
...
else:
    <else body>
```

## for循环

```py
for i in np.arange(3):
    print(i)
0
1
2
```

### 扩展数组

调用`np.append(array_name，value)`将求出一个新的数组，它是由`value`扩展的`array_name`，原数组不变

```py
pets = make_array('Cat', 'Dog')
np.append(pets, 'Another Pet')
array(['Cat', 'Dog', 'Another Pet'], 
      dtype='<U11')


pets
array(['Cat', 'Dog'], 
      dtype='<U3')
```

可以通过将扩展后的数组赋给原始数组来达到拓展原数组的效果

```py
pets = np.append(pets, 'Another Pet')
pets
array(['Cat', 'Dog', 'Another Pet'], 
      dtype='<U11')
```

## 事件不会发生的时候

P(事件不发生)=1-P（事件发生）

## 所有结果等可能的时候

P（一个事件发生）= 该事件发生的结果数/所有结果数

## 两个事件必须同时发生时

通常，我们拥有乘法规则：

两个事件同时发生的概率，等于第一个事件发生的概率，乘上第一个事件发生的情况下第二个事件发生的概率。

## 事件以两种不同的方式发生

通常，我们拥有加法规则：

事件发生的概率，等于以第一种方式发生的概率，加上以第二种方式发生的概率。

只要事件正好以两种方式之一发生。

### 至少有……的概率

P(至少有……)=1-P(全都不)

## 确定性样本

当你只是简单地指定，你要选择的集合中的哪些元素时，就不会涉及任何几率，称为确定性样本

## 概率样本

以概率进行抽样得到的样本

总体是抽取样本的所有元素的集合。

## 系统样本

想象一下，总体的所有元素都列出在序列中。 抽样的一种方法是，先从列表中选择一个随机的位置，然后是它后面的等间隔的位置。样本由这些位置上的元素组成。这样的样本被称为系统样本。

### 放回或不放回的随机抽样
