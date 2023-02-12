# Pandas数据结构

## Pandas数据结构

#### 介绍

Series是一种类似于一维数组的对象，它由一组数据（各种Numpy数据类型）以及一组与之相关的数据标签（即索引）组成。

**DataFrame** 是一个表格型的数据结构，它含有一组有序的列，每列可以是不同的值类型（数值、字符串、布尔型值）。DataFrame 既有行索引也有列索引，它可以被看做由 Series 组成的字典（共同用一个索引）。

索引不一定是行号，可以是数字、字符串等，索引可以不唯一

列名则需要唯一

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed@master/Snipaste_2023-02-04_17-28-00.png)

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed@master/Snipaste_2023-02-04_17-29-05.png)

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed@master/Snipaste_2023-02-04_17-31-27.png)

#### 有关DataFrame的一些操作

从文件读入DataFrame

```python
pd.read_文件类型(文件路径)
```

显示DataFrame的一些行

```python
DataFrame名.head(行数)
DataFrame名.tail(行数)
```

在某一列上设置索引，设置索引不会影响原DataFrame

```
pd.read_文件类型(文件路径，index_col="列名")
或者
DataFrame名.set_index("列名")
```

## Pandas索引

#### []操作符

根据索引名获取DataFrame的列，即获取某一Series

```
DataFrame名[索引名]
```

根据索引名获取子DataFrame

```
elections_year_index[["Candidate","Party"]]
```

将Series转变为DataFrame

```
elections_year_index[“Candidate"].to_frame()
```

[]也接受数字切片作为参数，此时索引是按行的

以下返回0、1、2行

```
elections_year_index[0:3]
```

#### 总结

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed@master/Snipaste_2023-02-04_18-01-42.png)

## Pandas布尔数组选择和查询

以下查询将 ==’win‘ 应用到Series中的每个元素，返回一个布尔数组

```
elections_year_index['Result'] == 'win'
```

返回Result列中为win的行

```
elections_year_index[elections_year_index['Result'] == 'win']
```

![](https://cdn.jsdelivr.net/gh/sesns/picgo_bed@master/Snipaste_2023-02-04_18-15-15.png)

## Pandas loc和iloc用法

| 方法名称    | 说明         |
| ------- | ---------- |
| .loc[]  | 基于标签索引选取数据 |
| .iloc[] | 基于整数索引选取数据 |

[Pandas loc/iloc用法详解](http://c.biancheng.net/pandas/loc-iloc.html)

## Sample方法

以下不带放回地抽样，样本量为10

```
elections.sample(10)
```

以下带放回地抽样

```
elections.sample(10,replace=True)
```

## Pandas里的一些工具

#### dataframe的一些方法

head返回前几行

size返回dataframe的项数（其等于行数*列数）

shape返回 行数、列数

describe返回一些计数信息

index有多个方法，返回一些索引信息

columns返回列的一些信息

sort_values(’列名‘，ascending=True or False)用来根据某列排序


