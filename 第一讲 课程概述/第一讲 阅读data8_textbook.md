# 1.什么是数据科学

    数据科学是关于通过探索，预测和推论从大量且多样的数据中得出有用的结论

    探索：发现信息中的模式

    预测：使用已知信息去作出有根据的猜测

    推论：包括量化确认度：我们的预测有多精确、我们在数据中发现的模式是否也会出现在新观察中？

    工具

- 对于探索，有描述性统计学、可视化

- 对于预测，有机器学习与优化

- 对于推论，有统计测试和模型

## 1.1介绍

#### 1.1.1运算工具

    本书采用python3及其一些数据可视化工具

#### 1.1.2统计技术

    统计的最重要贡献之一是描述观察和结论之间关系的一致且精确的词汇。

    本文涉及到以下问题：测试假设，估计置信度和预测未知数量等

## 1.3绘制经典

    从网上抓取两本经典书的文本，并将其转换成章节的列表

```python
# Read two books, fast!

huck_finn_url = 'https://www.inferentialthinking.com/data/huck_finn.txt'
huck_finn_text = read_url(huck_finn_url)
huck_finn_chapters = huck_finn_text.split('CHAPTER ')[44:]

little_women_url = 'https://www.inferentialthinking.com/data/little_women.txt'
little_women_text = read_url(little_women_url)
little_women_chapters = little_women_text.split('CHAPTER ')[1:]
```

```python
# Display the chapters of Huckleberry Finn in a table.

Table().with_column('Chapters', huck_finn_chapters)    
```

    结果

| Chapters                                                     |
|:------------------------------------------------------------:|
| I. YOU don't know about me without you have read a book ...  |
| II. WE went tiptoeing along a path amongst the trees bac ... |
| III. WELL, I got a good going-over in the morning from o ... |
| IV. WELL, three or four months run along, and it was wel ... |
| V. I had shut the door to. Then I turned around and ther ... |
| VI. WELL, pretty soon the old man was up and around agai ... |
| VII. "GIT up! What you 'bout?" I opened my eyes and look ... |
| VIII. THE sun was up so high when I waked that I judged ...  |
| IX. I wanted to go and look at a place right about the m ... |
| X. AFTER breakfast I wanted to talk about the dead man a ... |

... (33 rows omitted)


