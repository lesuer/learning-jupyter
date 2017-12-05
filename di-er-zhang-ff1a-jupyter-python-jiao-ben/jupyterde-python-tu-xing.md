### Jupyter Python脚本
****
Jupyter中的Python图形

Python图形如何在Jupyter中工作？

我为这个命名的Python图形开始了另一个视图，以区分以前的工作。

如果我们要建立一个宝宝名字的样本数据集，并在这个名字的一年内出生的人数，我们可以绘制数据。

Python编码很简单：


```
import pandas import matplotlib

%matplotlib inline

baby_name = ['Alice','Charles','Diane','Edward'] number_births = [96, 155, 66, 272]
dataset = list(zip(baby_name,number_births))

df = pandas.DataFrame(data = dataset, columns=['Name', 'Number']) df['Number'].plot()

```
脚本的步骤如下：

1.导入我们需要的图形库（和数据库）。

2.定义我们的数据。

3.将数据转换成允许简单图形显示的格式。

4.绘制数据。

我们会期望一个婴儿的名字出生人数的图表。
 



















[50]

 
Jupyter Python脚本

如果我们把前面的脚本放在Jupyter笔记本的单元格中，我们可以得到如下图所示的东西：

![](/assets/112.jpg)


