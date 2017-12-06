### 斯卡拉案例类

一个case类是一个简化的类型，可以在不调用新的Classname（..）的情况下使用。 例如，我们可以使用这个脚本来定义一个案例类并使用它：


```
case class Car(brand: String, model: String) val buickLeSabre = Car("Buick", "LeSabre")
```
所以，我们有一个叫做Car的案例类。 我们做了一个叫做buickLeSabre的类的实例。

Case类对模式匹配最有用，因为我们可以轻松地构造复杂的对象并检查其内容。 这是一个例子：


```
def carType(car: Car) = car match { case Car("Honda", "Accord") => "sedan" case Car("GM", "Denali") => "suv"

case Car("Mercedes", "300") => "luxury" case Car("Buick", "LeSabre") => "sedan" case _ => "Car: is of unknown type"

}

val typeOfBuick = carType(buickLeSabre)
 


[ 190 ]


```
我们定义一个模式匹配块（如本章前一节所述）。 在比赛中，我们看一下品牌= GM，车型= Denali等的Car对象。 对于每个感兴趣的模型，我们对它的类型进行分类。 最后我们也有一些猫腻，所以我们可以抓住意想不到的价值。

我们可以在Jupyter中运行案例类，如下图所示：

![](/assets/不固定.jpg)


我们定义并使用了Car case类。 然后，我们使用Car case类进行模式匹配。

