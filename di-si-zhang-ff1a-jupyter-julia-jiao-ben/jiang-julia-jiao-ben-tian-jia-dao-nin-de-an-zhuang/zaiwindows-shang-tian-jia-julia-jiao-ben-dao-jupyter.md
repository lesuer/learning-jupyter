### 在Windows上添加Julia脚本到Jupyter
****
如果你在Windows机器上运行，有几个步骤可以让Jupyter上的Julia。 请记住，这个环境确实是为Linux开发的。
 













[79]

 
Jupyter Julia脚本

首先，我们需要在Windows机器上安装Julia。 导航到Julia下载页面（http://julialang.org/downloads/），下载正确的版本，这是Windows的Julia 0.4.5（在我的情况下，我使用Windows自解压EXE文件的32位 机器），并以标准默认值运行安装。

您必须在您的机器上以管理员身份运行Julia安装。 下载文件后，打开下载文件夹，右键单击Julia可执行文件，然后选择以管理员身份运行。

一旦安装完成，你应该验证一切正常。 从程序列表中选择Julia并运行Julia程序。 您应该看到Julia命令行，如以下屏幕截图所示：



![](/assets/67.jpg)


在Julia窗口中，运行以下命令将Julia添加到Jupyter：

Pkg.add（“IJulia”）
 










[80]

 
Jupyter Julia脚本

这将导致IJulia（交互式Julia）被下载并安装在您的机器上。 有很多子包也会自动安装。 您的显示器将如下图所示：


![](/assets/68.jpg)

Julia使用字体颜色作为反馈。 我在屏幕顶部输入了白色文本Pkg.add，成功的执行步骤是蓝色的，可能的问题显示为红色。 您必须等待安装完成。 最后一行应该如下所示：

信息：包数据库已更新

此时，可以关闭Julia窗口（使用quit（）命令）。
 












[81]

 
Jupyter Julia脚本

最后一步是打开笔记本（使用jupyter笔记本命令），如果打开新建菜单（位于屏幕的右上角），您应该看到一个Julia类型，如以下屏幕截图所示：


![](/assets/69.jpg)