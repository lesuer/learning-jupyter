### R预测

在这个例子中，我们将根据https：// data的数据预测弗雷泽河的水位

market.com/data/set/22nm/fraser-river-at-hope-1913-1990#!ds=22nm&display=line

。 我无法找到合适的来源，所以我从网站上手动提取数据到本地文件。

我们将使用R预测软件包。 您必须将此软件包添加到您的设置中（如本章开头所述）。
 


[74]

 
Jupyter R脚本

我们将使用的R脚本如下：

库（预测）

fraser < - scan（“fraser.txt”）plot（fraser）

fraser.tsl = stl（fraser.ts，s.window =“periodic”）monthplot（fraser.stl）fraser.ts <-ts（fraser，frequency = 12，start = c（1913,3）

seasonplot（fraser.ts）

这个例子中的兴趣输出是三个地块：简单的情节，每月和计算季节。

简单的情节（使用R plot命令）就像下面的截图一样。 没有明显的组织或结构：
![](/assets/464.jpg)

每月图（使用monthplot命令）就像下面的截图一样。 河流在一个月内似乎非常一致：


![](/assets/332.jpg)

最后，季节性阴谋显示了我们一直在试图预测的东西，也就是河流的确定季节性：


![](/assets/224.jpg)





