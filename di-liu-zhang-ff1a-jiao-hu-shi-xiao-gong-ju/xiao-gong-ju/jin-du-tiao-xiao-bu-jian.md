### 进度条小部件

这个软件包中的一个小部件向用户显示一个进度条。 采取以下脚本：



```
import ipywidgets as widgets widgets.FloatProgress(
value=45,

min=0,

max=100,

step=5,

description='Percent:',

)

```
这将显示我们的进度条，如下所示：

![](/assets/mn.jpg)
