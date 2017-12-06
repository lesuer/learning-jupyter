### 斯卡拉关闭

闭包是一个功能。 得到的函数值取决于函数外声明的变量的值。

我们可以用这个小脚本来说明它：


```
var factor = 7

val multiplier = (i:Int) => i * factor val a = multiplier(11)

val b = multiplier(12)

```
我们定义一个名为multiplier的函数。 该函数需要一个整数参数。 对于每一个论点，我们都把这个论点乘以外部变量因子。

我们看到这个结果：


![](/assets/违法无法.jpg)
