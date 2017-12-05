### 朱比特的基本朱莉娅
****
在这个例子中，我们将使用Iris数据集进行一些标准分析。所以，开始一个新的茱莉亚笔记本，并称之为茱莉亚虹膜。我们可以输入一个小脚本来查看Julia脚本的步骤。

这个脚本使用另一个包来绘制，Gadfly。在操作脚本之前，您将必须像以前一样执行类似的步骤来安装软件包。

将以下脚本输入到笔记本的单独单元格中：

使用RDatasets，DataFrames，Gadfly set_default_plot_size（5inch，5inch / golden）; plot（数据集（“数据集”，“虹膜”），x =“SepalWidth”，
y =“SepalLength”，color =“Species”）

RDataSets是一个包含几个常用R数据集的库，例如Iris。这是一个简单的脚本 - 我们定义要使用的库，设置绘图区的大小，绘制虹膜数据点（颜色编码为物种）。
 











[83]

 
Jupyter Julia脚本

所以，你最终会看到如下屏幕截图：

![](/assets/70.jpg)

我们应该注意到Julia笔记本视图的几个方面：

   我们在右上角有Julia徽标（三个彩色圆圈）。 你会看到这个徽标运行在其他的Julia安装中（正如我们之前在运行Julia命令行时看到的那样）。

   Julia徽标右侧的圆圈是繁忙的指标。 当你的脚本开始时，表格的标题表示繁忙的Julia正在启动。 当您的脚本正在运行时，该圈被填充为黑色。 当它没有运行时，它是空的。
   其余的菜单项与以前一样。

在我的Windows机器上，Julia笔记本第一次启动需要一段时间。 内核启动，请稍候...消息

显示几分钟。
 







[84]

 
Jupyter Julia脚本

如果你运行这个脚本（使用Cell | Run All菜单命令），你的输出应该如下图所示：
![](/assets/71.jpg)


我注意到，如果将鼠标悬停在图形上，则会显示网格线，并使用滑动条来调整缩放级别（如前面屏幕截图的右上部分所示）。

所以，就像你在Julia解释器中运行脚本一样，你得到你的输出（带有数字前缀）。 Jupyter已经对这些陈述进行了统计，所以我们对这些单元格进行了增量编号。 Jupyter没有做任何特别的事情来打印变量或类似的东西。
 










[85]

 
Jupyter Julia脚本

我们启动了服务器，创建了一个新的笔记本，并将其保存为Julia Iris。 如果我们打开磁盘上的IPYNB文件（使用文本编辑器），我们可以看到以下内容：



```
{

"cells": [

...<similar to previously displayed>

],

"metadata": {

"kernelspec": {

"display_name": "Julia 0.4.5",

"language": "julia",

"name": "julia-0.4"

},

"language_info": { "file_extension": ".jl",

"mimetype": "application/julia",

"name": "julia",

"version": "0.4.5"

}

...<omitted>

}

```
这与我们在前几章中用其他笔记本语言编码看到的有点不同。 尤其是，元数据明确地将脚本单元定位为Julia脚本。


