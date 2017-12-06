### Scala模式匹配

斯卡拉有非常有用的，内置的模式匹配。 模式匹配可用于测试整个值，部分对象等的精确和/或部分匹配; 你的名字！

我们可以使用这个示例脚本作为参考：


```
def matchTest(x: Any): Any = x match { case 7 => "seven"

case "two" => 2

case _ => "something"

}

val isItTwo = matchTest("two") val isItTest = matchTest("test") val isItSeven = matchTest(7)

```
我们定义一个名为matchTest的函数。 它采取任何形式的参数，并可以返回任何类型的结果（不知道这是否是真实的编程！）。

感兴趣的关键字是匹配的。 这意味着函数将沿着选择列表走下去，直到获得传递的值x上的匹配，然后返回它。

正如你所看到的，我们有数字和字符串作为输入和输出。

最后一个case语句是一个通配符，如果代码得到这么多，它将匹配任何参数。

我们可以在这里看到输出：

![](/assets/我是不玩.jpg)
 
















[189]
