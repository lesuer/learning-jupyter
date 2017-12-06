### 小部件事件
****
所有的控件都可以通过用户的操作进行响应，无论是使用鼠标还是键盘。 控件的默认操作已内置到软件中，但您可以添加自己的事件处理（用户操作）。

我们已经看到了这种事件的早期处理，例如，在滑动条的部分，当用户改变滑动条的值时，调用一个函数 - 但是让我们稍微深入地探讨一下。 我们可以有以下脚本：


```
from ipywidgets import widgets

from IPython.display import display

button = widgets.Button(description="Click Me!") display(button)

def	on_button_clicked(b): print("Button clicked.")

button.on_click(on_button_clicked)

```
该脚本执行以下操作：

   创建一个按钮。

   显示按钮（给用户）。

   定义处理程序点击事件。 它会打印您在屏幕上单击的消息。 您可以在处理程序中拥有任何Python语句。
 



[140]

 
交互式的小工具

   最后，它将点击处理程序与我们创建的按钮相关联。 所以，现在，当用户点击我们的按钮时，处理程序被调用并且按钮被点击的消息显示在屏幕上（如以下屏幕截图所示）。

如果我们在笔记本上运行这个脚本，并点击几次按钮，我们得到如下的显示：

![](/assets/we.jpg)
