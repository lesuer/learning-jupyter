### 在Jupyter的基本R.

开始一个新的R笔记本电脑，并称之为R基础。 我们可以输入一个小脚本，这样我们就可以看到R脚本的步骤是如何进行的。 将以下内容输入到笔记本的单独单元格中：

myString < - “你好，世界！” print（myString）

您将会看到如下的开始屏幕：
 











[63]

 
Jupyter R脚本

![](/assets/118.jpg)
我们应该注意R笔记本视图的几个方面：

   我们在右上角有R标志。 你会看到这个标志运行在其他R安装。

   R图标下面还有一个特殊的R O。 未填充的圆圈表示内核处于静止状态，实心圆圈表示内核正在工作。

   其余的菜单项与我们之前见过的一样。

这是一个非常简单的脚本 - 在一个单元格中设置一个变量，然后在另一个单元格中输出它的值。 一旦执行（Cell | Run All），您将看到您的结果：

![](/assets/119.jpg)

所以，就像你在R解释器中运行脚本一样，你得到你的输出（用数字前缀）。 Jupyter已经对这些陈述进行了统计，所以我们对这些单元格进行了增量编号。 Jupyter没有做任何特别的事情来打印出调试的变量，你将不得不单独做这件事。
 


[64]

 
Jupyter R脚本

如果我们看看R服务器日志语句（我们启动Jupyter时创建了一个命令行窗口），我们看到发生的操作：



```
$ jupyter notebook

[I 11:00:06.965 NotebookApp] Serving notebooks from local directory:

/Users/dtoomey/miniconda3/bin

[I 11:00:06.965 NotebookApp] 0 active kernels

[I 11:00:06.965 NotebookApp] The Jupyter Notebook is running at: http://localhost:8888/

[I 11:00:06.965 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).

[I 11:00:17.447 NotebookApp] Creating new notebook in [I 11:00:18.199 NotebookApp] Kernel started:

518308da-460a-4eb9-9959-1411e31dec69

[1] "Got unhandled msg_type:" "comm_open"

[I 11:02:18.160 NotebookApp] Saving file at /Untitled.ipynb

[I 11:08:27.340 NotebookApp] Saving file at /R Basics.ipynb [1] "Got unhandled msg_type:" "comm_open"

[I 11:14:45.204 NotebookApp] Saving file at /R Basics.ipynb


```
我们启动服务器，创建一个新的笔记本，并将其保存为R基础。 如果我们打开磁盘上的IPYNB文件（使用文本编辑器），我们可以看到以下内容：



```
{

"cells": [

...<similar to previously displayed>

],

"metadata": {

"kernelspec": { "display_name": "R",

"language": "R", "name": "ir"
},

"language_info": { "codemirror_mode": "r", "file_extension": ".r", "mimetype": "text/x-r-source",
"name": "R",

"pygments_lexer": "r", "version": "3.2.2"

}

},

...<omitted>

}
 





[ 65 ]


```
这与我们在Python笔记本编码的前一章中看到的有点不同。 特别是，元数据清楚地告诉脚本单元是R脚本。 请注意，实际的单元格不是特定于某种语言的 - 它们只是将按照元数据执行的脚本

指令。





































