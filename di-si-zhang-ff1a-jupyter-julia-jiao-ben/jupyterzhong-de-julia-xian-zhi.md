### Jupyter中的Julia限制
****
我已经写了朱莉娅脚本和Jupyter没有问题访问不同的朱莉娅图书馆。 我没有注意到它的使用或性能下降的任何限制。 我想象一下Julia的一些非常依赖屏幕的方面（比如使用Julia Webstack构建一个网站）可能会受到相同概念冲突的阻碍。
 
















[86]

 
Jupyter Julia脚本

当我试图运行一个Julia脚本时，我曾多次看到更新正在运行，如下面的截图所示。 我不知道他们为什么决定总是更新底层工具，而不是使用正在使用的工具，并让用户指定是否更新库：


![](/assets/72.jpg)

我也注意到，一旦Julia笔记本被打开，即使我关闭了页面，它仍然会在主页上显示Running。我不记得看到与其他脚本语言可用的行为。

另一个问题一直在试图在我的脚本中使用一个安全的软件包，例如，阴谋。这似乎是一个干净的过程来获得凭据，但使用规定的方法传递您的凭据情节在Windows下不起作用。我很犹豫提供不适用于这两种环境的示例。

与Windows的进一步交互也是有限的，例如，试图通过调用通常不在Windows安装中的标准C库来访问环境变量。
 






[87]

 
Jupyter Julia脚本

我还有一个与Julia本身有关的问题 - 不管它是否在Jupyter中运行。

使用软件包时，会抱怨软件包中已被弃用或改进的功能。作为软件包的使用者，我无法控制这种行为，所以对我的工作没有帮助。