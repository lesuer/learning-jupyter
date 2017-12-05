### Node.js统计分析包

统计分析软件包有许多您可能想要对数据执行的常见统计数据。 你将不得不使用npm来安装这个包，如前所述。

如果我们有一小部分人的气温可以使用，那么我们可以使用这个脚本来获得一些关于数据的统计数据：


```
const stats = require("stats-analysis");

var arr = [98, 98.6, 98.4, 98.8, 200, 120, 98.5]; //standard deviation

var my_stddev = stats.stdev(arr).toFixed(2);

//mean

var my_mean = stats.mean(arr).toFixed(2);

//median

var my_median = stats.median(arr);

//median absolute deviation var my_mad = stats.MAD(arr);

//	Get the index locations of the outliers in the data set var my_outliers = stats.indexOfOutliers(arr);

//	Remove the outliers

var my_without_outliers = stats.filterOutliers(arr); //display our stats

console.log("Raw data is ", arr); console.log("Standard Deviation is ", my_stddev); console.log("Mean is ", my_mean); console.log("Median is ", my_median); console.log("Median Abs Deviation is " + my_mad);

console.log("The outliers of the data set are ", my_outliers); console.log("The data set without outliers is ", my_without_outliers);
 










[ 108 ]


```
Jupyter JavaScript编码

当这个脚本被输入到笔记本中时，我们得到类似于以下屏幕截图的东西：
![](/assets/VC.jpg)

运行时，我们得到如下屏幕截图所示的结果：
![](/assets/发.jpg)

