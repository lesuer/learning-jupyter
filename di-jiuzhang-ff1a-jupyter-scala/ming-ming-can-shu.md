### 命名的参数

Scala允许你指定参数分配的名称，而不仅仅是序号的位置。 例如，我们可以有这样的代码：


```
def divide(dividend:Int, divisor:Int): Float =

{ dividend.toFloat / divisor.toFloat } divide(40, 5)

divide(divisor = 40, dividend = 5)


```
如果我们在笔记本上运行它，我们可以看到结果：



![](/assets/㐇.jpg)














第一个调用是按位置划分指定的参数。 第二个电话相应地设置它们。
