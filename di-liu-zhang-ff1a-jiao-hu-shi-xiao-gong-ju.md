
### 交互式的小工具


有一种为Jupyter在脚本运行时从用户收集输入的机制。为此，我们在脚本中以小部件或用户界面控件的形式进行编码。我们将在本章中使用的小部件在http：//ipywidgets.readthedocs.i中定义

O / EN /最新/。

有以下小部件：

  文本输入：笔记本用户输入稍后将在脚本中使用的字符串。

  按钮点击：用户以按钮的形式呈现多个选项;然后，根据选择哪个按钮（点击），脚本可以根据用户改变方向。
  滑块：您可以为用户提供一个滑块，用户可以使用该滑块在您指定的范围内选择一个值，然后脚本可以相应地使用该值。
  切换框和复选框：用户选择他们感兴趣的脚本的不同选项。

  进度条：如果你的脚本需要一些时间来处理，那么提供一个进度条会让他们有一些想法来完成它。类似地，可以使用进度条来显示在多步骤过程中多远。

  您可以从用户处收集的输入类型有一些限制。所以，你可以做出非常有趣的小部件，不符合标准的用户输入控制范例。例如，有一个小部件（ipyleaflet）允许用户点击一个地理地图，其中底层脚本将获得所选的地理数据点，并相应地进行操作。
 
交互式的小工具

在本章中，我们将介绍以下主题：

  安装小部件

  小部件的基本知识

  交互小部件

  互动小部件

  小工具包