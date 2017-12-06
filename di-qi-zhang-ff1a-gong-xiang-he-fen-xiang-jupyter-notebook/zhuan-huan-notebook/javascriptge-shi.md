### JavaScript格式

JavaScript（.js）格式对应于笔记本的JavaScript实现。 如果您使用JavaScript作为笔记本的语言，则这是笔记本页面的直接导出。

如果您对笔记本的脚本使用了另一种语言（例如Python），则“下载为”选项将会相应更改，即“下载为|的Python（的.py）。

按照我们的例子，JS格式等同于Jupyter显示：


```
const stats = require("stats-analysis");

var arr = [98, 98.6, 98.4, 98.8, 200, 120, 98.5]

//standard deviation

var my_stddev = stats.stdev(arr).toFixed(2);

//mean

var my_mean = stats.mean(arr).toFixed(2); //median

var my_median = stats.median(arr); //median absolute deviation
var my_mad = stats.MAD(arr);

// Outlier detection. Returns indexes of outliers var my_outliers = stats.indexOfOutliers(arr);

...
 













[ 154 ]

 
Sharing and Converting Jupyter Notebooks

```
使用JS格式，您可以使用JavaScript解释器直接运行脚本。 在Mac上，有js命令。 Windows机器也有类似的工具。

另外，对于其他脚本语言，您应该能够在合适的解释器（如Python）中运行该脚本。

如果我们运行这个JavaScript文件（从命令行窗口），我们在单元格输出中看到这些结果：



```
$ node Stats+Analysis.js

Raw data is  [ 98, 98.6, 98.4, 98.8, 200, 120, 98.5 ]

Standard Deviation is 35.07 Mean is 116.04

Median is  98.6

Median Abs Deviation is 0.20000000000000284

The outliers of the data set are  [ 4, 5, 6 ]

The data set without outliers is  [ 98, 98.6, 98.4, 98.8 ]


```



