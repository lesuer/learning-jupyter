### 微件属性

所有小部件的控件都有一组属性，可以根据需要为显示进行调整。 您可以通过获取控件的实例并在笔记本中运行control.keys命令来查看属性列表。 例如，看下面的脚本：



```
from ipywidgets import * w = IntSlider()

w.keys
 

```
该脚本全面引用了小部件中可用的所有控件。 然后，我们创建一个IntSlider实例，并显示我们可以调整的属性的可能列表：

![](/assets/iy.jpg)

正如你所看到的，名单是广泛的。 下表更详细地显示了列表：

![](/assets/图像 6.png)

我们可以使用类似下面的示例脚本来调整脚本中的任何脚本（禁用文本框（文本框将显示，但用户无法在文本框中输入值））：


```
from ipywidgets import *

Text(value='You can not change this text!', disabled=True)

```
![](/assets/er.jpg)

当一个字段被禁用时，文本框会变灰，当用户将光标悬停在字段上时，会出现一个红色圆圈，表示不能更改。



