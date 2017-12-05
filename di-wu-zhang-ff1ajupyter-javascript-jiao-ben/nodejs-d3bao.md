### Node.js d3包

d3软件包具有数据访问功能。 在这种情况下，我们将从一个制表符分隔的文件中读取并计算一个平均值。 请注意使用lodash的下划线变量名称。 以下划线开头的变量名称被认为是私有的，但在这种情况下，它只是我们使用的包名称，lodash或下划线。 此外，lodash是一个广泛使用的实用程序包。

我们使用的脚本如下：


```
var fs = require("fs"); var d3 = require("d3"); var _ = require("lodash");

//read in the animals file

fs.readFile("data/animals.tsv", "utf8", function(error, data) { data = d3.tsv.parse(data);

//display on screen console.log(JSON.stringify(data));
//compute the maximum weight

var maxWeight = d3.max(data, function(d) { return d.avg_weight; });

//display the max on screen console.log(maxWeight);
});
 


[ 106 ]


```
假设我们已经使用npm加载了fs和d3软件包，如前面的脚本所述。

在这个例子中，我在笔记本所在的目录（通常是用户的主目录）中创建了一个数据子目录，并在该目录下创建了一个标签文件（animal.tsv）：

使用<tab>包含一个实际的制表符。


```
name<tab>avg_weight lion<tab>400 tiger<tab>400 human<tab>150 elephant<tab>2000
```
如果我们将这个脚本加载到笔记本中并运行它，我们会得到如下输出：

![](/assets/吧.jpg)

有趣的是，最大功能不能按预期工作。 我本可以预期的是，2000磅的大象价值将被显示出来。 我已经被告知，如果脚本属性将字符串转换为数字，则会描绘正确的结果。
