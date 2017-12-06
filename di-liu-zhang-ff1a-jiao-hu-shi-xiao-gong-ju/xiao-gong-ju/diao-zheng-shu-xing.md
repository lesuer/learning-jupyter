### 调整属性

以前显示的所有属性都可以读取和写入。 我们可以用一个小脚本来展示这个过渡：


```
from ipywidgets import * w = IntSlider() original = w.value w.value = 5

original, w.value


```
该脚本创建一个滑块，检索其当前值，将值更改为5，然后显示该控件的原始值和当前值。
 










[139]

 
交互式的小工具

如果我们要在笔记本上运行这个脚本，我们会看到以下结果：

![](/assets/vf.jpg)
