### 列表框部件

我们也可以在这个脚本中使用名为Dropdown的列表框小部件：


```
import ipywidgets as widgets

from IPython.display import display w = widgets.Dropdown(

options={'Pen': 7732, 'Pencil': 102, 'Pad': 33331}, description='Item:',

)

display(w)

w.value

```
这个脚本将显示一个列表框给用户，显示Pen，Pencil和Pad的值。 当用户选择其中一个值时，相关的值将返回给我们显示的w变量：

![](/assets/pl.jpg)

