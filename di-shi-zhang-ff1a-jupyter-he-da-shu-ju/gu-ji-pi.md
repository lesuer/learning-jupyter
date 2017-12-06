### 估计Pi

我们可以使用map / reduce来估计Pi。 假设我们有代码l


```
import pyspark import random

if not 'sc' in globals():

sc = pyspark.SparkContext() NUM_SAMPLES = 1000

def sample(p):

x,y = random.random(),random.random() return 1 if x*x + y*y < 1 else 0

count = sc.parallelize(xrange(0, NUM_SAMPLES)) \

.map(sample) \

.reduce(lambda a, b: a + b)

print "Pi is roughly %f" % (4.0 * count / NUM_SAMPLES)
 


[ 203 ]


```
此代码具有相同的序言。 我们正在使用随机的Python包。 有一个样本的数量不断尝试。

我们正在建立一个名为count的RDD。 我们要求并行化功能把这个过程分解成可用的节点。 代码只是映射示例函数调用的结果。 最后，我们通过添加所有样本来减少生成的地图集。

示例函数获取两个随机数，并返回1或0，具体取决于两个数字的大小。 我们正在寻找一个小范围内的随机数，然后比较它们是否出现在相同直径的圆内。 有了足够大的样本，我们最终会得到Pi（3.141 ...）。

如果我们在Jupyter中运行它，我们看到以下内容：

![](/assets/关闭.jpg)


当我用NUM_SAMPLES = 10000运行这个时，我结束了这个：

PI = 3.138000。
