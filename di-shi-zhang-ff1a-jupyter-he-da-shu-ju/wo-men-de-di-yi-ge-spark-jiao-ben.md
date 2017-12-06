### 我们的第一个Spark脚本

我们的第一个脚本读入一个文本文件，看看这些行长度加起来多少：


```
import pyspark

if not 'sc' in globals():

sc = pyspark.SparkContext()

lines = sc.textFile("Spark File Words.ipynb") lineLengths = lines.map(lambda s: len(s)) totalLength = lineLengths.reduce(lambda a, b: a + b) print(totalLength)
 







[ 199 ]


```
在脚本中，如果我们还没有做，我们首先会初始化Spark。 如果您尝试多次初始化Spark，Spark会发出抱怨，所以如果前缀语句中的所有Spark脚本都应该有这个。

脚本读入一个文本文件（这个脚本的来源），占用每一行，并计算其长度; 然后将所有长度加在一起。

lambda函数是一个匿名（未命名）函数，它接受参数并返回一个值。 在第一种情况下，给定一个字符串s，它返回它的长度。

reduce函数接受一个参数，将第二个参数应用于它，用结果替换第一个值，然后继续列表的其余部分。 在我们的例子中，它遍历线的长度，并把它们全部加起来。

然后，在笔记本上运行，我们看到以下结果：

![](/assets/提要.jpg)


请注意，文件的大小可能会稍有不同。 另外，第一次启动Spark引擎（使用sc = pyspark.SparkContext（）行），可能需要一段时间，脚本可能无法成功完成。 如果发生这种情况，请再试一次。
 









[200]
