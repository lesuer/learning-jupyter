### Jupyter中的Python随机数字
****
对于许多分析，我们有兴趣计算可重复的结果。 但是，大量的分析依赖于使用随机数字。 在Python中，您可以使用random_seed（）函数设置随机数生成器的种子以获得可重复的结果。
 


[55]

 
Jupyter Python脚本

在这个例子中，我们模拟滚动一对骰子，看看结果。 我们正在使用的脚本是这样的：


```
import pylab import random random.seed(113) samples = 1000 dice = []

for i in range(samples):

total = random.randint(1,6) + random.randint(1,6) dice.append(total)

pylab.hist(dice, bins= pylab.arange(1.5,12.6,1.0)) pylab.show()

```
一旦我们在Jupyter中有脚本并执行它，我们就得到了这样的结果：

![](/assets/115.jpg)


我增加了更多的统计数据。 我不确定我是否会有这么高的标准偏差。 如果我们增加样本的数量，这将会增加。

结果图在新窗口中打开，就像在另一个Python开发环境中运行该脚本一样：
![](/assets/116.jpg)

图形顶部的工具栏非常丰富，您可以通过多种方式操作图形。

