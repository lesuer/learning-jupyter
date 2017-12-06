### 火花字数

现在我们已经看到了一些功能，让我们进一步探讨。 我们可以使用类似的脚本来计算文件中出现的单词，如下所示：



```
import pyspark

if not 'sc' in globals():

sc = pyspark.SparkContext()

text_file = sc.textFile("Spark File Words.ipynb")

counts = text_file.flatMap(lambda line: line.split(" ")) \

.map(lambda word: (word, 1)) \

.reduceByKey(lambda a, b: a + b) for x in counts.collect():

print x


```
我们对编码有相同的序言。然后我们加载文本文件到内存中。

一旦文件被加载，我们将每一行分成单词。使用lambda函数勾选每个单词的出现。代码确实为每个单词的出现创建了一个新的记录。如果流中出现一个单词，则为该单词添加一个计数为1的记录，对于该单词出现的每个其他实例，将添加具有相同计数1的新记录。这个想法是，这个过程可以分成多个处理器，每个处理器产生这些低级别的信息位。我们不关心优化这个过程。

一旦我们拥有了所有这些记录，我们就根据提到的单词出现次数来减少/总结记录集。

计数对象在Spark中称为弹性分布式数据集（RDD）。这是坚韧的，因为谨慎坚持数据集。 RDD是分布式的，因为它可以被操作集群中的所有节点操纵。当然，这是一个包含各种数据项的数据集。

最后一个for循环对RDD运行collect（）。如上所述，这个RDD可以分布在许多节点中。 collect（）函数将RDD的所有副本拖放到一个位置。然后我们遍历每条记录。
 











[201]

 
Jupyter和大数据

当我们在Jupyter中运行这个时，我们看到类似于这个显示的东西：


![](/assets/工本费.jpg)

列表缩写为单词列表持续一段时间。 奇怪的是，Spark中的分词逻辑似乎不能很好地工作！ 一些结果不是单词，比如第一个输入 - 空字符串。

