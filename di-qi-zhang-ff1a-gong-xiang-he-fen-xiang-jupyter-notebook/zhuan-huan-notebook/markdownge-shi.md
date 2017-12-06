### Markdown格式

Markdown（.md）格式是HTML的一个宽松版本（请记住，HTML代表超文本标记语言）。 MD文件可以被某些工具使用。 它通常用作软件发行版的README文件格式（客户端的显示功能可能非常有限）。

例如，同一个笔记本的Markdown格式如下：


```
```javascript

const stats = require("stats-analysis");

var arr = [98, 98.6, 98.4, 98.8, 200, 120, 98.5]; //standard deviation

var my_stddev = stats.stdev(arr).toFixed(2);

//mean

var my_mean = stats.mean(arr).toFixed(2);

//median

var my_median = stats.median(arr);

//median absolute deviation var my_mad = stats.MAD(arr);

//	Outlier detection. Returns indexes of outliers var my_outliers = stats.indexOfOutliers(arr);

//	Remove the outliers

var my_without_outliers = stats.filterOutliers(arr);

//display our stats console.log("Raw data is ", arr);
...

```
显然，Markdown格式是非常低级的显示。 只有很小的文字标记可帮助读者确定使用的不同格式。 我使用Atom编辑器来查看这看起来像什么解释：
 


















[157]
![](/assets/据了解.jpg)

再次，一个非常干净的显示器 - 仍然接近Jupyter Notebook显示器。

