### Julia并行处理
****
Julia的高级内置功能是在脚本中使用并行处理。 通常，您可以直接在Julia中指定要使用的进程数量。 但是，在Jupyter中，您将使用addproc（）函数来添加可用于脚本的其他进程。 例如，这个小脚本：

addprocs（1）

函数srand（111）

r = remotecall（rand，2，3，4）s = @spawnat 2 1。+ fetch（r）fetch（s）

这个例子调用了rand，随机数生成器和那个代码执行

在函数调用的第二个参数（过程2）上，然后将剩余的参数传递给rand函数（使rand生成一个3 x 4的随机数矩阵）。 spawnat是一个评估上述过程的宏。 然后，获取访问产生的进程的结果。

我们可以在Jupyter的例子中看到结果，如下图所示：


![](/assets/83.jpg)