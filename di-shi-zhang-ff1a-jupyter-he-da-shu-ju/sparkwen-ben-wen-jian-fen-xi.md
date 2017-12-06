火花文本文件分析

在这个例子中，我们将浏览一篇新闻文章，从中确定一些基本信息。

我们将使用下面的脚本对2600raid新闻文章（来自http：// newsi tem.com/）：


```
import pyspark

if not 'sc' in globals():

sc = pyspark.SparkContext() sentences = sc.textFile('2600raid.txt') \

.glom() \

.map(lambda x: " ".join(x)) \

.flatMap(lambda x: x.split(".")) print(sentences.count(),"sentences")

bigrams = sentences.map(lambda x:x.split()) \

.flatMap(lambda x: [((x[i],x[i+1]),1) for i in range(0,len(x)-1)]) print(bigrams.count(),"bigrams")

frequent_bigrams = bigrams.reduceByKey(lambda x,y:x+y) \

.map(lambda x:(x[1],x[0])) \

.sortByKey(False) frequent_bigrams.take(10)

```
代码读入文章，并把文章分成句子结尾的句子。 从那里，代码映射出现在的bigrams。 双字母是一对相邻的词语。 然后，我们对这个列表进行排序，并列出排名前十的最普遍的对。
 





















[209]

 
Jupyter和大数据

当我们在笔记本上运行这个时，我们看到了这些结果：

![](/assets/吗.jpg)

我真的不知道从输出中得到什么。 很奇怪的是，你可以从文章中获得一些见解，因为“商店”出现了15次，“出现”和“看守”出现了11次 - 在商场里一定发生了突袭，并以某种方式包括了保安人员！
 










[210]