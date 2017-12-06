### 分类的字数

使用相同的脚本稍作修改，我们可以再调用一次，并对结果进行排序。 脚本现在看起来像这样：


```
import pyspark

if not 'sc' in globals():

sc = pyspark.SparkContext()

text_file = sc.textFile("Spark File Words.ipynb")

sorted_counts = text_file.flatMap(lambda line: line.split(" ")) \

.map(lambda word: (word, 1)) \

.reduceByKey(lambda a, b: a + b) \

.sortByKey()

for	x in sorted_counts.collect(): print x
 


[ 202 ]


```
在这里，我们添加了对RDD创建的另一个函数调用sortByKey（）。 所以，当我们有了地图/缩小到达单词和事件列表后，我们可以很容易地对结果进行排序。

结果输出如下所示：

![](/assets/分人.jpg)
