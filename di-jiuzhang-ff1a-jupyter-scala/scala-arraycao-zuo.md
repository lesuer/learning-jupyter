### 斯卡拉阵列操作
****
Scala没有熊猫，但我们可以用我们自己的编码来模拟一些逻辑。 我们将使用来自http的第2章Jupyter Python Scripting中使用的相同的Titanic数据集
：//www.kaggle.com/c/titanic-gettingStarted/download/train.csv，我们已经在本地下载了。

然后，我们可以使用与第2章Jupyter Python脚本中使用的类似的代码，在熊猫上：


```
import scala.io.Source; val filename = "train.csv"

//PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,

Parch,Ticket,Fare,Cabin,Embarked

//1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S var males = 0

var females = 0

var males_survived = 0 var females_survived = 0

for	(line <- Source.fromFile(filename).getLines) { var cols = line.split(",").map(_.trim);

var sex = cols(5); if (sex == "male") {

males = males + 1;

if (cols(1).toInt == 1) { males_survived = males_survived + 1;

}

}

if (sex == "female") { females = females + 1; if (cols(1).toInt == 1) {
females_survived = females_survived + 1;

}

}

}

val mens_survival_rate = males_survived.toFloat/males.toFloat

val womens_survival_rate = females_survived.toFloat/females.toFloat


```
在代码中，我们逐行读取文件，解析出列（这是一个CSV），然后根据数据的性别列进行计算。 有趣的是，Scala数组不是基于零的！
 







[184]

 
Jupyter Scala

当我们运行这个脚本时，我们看到和以前非常相似的结果：

![](/assets/87i.jpg)
