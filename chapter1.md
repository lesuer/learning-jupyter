### 前言
****

学习Jupyter讨论使用Jupyter来记录您的脚本和数据分析项目的结果。 Jupyter允许数据科学家记录他们完整的分析过程，这与其他科学家使用实验记录记录测试，进度，结果和结论的方式大致相同。 Jupyter适用于各种操作系统，本书涵盖了在Windows和Mac OS X中使用Jupyter以及满足特定需求所需的各种步骤。 Jupyter通过添加语言引擎来支持各种脚本语言，因此用户可以在其中原生地描绘脚本。

**这本书涵盖了什么**

第1章“Jupyter简介”首先介绍了Jupyter用户界面，介绍了如何在Windows和Mac OS X上安装Jupyter，并通过所有引擎的用户界面来检查Jupyter Notebook的基本操作，并概述了安全功能可用和配置选项。

第2章，Jupyter Python Scripting，介绍了一个简单的Python笔记本和底层结构。本章还介绍了在Python脚本中使用熊猫，图形和使用随机数的例子。

第3章，Jupyter R Scripting，增加了在Jupyter Notebook中使用R脚本的能力，增加了一个不包含在标准R安装中的R库，在R中创建了一个Hello World脚本，并且显示了R数据访问和内置库一些更简单的图形和统计数据是自动生成的。我们使用R脚本以几种不同的方式生成3D图形，执行聚类分析，并使用R中可用的预测工具之一。

第4章，Jupyter Julia Scripting，增加了在Jupyter Notebook中使用Julia脚本的功能，增加了一个不包含在标准Julia安装中的Julia库，并展示了Julia的基本功能。我们概述了在Jupyter中使用Julia以及使用一些可用的图形包（包括Gadfly，Winston，Vega和Pyplot）来显示图形的一些限制。我们展示了并行处理，一个小的控制流程示例，以及如何将单元测试添加到您的Julia脚本。
 
前言
****
第5章Jupyter JavaScript Coding展示了如何在Jupyter Notebook中添加JavaScript，在Jupyter中使用Javascript的一些限制，以及几个包含Node.js代码示例的包的例子，包括用于图形的d3，统计分析，内置的JSON处理，用于创建图形文件的Canvas以及用于通过第三方工具生成图形的Plotly。您将了解如何使用Jupyter中的Node.js开发多线程应用程序，并使用机器学习来开发决策树。

第6章“交互式小部件”将小部件添加到我们的Jupyter安装中，使用交互式和交互式小部件来生成各种用户输入控件。我们深入地解释了小部件包，以调查可用的用户控件，容器中可用的属性以及从控件发出的事件。您将看到如何构建控件的容器。

第7章共享和转换Jupyter笔记本，在笔记本服务器上共享笔记本，向笔记本服务器添加笔记本，使用GitHub在笔记本上分发笔记，并将笔记本转换为不同的格式，如HTML和PDF。

第8章，多用户Jupyter笔记本，公开笔记本，以便多个用户可以同时使用笔记本，并显示发生多用户错误的示例。我们将安装一个Jupyter服务器来克服多用户问题，并使用Docker来缓解这个问题。

第9章，Jupyter Scala，为Jupyter安装Scala，使用Scala编码来访问更大的数据集，展示Scala如何操作数组，以及如何在Scala中生成随机数。有一些高阶函数和模式匹配的例子，用例类和Scala中的不变性。我们使用Scala包构建集合，并展示Scala特性的使用。

第10章Jupyter和Big Data通过Python为Jupyter编写了Spark功能，在Windows机器和Mac机器上安装Spark Jupyter，并显示刚刚读取文本文件中的行的初始脚本。我们还可以确定该文件中的字数，对结果进行排序，使用脚本来估计pi，评估web日志文件中的异常情况，确定一组素数，并评估文本流的某些特征。
 
**
这本书你需要什么**

本书中的步骤假定您有一台可以访问Internet的现代Windows或Macintosh机器。有几点你需要安装软件，所以你需要管理权限的机器这样做。

**这本书是谁的**

本书是为希望在自然编程环境中将软件描述给其他人的用户编写的。 Jupyter提供了执行许多不同语言和存储t的机制


```
{

"cells": [

<<same format as seen earlier for the cells>>

],

"metadata": {

"kernelspec": {

"display_name": "Javascript (Node.js)", "language": "javascript",

"name": "javascript"

},

"language_info": { "file_extension": ".js",

"mimetype": "application/javascript", "name": "javascript",

"version": "4.2.4"

}

}, "nbformat": 4,

"nbformat_minor": 0

}
 


[ 3 ]



```
任何命令行输入或输出如下所示：

Pkg.add（ “DataFrames”）

Pkg.add（ “RDatasets”）

Pkg.add（ “牛虻”）

quit（）;

新术语和重要词汇以粗体显示。例如，在屏幕上看到的单词或对话框中的文字会显示在文本中，如下所示：“上传按钮用于将文件添加到笔记本电脑空间。

警告或重要的笔记就像这样出现在一个盒子里。




提示和技巧是这样的。





**读者反馈**

我们欢迎读者反馈。让我们知道你对这本书的看法 - 你喜欢或不喜欢的东西。读者反馈对我们非常重要，因为它可以帮助我们开发您真正能从中获益最多的标题。给我们一般的反馈，

mail feedback@packtpub.com，并提及本书的标题在您的消息的主题。如果您有一个专业知识的话题，并且您对写作或撰写书籍感兴趣，请参阅我们的作者指南，网址为www.packtpub.com/authors。

**客户支持**

既然您是Packt书的自豪拥有者，我们有许多事情可以帮助您从购买中获得最大收益。

**下载示例代码**

您可以从http：//www.p acktpub.com上的帐户下载本书的示例代码文件。如果您在其他地方购买了此书，则可以访问http://www.packtpub.c om / support并注册，以便将文件直接发送给您。
 


您可以通过以下步骤下载代码文件：

1.使用您的电子邮件地址和密码登录或注册我们的网站。

2.将鼠标指针悬停在顶部的SUPPORT选项卡上。

3.点击Code Downloads＆Errata。

4.在搜索框中输入书名。

5.选择您要下载代码文件的书。

6.从您购买本书的下拉菜单中选择。

7.点击代码下载。

一旦文件被下载，请确保您使用最新版本的解压缩或解压缩文件夹：

  用于Windows的WinRAR / 7-Zip

  适用于Linux的Zipeg / iZip / UnRarX for Mac 7-Zip / PeaZip

本书的代码包也在https://github.com/PacktPubl ishing / Learning-Jupyter的GitHub上托管。我们还从https://github.com/PacktPublishing/提供了丰富的书籍和视频目录中的其他代码包。去看一下！

**下载本书的彩色图像**

我们还为您提供PDF文件，其中包含本书中使用的截图/图表的彩色图像。彩色图像将帮助您更好地理解输出中的变化。您可以从https://www.packtpub.com/sites/default/files/down下载此文件

负载/ LearningJupyter_ColorImages.pdf。

**勘误表**

尽管我们已经尽力确保内容的准确性，但错误确实发生了。如果您在我们的某本书中发现错误（可能是文本或代码中的错误），我们将不胜感激，如果您可以向我们报告。通过这样做，可以让其他读者免于挫折，帮助我们改进本书的后续版本。如果您发现勘误，请访问http://www.packtpub.com/submit-errata，选择您的书籍，点击勘误提交表格链接，并输入您的勘误详情。一旦您的勘误被验证，您的提交将被接受，勘误将被上传到我们的网站或添加到该标题的勘误部分下的现有勘误表的任何列表。
 

要查看以前提交的勘误表，请访问https://www.packtpub.com/books/conten t / support并在搜索字段中输入书名。所需的信息将出现在勘误部分下。
**
海盗行为**

互联网上受版权保护的材料的盗版是所有媒体中一直存在的问题。在Packt，我们非常重视保护我们的版权和许可证。如果您在互联网上发现任何非法复制的作品，请立即向我们提供地址或网站名称，以便我们寻求补救措施。

请通过copyright@packtpub.com与我们联系，并附有可疑的盗版材料的链接。

感谢您的帮助，保护我们的作者和我们为您提供有价值内容的能力。
**
问题**

如果您对本书的任何方面有疑问，请联系我们

在questions@packtpub.com，我们将尽我们所能解决这个问题。
 



























[6]

