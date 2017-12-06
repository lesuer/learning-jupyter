### 斯卡拉特质

Scala中的一个特征定义了一系列可以通过类实现的特性。 一个特征类似于Java中的一个接口。

特质可以部分实现，迫使特性的用户（类）实现细节。

例如，我们可以有这样的代码：


```
trait Color {

def isRed(): Boolean

}

class Red extends Color {
 

[ 194 ]

 
Jupyter Scala

def isRed() = true

}

class Blue extends Color { def isRed() = false

}

var red = new Red(); var blue = new Blue(); red.isRed() blue.isRed()

```
该代码创建了一个名为Color的特性，其中包含一个部分实现的函数isRed。 所以，每个使用Color的类都必须实现isRed（）。

然后，我们实现了两个类Red和Blue，它们扩展了Color特征（这是使用特征的Scala语法）。 由于部分实现了isRed（）函数，两个类都必须为trait函数提供实现。

我们可以在下面的笔记本电脑屏幕截图中看到如何操作：

![](/assets/分的人.jpg)

我们看到（在底部的输出部分）创建的特征和类，创建的两个实例以及调用这两个类的特征函数的结果。
