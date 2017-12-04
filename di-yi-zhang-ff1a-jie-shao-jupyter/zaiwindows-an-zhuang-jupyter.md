### 在Windows上安装Jupyter
****
Jupyter需要安装Python（它基于Python语言）。 有几个工具可以自动从GUI中安装Jupyter（也可以是Python）。 在这种情况下，我们展示了如何使用Anaconda进行安装，这是一个用于分发软件的Python工具。 你首先必须安装Anaconda。 它可以在Windows和Mac环境中使用。 从https://www.continuum.io/（生成Anaconda的公司）下载可执行文件并运行它来安装Anaconda。 该软件提供了一个常规的安装过程，如下图所示：
![](/assets/14.jpg)

安装过程经过了使您同意分配权许可证的常规步骤：


![](/assets/15.jpg)


标准的Windows安装允许您决定机器上的所有用户是否可以运行新软件。 如果您要共享具有不同级别用户的计算机，则可以决定适当的操作：

![](/assets/16.jpg)


点击下一步后，它将要求软件驻留的目的地（我几乎总是保持默认路径）：
 














[16]
****

![](/assets/17.jpg)

最重要的是，确保使用Anaconda安装的Python提供了Python基础（通过放置在执行路径中）。 请记住，Anaconda本身使用Python工具，所以这很重要。

**这个过程需要一些时间来下载和安装**。




一旦安装了Anaconda，就需要运行命令行指令来安装Jupyter。 命令如下：

**conda install jupyter
 **
****

这将调用一个过程，将Jupyter的所有必要组件下载到PC上。 你的输出应该是这样的：


```
C:\Users\Dan>conda install jupyter

Using Anaconda Cloud api site https://api.anaconda.org

Fetching package metadata: ....

Solving package specifications: .........

# packages in environment at C:\Users\Dan\Anaconda2:

#

jupyter	1.0.0	py27_2

```
额外的行将出现一个安装。 我缩小了输出。 你现在已经在你的机器上安装了Jupyter。 您可以使用以下命令启动进程：

C:\Users\Dan>jupyter notebook

这个命令在你的机器上启动Jupyter Notebook服务器。 一旦服务器启动，浏览器实例将在笔记本的开始点打开。 在服务器启动时，您应该在计算机上看到类似于以下内容的日志记录：


```
[I 16:21:59.144 NotebookApp] Writing notebook server cookie secret to

C:\Users\Dan\AppData\Roaming\jupyter\runtime\notebook_cookie_secret

[I 16:21:59.846 NotebookApp] Serving notebooks from local directory:

C:\Users\Dan

[I 16:21:59.846 NotebookApp] 0 active kernels

[I 16:21:59.846 NotebookApp] The Jupyter Notebook is running at: http://localhost:8888/

[I 16:21:59.862 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).


```
一旦Jupyter运行，你会注意到屏幕底部的Jupyter（两个倒立的新月）的运行图标：
 















[18]

 
Jupyter简介

请注意，日志的最后一行是您必须用来停止服务器的指令（在运行服务器的命令行窗口中按Ctrl + C）。

如果您在该窗口中按Ctrl + C，Jupyter服务器将优雅地关闭：


