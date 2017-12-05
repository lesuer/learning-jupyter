### 将朱莉娅包添加到Jupyter
****
Jupyter中Julia的标准安装有许多Julia编程中常用的软件包。但是，如果您确实需要添加其他软件包，则需要执行以下步骤：

1.关闭笔记本电脑（包括服务器）。

2.运行Julia命令行程序并输入以下内容：

Pkg.add（ “DataFrames”）

Pkg.add（ “RDatasets”）

Pkg.add（ “牛虻”）

放弃（）;

3.重新启动您的笔记本电脑，应该在您的Julia脚本中提供该软件包。要使用已安装的软件包，请键入library（要添加的R软件包的名称）。
 






[82]

 
Jupyter Julia脚本

我建议马上添加三个前面的包，因为它们是许多脚本所需要的。

第一次在Julia使用一个包时，你会看到一条以浅红色突出显示的线，表示Julia正在预编译，比如：



INFO：预编译模块Dataframes ...

您可以直接在您的脚本中使用Pkg.add（...）函数，但这似乎不正确。每次运行脚本时，系统都会尝试验证您是否具有指定的包，如果需要的话将其安装到您的环境中，甚至告诉您是否过期。这些步骤都不属于您的脚本的一部分。