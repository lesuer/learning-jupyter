### 小部件容器

您还可以通过在构造函数中传递子元素来直接使用Python语法来组装容器的小部件。 例如，我们可以有以下脚本：


```
from ipywidgets import *

from IPython.display import display slider = widgets.FloatSlider()

message = widgets.Text(value='Hello World') container = widgets.Box(children=[slider, message])
 

[ 141 ]

 
Interactive Widgets

container.layout.border = '1px black solid' display(container)

```
在这里，我们正在创建一个容器（这是一个盒子小部件），我们正在指定包含子控件的控件。 显示容器的调用也会迭代地显示子元素。 所以，我们最终得到如下的显示：

![](/assets/ou.jpg)

您可以在框中看到边框和框中的两个控件。

同样，我们可以在容器显示之后使用如下语法将子项添加到容器中：


```
from ipywidgets import *

from IPython.display import display container = widgets.Box() container.layout.border = '1px black solid' display(container)

slider = widgets.FloatSlider()

message = widgets.Text(value='Hello World') container.children=[slider, message]

```
当我们将孩子添加到容器中时，容器将重新绘制，这将导致重绘任何儿童。
 




[142]

 
交互式的小工具

如果我们在另一个笔记本上运行这个脚本，我们会得到与前面例子非常相似的结果：

![](/assets/dv.jpg)


