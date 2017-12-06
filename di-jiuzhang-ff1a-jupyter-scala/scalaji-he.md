### 斯卡拉集合

在Scala中，集合会根据您的使用情况自动变化或不可变。 scala.collections.immutable中的所有集合都是不可变的，scala.collections.immutable则是相反的。 Scala默认选择不可变集合，所以你的代码会自动从可变集合中获取：

var List mylist;

除非你用不可变的前缀变量，

var mylist immutable.List;

我们可以在这个少量的代码中看到这个，例如：



```
var mutableList = List(1, 2, 3);

var immutableList = scala.collection.immutable.List(4, 5, 6); mutableList.updated(1,400);

immutableList.updated(1,700);
```



正如你可以在笔记本的这个截图中看到的那样：

![](/assets/菜单.jpg)


请注意，斯卡拉在这里有一点欺骗， 它在我们更新了immutableList的时候创建了一个新的集合，就像你看到的那样，变量名是real_3。
 






[193]
