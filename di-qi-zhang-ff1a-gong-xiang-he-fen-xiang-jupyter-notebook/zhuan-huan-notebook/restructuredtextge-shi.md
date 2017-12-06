### reStructuredText格式

reStructuredText（.rst）格式是一种简单的纯文本标记语言，有时用于编程文档。

例如，示例页面的RST格式如下所示：


```
.. code:: python

const stats = require("stats-analysis");

var arr = [98, 98.6, 98.4, 98.8, 200, 120, 98.5];

//standard deviation

var my_stddev = stats.stdev(arr).toFixed(2);

//mean

var my_mean = stats.mean(arr).toFixed(2); //median

var my_median = stats.median(arr);

//median absolute deviation var my_mad = stats.MAD(arr);

//	Outlier detection. Returns indexes of outliers var my_outliers = stats.indexOfOutliers(arr);

//	Remove the outliers

var my_without_outliers = stats.filterOutliers(arr);

//display our stats console.log("Raw data is ", arr);

...

```
正如你所看到的，它和前面例子中的Markdown类似，只是把代码分解成块。
 





















[159]

 
共享和转换Jupyter笔记本

使用Atom显示RST文件的结果如下：

![](/assets/技能.jpg)

RST显示器不如其他一些显示器好。

