### 斯卡拉更高阶的功能

高阶函数或者将其他函数作为参数，或者返回一个函数作为结果。

我们可以使用这个示例脚本：


```

def squared(x: Int): Int = x * x def cubed(x: Int): Int = x * x * x

def process(a: Int, processor: Int => Int): Int = {processor(a) } val fiveSquared = process(5, squared)

val sevenCubed = process(7, cubed)

```
我们定义两个函数; 一个正方形的数字通过，另一个立方体的数字通过。

接下来，我们定义了需要处理的数字和处理器应用的高阶函数。

最后，我们称之为每一个。 例如，我们使用5和squared（）函数调用process（）。 process（）函数将5传递给squared（）函数并返回结果：
![](/assets/按时吃.jpg)

我们利用Scala的引擎自动打印变量值来查看预期结果。
