### 在Jupyter的Python熊猫
****
Python中使用最广泛的功能之一是熊猫。 这是一个可以自由使用的第三方数据分析软件包库。 在这个例子中，我们将开发一个使用大熊猫的Python脚本来查看在Jupyter中使用它是否有任何影响。

我正在使用http://www.kaggle.com/c/titanic-gettingStarted/download/train.csv中的泰坦尼克号数据集。 我确信从各种来源可以得到相同的数据。

这里是我们想要在Jupyter中运行的Python脚本：


```
from pandas import *

training_set = read_csv('train.csv') training_set.head()

male = training_set[training_set.sex == 'male'] female = training_set[training_set.sex =='female']

womens_survival_rate = float(sum(female.survived))/len(female) mens_survival_rate = float(sum(male.survived))/len(male)

```
结果是我们根据他们的性别来计算泰坦尼克号乘客的生存率。
 



我们创建一个新的笔记本，将脚本输入到适当的单元格中，包括在每个点添加计算数据的显示，并产生我们的结果。

这是我们的笔记本布局; 我们在每个单元格中添加了计算数据的显示，如以下屏幕截图所示：


![](/assets/50.jpg)

当我运行这个脚本时，我遇到了两个问题。

在Windows上，通常使用反斜线（\）来分隔文件名的一部分。 但是，这种编码使用反斜杠作为特殊字符。 所以，我不得不在我的CSV文件路径中使用正斜杠（/）。 我原来在前面的代码示例中有一个完整的CSV路径。 数据集列名直接从文件中获取，并且是大小写的

敏感。 在这种情况下，我原本是在脚本中使用sex字段，但是在CSV文件中，该列名为Sex。 同样，我不得不改变

幸免于难。


Jupyter Python脚本

当我们运行它时，最终的脚本和结果如下图所示：

![](/assets/51.jpg)

我用head（）函数来显示数据集的前几行。 看到为所有乘客提供的细节数量是有趣的。
 















[48]

 
Jupyter Python脚本

如果向下滚动，则会看到结果，如以下屏幕截图所示：