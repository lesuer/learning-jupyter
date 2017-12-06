### 斯卡拉不变性

不可变意味着你不能改变一些东西。 在Scala中，所有的变量都是不可变的，除非特别指出。 这与Java等语言相反，除非另有明确标示，否则所有变量都是可变的。
 



[191]

 
Jupyter Scala

在Java中，我们可以有以下功能：
public void calculate（integer amount）{

}

我们可以修改计算函数内的数值。 如果我们使用final关键字，我们可以告诉Java不允许改变值：

public void calculate（final integer amount）{

}

而在斯卡拉，类似的例程如下：



```

def calculate (amount: Int): Int = { amount = amount + 1;

return amount;

}

```


前面的代码在调用例程之前保留了数量变量的值。

![](/assets/沟通.jpg)

我们可以在显示中看到，即使balance是一个变量（标记为var），Scala也不会允许您在函数内部更改它的值。
 






[192]