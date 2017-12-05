### Spark - 评估历史数据

在这个例子中，我们结合前面的章节来看一些历史数据，并确定一些有用的属性。

我们使用的历史数据是Jon Stewart Show的客人名单。 数据中的典型记录如下所示：

1999年1/11/99演员，演员迈克尔·福克斯

它包含年份，客人的占用情况，出现的日期，职业的逻辑分组以及客人的姓名。

对于我们的分析，我们会看看每年的出场次数，最显眼的职业，最显着的个性。

我们将使用这个脚本：


```
import pyspark import csv import operator import itertools

import collections

if not 'sc' in globals():

sc = pyspark.SparkContext() years = {}

occupations = {} guests = {}

#The file header contains these column descriptors

#YEAR,GoogleKnowlege_Occupation,Show,Group,Raw_Guest_List with open('daily_show_guests.csv', 'rb') as csvfile:

reader = csv.DictReader(csvfile) for row in reader:

year = row['YEAR']

if years.has_key(year): years[year] = years[year] + 1

else:

years[year] = 1

occupation = row['GoogleKnowlege_Occupation'] if occupations.has_key(occupation):

occupations[occupation] = occupations[occupation] + 1 else:

occupations[occupation] = 1 guest = row['Raw_Guest_List'] if guests.has_key(guest):

guests[guest] = guests[guest] + 1 else:
 

[ 211 ]

 
Jupyter and Big Data

guests[guest] = 1

syears = sorted(years.items(), key=operator.itemgetter(1), reverse=True)

soccupations = sorted(occupations.items(), key=operator.itemgetter(1), reverse=True)

sguests = sorted(guests.items(), key=operator.itemgetter(1), reverse=True)

print syears[:5] print soccupations[:5] print sguests[:5]


```
该脚本有一些功能：

   我们正在使用几个软件包。

   它有熟悉的背景序言。

   我们开始多年的字典，职业和客人。 一个字典包含一个键和一个值。 对于这种使用，密钥将是CSV中的原始值。 该值将是数据集中出现的次数。

   我们打开文件，并开始逐行使用阅读器对象阅读。

   在每条线上，我们都会考虑利息的价值（年，职业，客人）：

   查看该值是否出现在适当的字典中

   如果在那里，增加值（计数器）

   否则，初始化字典中的一个条目

   然后，我们按照与项目出现次数相反的顺序对每个字典进行排序

   最后，我们显示每个字典的前五个值
 





















[212]

 
Jupyter和大数据

如果我们在笔记本上运行它，我们有这样的输出：

![](/assets/重复.jpg)
我们的脚本的第一部分是处理年份和职业累积。 这是脚本的其余部分：
 













[213]
![](/assets/分拆.jpg)

可能有更聪明的办法做到这一切，但我不知道！ 无论您使用何种语言，累加器的累积都是相当标准的。 我认为这里有一个使用map（）函数的机会。 我们可以将每个集合添加到Spark Context作为列表，然后应用map.distinct.count。

我真的很喜欢只是简单地修剪列表/数组，而不必调用某个函数。 每年的客人数量非常一致。 演员很流行 - 可能

对观众最感兴趣的人。 客人名单有点令人惊讶。 客人大多是演员，但我认为都有强大的政治方向。