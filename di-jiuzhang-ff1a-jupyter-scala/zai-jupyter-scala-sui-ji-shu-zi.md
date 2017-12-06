### 在Jupyter的斯卡拉随机数字

在这个例子中，我们模拟一个滚动的骰子，并计算每个组合出现的次数。 为了便于说明，我们提供一个简单的直方图。

脚本如下：


```
val r = new scala.util.Random r.setSeed(113L)

val samples = 1000

var dice = new Array[Int](12) for( i <- 1 to samples){

var total = r.nextInt(6) + r.nextInt(6) dice(total) = dice(total) + 1

}

val max = dice.reduceLeft(_ max _) for( i <- 0 to 11) {
 

[ 185 ]

 
Jupyter Scala

var str =	""
for( j <-	1 to dice(i)/3) {
str =	str + "X"

}

print(i+1, str, "\n")

}


```
我们首先拉斯卡拉随机库。 我们设置种子（为了有可重复的结果）。 我们正在抽1000卷。 对于每一卷，我们增加一个计数器，显示出1号和2号点的总点数。 然后我们给出一个缩略的结果直方图。

Scala有许多快捷方法可以快速扫描列表/集合，如reduceLeft（_ max _）语句所示。 我们还可以通过在reduceLeft语句中使用min而不是max来找到最小值。

当我们运行这个脚本时，我们得到了这些结果：

![](/assets/i7y.jpg)

我们可以看到粗略的直方图以及脚本中标量变量的当前值的后续显示。 请注意，我除以三，结果将适合在一个页面上。