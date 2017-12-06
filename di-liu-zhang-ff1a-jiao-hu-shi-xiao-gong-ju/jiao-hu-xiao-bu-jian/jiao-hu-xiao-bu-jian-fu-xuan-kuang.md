### 交互小部件滑块

我们可以通过传递一个范围来使用交互来产生一个滑块。 采取以下脚本：



```
from ipywidgets import interact

# define a function to work with (cubes the number) def myfunction(arg):

return arg+1 interact(myfunction, arg=9);

```
在这里，我们有一个脚本，它执行以下操作：

   引用我们想要使用的包

   定义一个函数（为每个用户输入的值调用）调用交互，传递我们的处理函数和一系列值

当我们运行这个脚本时，我们得到一个可以被用户修改的滚动条：

![](/assets/tr.jpg)

我更新了我的安装，但仍收到一些屏幕的警告消息。 我认为在未来版本的软件中解决此警告消息错误是时间问题。