### Node.js JSON处理

在这个例子中，我们将加载一个JSON数据集，并对数据执行一些标准的操作。我参考了http://www.carqueryapi.com/api/0.3/?callback=?&cmd=getModels&make=ford的福特车型列表。我不能直接引用它，因为它不是一个平面文件，而是一个API调用。所以，我将数据下载到本地文件fords.json中。此外，来自API调用的输出包装JSON，如？（json？？）;这将不得不在解析之前被删除。

我们将使用的脚本如下。在脚本中，JSON是一个Node.js的内置包，所以我们可以直接引用这个包。 JSON包提供了许多你需要处理你的JSON文件和对象的标准工具。

这里感兴趣的是构造一个标准的JavaScript对象数组的JSON文件阅读器。每个对象的属性可以通过名称来引用，例如model.model_name。我们可以看到这个特性在使用这个脚本读取JSON文件并根据JSON文件中的字段名称解析出感兴趣的数据元素：


```
//load the JSON dataset //http://www.carqueryapi.com/api/0.3/ ?callback=?&cmd=getModels&make=ford

var fords = require('/Users/dtoomey/fords.json');

//display how many Ford models are in our data set console.log("There are " + fords.Models.length +

" Ford models in the data set"); //loop over the set

var index = 1

for(var i=0; i<fords.Models.length; i++) { //get this model

var model = fords.Models[i];

//pull it's name

var name = model.model_name;

//if the model name does not have numerics in it if(! name.match(/[0-9]/i)) {

//display the model name
 

[ 110 ]

 
Jupyter JavaScript Coding

console.log("Model " + index + " is a " + name); index++;

}

//only display the first 5 if (index>5) break;

}

```
如果我们把这个脚本放到一个新的笔记本中，我们会得到如下屏幕：

![](/assets/程序.jpg)

当行被执行时，我们得到预期的结果，如下所示：

![](/assets/指向.jpg)
