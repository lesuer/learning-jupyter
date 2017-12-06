### 按钮小部件
****
同样，我们可以在我们的脚本中使用一个按钮小部件。 例如，采取以下脚本：



```
from ipywidgets import widgets

from IPython.display import display

button = widgets.Button(description="Submit"); display(button)

def on_button_clicked(widget):

print("Clicked Button:" + widget.description); button.on_click(on_button_clicked);


```
该脚本执行以下操作：

   从小部件包引用我们想要使用的功能。

   创建我们的按钮。

   为按钮上的单击事件定义处理程序。 处理程序接收被点击的按钮对象（widget）。

   在处理程序中，我们显示关于点击按钮的信息（可以想象，如果我们在显示中有几个按钮，我们将要确定哪个按钮被点击）。

   最后，它将定义的处理程序分配给我们创建的按钮对象。

处理程序编码的缩进 - 这是必须遵循的标准Python风格。
 













[134]

 
交互式的小工具

如果我们在笔记本上运行这个脚本，我们得到如下的显示：

![](/assets/vc.jpg)

请注意屏幕截图底部的提交按钮。 您可以更改按钮的其他属性，例如其位置，大小，颜色等。
 




















[135]

 
交互式的小工具

如果我们点击提交按钮，我们得到如下的显示：

![](/assets/nb.jpg)

现在显示关于点击按钮的消息。
