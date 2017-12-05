### Node.js决策树包
****
决策树包是一个机器学习包的例子。 它可以在https://www.npmjs.com/package/decision-tree获得。 该软件包使用以下命令安装：

npm安装决策树

我们需要一个数据集用于培训/开发我们的决策树。 我正在使用汽车MPG

数据集：https://alliance.seas.upenn.edu/~cis520/wiki/index.php?n=Le ctures.DecisionTrees。 它似乎没有直接可用，所以我把它复制到Excel中，并保存为本地CSV。

机器学习的逻辑非常相似：

   加载我们的数据集

   分成训练集和测试集

   使用训练集来开发我们的模型在测试集上测试模式。
 


[118]

 
Jupyter JavaScript编码

通常情况下，您可以使用三分之二的数据进行培训，三分之一的数据用于测试。



使用决策树软件包和汽车MPG数据集，我们将有一个类似于以下的脚本：




```
//Import the modules

var DecisionTree = require('decision-tree'); var fs = require("fs");

var d3 = require("d3"); var util = require('util');

//read in the car/mpg file

fs.readFile("/Users/dtoomey/car-mpg.csv", "utf8", function(error, data)

{

//parse out the csv into a dataset var dataset = d3.tsv.parse(data);
//display on screen - just for debugging

//console.log(JSON.stringify(dataset)); var rows = dataset.length; console.log("rows = " + rows);

var training_size = rows * 2 / 3; console.log("training_size = " + training_size); var test_size = rows - training_size; console.log("test_size = " + test_size); //Prepare training dataset

var training_data = dataset.slice(1, training_size);

//Prepare test dataset

var test_data = dataset.slice(training_size, rows); //Setup Target Class used for prediction

var class_name = "mpg";

//Setup Features to be used by decision tree

var features = ["cylinders","displacement","horsepower",

"weight","acceleration", "modelyear", "maker"];

//Create decision tree and train model

var dt = new DecisionTree(training_data, class_name, features); console.log("Decision Tree is " + util.inspect

(dt, {showHidden: false, depth: null}));

//Predict class label for an instance var predicted_class = dt.predict({

cylinders: 8, displacement: 400, horsepower: 200, weight: 4000, acceleration: 12, modelyear: 70,
 

[ 119 ]

 
Jupyter JavaScript Coding

maker: "US"

});

console.log("Predicted Class is " + util.inspect (predicted_class, {showHidden: false, depth: null})); //Evaluate model on a dataset

var accuracy = dt.evaluate(test_data); console.log("Accuracy is " + accuracy);

//Export underlying model for visualization or inspection var treeModel = dt.toJSON();

console.log("Decision Tree JSON is " + util.inspect(treeModel, {showHidden: false, depth: null}));

});

```
console.log有广泛的使用来显示正在发生的处理的渐进信息。 我进一步使用util（）函数来显示正在使用的对象的成员。

软件包也必须使用npm进行安装。




如果我们在笔记本中运行这个功能，我们将在下面的截图中显示结果：


![](/assets/啊.jpg)











根据车辆的特性，我们得出一个模型来确定车辆的MPG是否可以接受。 在这种情况下，我们有一个不好的预测结果如上所述。
 











[120]

 
Jupyter JavaScript编码





