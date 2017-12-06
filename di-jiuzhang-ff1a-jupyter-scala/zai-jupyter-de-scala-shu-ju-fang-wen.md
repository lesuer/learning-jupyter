### 在Jupyter的Scala数据访问
****
加州大学欧文分校的网站https上有一个iris数据集的副本

：//archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data。 我们将访问这些数据并执行一些简单的统计。

Scala代码如下：


```
import scala.io.Source;

//copied file locally https://archive.ics.uci.edu/ml/ machine-learning-databases/iris/iris.data

val filename = "iris.data"

//DEBUGGING Uncomment this line to display more information - println("SepalLength, SepalWidth, PetalLength, PetalWidth, Class"); val array = scala.collection.mutable.ArrayBuffer.empty[Float]

for	(line <- Source.fromFile(filename).getLines) { var cols = line.split(",").map(_.trim);

//println(s"${cols(0)}|${cols(1)}|${cols(2)}| ${cols(3)} |${cols(4)}");

val i = cols(0).toFloat array += i;

}

val count = array.length; var min:Double = 9999.0; var max:Double = 0.0; var total:Double = 0.0; for ( x <- array ) {

if (x < min) { min = x; } if (x > max) { max = x; } total += x;

}

val mean:Double = total / count;

```
斯卡拉会对原始文件中可能存在的多余空间抱怨不已。 一定要修剪文件。 通过Internet访问CSV文件似乎存在问题。 所以，我在本地复制文件（到笔记本所在的同一个目录）。

值得注意的是，在这个脚本中，我们没有必要将Scala代码包装在一个对象中，因为Jupyter提供了包装类。
 









[182]

 
Jupyter Scala

当我们运行脚本时，我们看到了这些结果：

![](/assets/恶女.jpg)

这是Iris数据的不同版本; 因此，我们在统计中看到的结果不同于第2章Jupyter Python Scripting中的结果。
 









[183]

 
Jupyter Scala
