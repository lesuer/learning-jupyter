### 互动小部件

还有一个互动小部件。 交互式小部件像交互式小部件一样工作，但直到由脚本直接调用才显示用户输入控件。 如果您必须对小部件显示的参数进行一些计算，或者即使您想确定是否需要在运行时进行控制，这也是非常有用的。
 



[128]

 
交互式的小工具

例如，我们可以使用以下脚本（类似于前面的脚本）：


```
from ipywidgets import interactive def myfunction(x):

return x

w = interactive(myfunction, x= "Hello World "); from IPython.display import display

display(w)

```
脚本有一些变化：

   我们正在引用交互式小部件

   交互式函数返回一个小部件，而不是立即显示一个值

   我们必须自己编写小部件的显示

如果我们运行这个脚本，它看起来和以前的脚本非常相似：

![](/assets/jh.jpg)

