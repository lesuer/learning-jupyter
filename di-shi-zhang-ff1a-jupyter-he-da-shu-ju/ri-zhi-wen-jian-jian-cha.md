### 日志文件检查
****
我从http://www.monitorware.com/下载了一个access_log文件。 像任何其他Web访问日志一样，每条记录有一行，如下所示：

64.242.88.10 - - [07 / Mar / 2004：16：05：49 -0800]“GET

/twiki/bin/edit/Main/Double_bounce_sender?topicparent=Main.ConfigurationVar iables HTTP / 1.1“401 12846

   第一部分是调用者的IP地址，后跟时间戳，HTTP访问类型，引用的URL，HTTP类型，生成的HTTP响应代码，最后是响应中的字节数。

   我们可以使用Spark来加载和解析日志条目的一些统计信息，如下面的脚本所示：


```
import pyspark

if not 'sc' in globals():

sc = pyspark.SparkContext() textFile = sc.textFile("access_log") print(textFile.count(),"access records")

gets = textFile.filter(lambda line: "GET" in line) print(gets.count(),"GETs")

posts = textFile.filter(lambda line: "POST" in line) print(posts.count(),"POSTs")

other = textFile.subtract(gets).subtract(posts) print(other.count(),"Other")

for	x in other.collect(): print x

```
这个脚本与其他脚本有相同的序言。

我们在access_log文件中读取。 然后我们打印记录的数量。

同样，我们找出有多少个日志条目是GET和POST操作。 GET被认为是最普遍的。

当我第一次这样做的时候，我真的没有想到其他的东西，所以我删除了集合中的获取和帖子，并打印出来，看看它们是什么。
 









[205]

 
Jupyter和大数据

当我们在Jupyter中运行这个时，我们看到了预期的输出：

![](/assets/一年.jpg)

文本处理速度不是很快（特别是对于那么少的记录）。

我喜欢能够以这种方式处理数据帧。 能够以程序化方式使用基本代数进行基本代数，而不必担心边缘情况，这是令人高兴的。

顺便说一下，一个HEAD请求就像一个GET，但不返回HTTP正文。 这使得调用者可以确定什么样的响应会返回并适当地作出响应。
 







[206]

