### Jupyter中的基本Python
****
在本章中，我们将在Jupyter Notebook中使用Python脚本。 Jupyter不会像脚本那样与脚本交互，而是执行脚本并记录结果。我认为这是如何Jupyter笔记本已被扩展到使用除Python以外的其他语言

笔记本只需要一个脚本，在语言引擎上运行它，并记录引擎的输出，而不是真的知道正在执行哪种脚本。

同样，在Jupyter中使用Python时，我没有注意到任何特殊的限制。我运行的一些脚本花了很多时间来运行，使用了大量的内存，打开了新的窗口等等，所有这些都没有失败。运行Python脚本的已知问题包含__main__执行循环和多线程应用程序。

我们必须在我们的笔记本上打开Python部分来使用Python编码。所以，启动你的笔记本，然后在右上角的菜单中选择Python 2。
 
Jupyter Python脚本

我在2016年春季在Windows机器和Mac上安装了Jupyter。他们都显示了Python 2的菜单选项。我知道在其他地方，需求讨论的是Python的后续版本，但Jupyter的安装版本是2.（实际上，在元数据显示中，它是2.7）

菜单显示在以下屏幕截图中：


![](/assets/34.jpg)

这将打开一个Python窗口，如下图所示：

![](/assets/35.jpg)


Jupyter Python脚本

如前一章所述，新窗口显示一个空单元格供您输入Python代码。

让我们给新的工作区域一个名字，学习Jupyter第2章。自动保存应该是（正如你可以看到标题旁边）。 用一个准确的名字，我们可以很容易地从笔记本主页找到这个部分。 如果您选择浏览器的“主页”选项卡并进行刷新，您将看到显示此新的窗口名称，如以下屏幕截图所示：

![](/assets/36.jpg)

请注意，它有一个项目图标与文件夹图标。 自动分配的扩展名是IPYNB（IPython Notebook）。 由于该项目在Jupyter环境中的浏览器中，因此被标记为正在运行。 在磁盘上的目录中也有一个按照该名称的文件，如以下屏幕截图所示：


![](/assets/37.jpg)

如果在文本编辑器中打开IPYNB文件，将会看到Jupyter节点的基本内容（如前一章的“笔记本结构”部分所述）。 我们有一个关于笔记本的空单元和元数据：


```
{

"cells": [

{

"cell_type": "code",

"execution_count": null,

"metadata": { "collapsed": true},
 

[ 38 ]

 
Jupyter Python Scripting

"outputs": [],

"source": []

}

], "metadata": {

"kernelspec": {

"display_name": "Python 2", "language": "python", "name": "python2"

},

"language_info": {

"codemirror_mode": {

"name": "ipython", "version": 2

},

"file_extension": ".py",

"mimetype": "text/x-python",

"name": "python", "nbconvert_exporter": "python",

"pygments_lexer": "ipython2",

"version": "2.7.11"

}

}, "nbformat": 4,

"nbformat_minor": 0

}

```
我们现在可以将Python编码输入到单元格中：

1.在第一个单元格中输入一些Python。

2.添加另一个单元格（使用Insert | Insert Cell在菜单命令下面）：

name = "Dan" age = 37

3.在第二个单元格中，输入引用第一个单元格变量的Python代码：

print(name + ' is ' + str(age) + ' years old.')

4.我们有这样的显示：



![](/assets/38.jpg)
 
请注意，Jupyter对Python进行了颜色编码（就像一个像样的编辑器一样），每个代码块的左边都有空括号。

如果我们执行Cell | 运行所有单元格，结果显示为内联：



![](/assets/39.jpg)

Jupyter Python脚本

我们现在用大小号填充大括号，单元格的输出被附加到每个单元格的底部。 需要注意的是单元格2能够引用在单元格1中声明的变量。

如果我们要等自动保存启动或者点击保存图标（软盘最左侧的图标），我们将使用我们的结果更新磁盘上的IPYNB文件：


```
{

"cells": [

{

"cell_type": "code",

"execution_count": 1,

"metadata": {

"collapsed": true

}, "outputs": [],

"source": [

"name = "Dan"\n",

"age = 37"

]

},

{

"cell_type": "code",

"execution_count": 2,

"metadata": { "collapsed": false

},

"outputs": [

{

"name": "stdout",

"output_type": "stream", "text": [

"Dan is 37 years old.\n"

]

}

], "source": [

"print(name + ' is ' + str(age) + ' years old.')"

]

}

],

... metadata as above

}
 






[ 41 ]


```
Jupyter Python脚本

有趣的是，Jupyter跟踪保存的文件版本和保存的检查点中最后生成的输出。 您也可以使用Cell |清除输出 所有输出| 清除命令。

如果您然后重新运行您的单元格（使用单元格|全部运行），输出将被重新生成（并通过自动保存保存）。 如果你这样做，单元格编号就会增加 - Jupyter正在跟踪每个单元格的最新版本。

同样，如果您要关闭浏览器选项卡，刷新主页选项卡中的显示，找到我们创建的新项目（学习Jupyter Chapter 2.pynb），然后单击它，将显示新选项卡（如前所创建的） 显示上次运行时产生的输出。

如果打开服务器命令行窗口（Jupyter服务正在运行），您将看到我们在会话期间所做的操作的列表，如以下屏幕截图所示：


![](/assets/45.jpg)


日志条目处于较高级别。 如果遇到一些困难，可能有办法提高日志记录级别。
 















[42]

 
Jupyter Python脚本






















