### 安装Scala内核
****
目前还没有在Windows环境下安装Scala内核的过程。 我不知道为什么。 我预计这会随着时间而改变。

这里给出Mac OS / X的步骤（摘自https://developer.ibm.com/hadoop/ 2016/05/04 / install-jupyter-notebook-spark）：

1. 使用这个安装GIT：

yum install git

2. 在本地复制Scala包：

git clone https://github.com/alexarchambault/jupyter-scala.git

3. 运行以下命令安装sbt构建工具：
 

sudo yum install sbt
 

 

4.移动到Scala包目录：

cd jupyter-scala

5. 构建包：

sbt cli/packArchive

6.要启动Scala shell，请使用以下命令：

./jupyter-scala

7.通过运行这个命令检查安装的内核：（你现在应该在列表中看到Scala）：

jupyter kernelspec list

8. 启动Jupyter笔记本电脑：

jupyter notebook

9. 你现在可以选择使用Scala 2.11 shell。

At this point, if you start Jupyter, you will see the choice for Scala listed:

![](/assets/没空看.jpg)

如果我们创建一个Scala笔记本，我们最终会看到一个熟悉的布局，其中一个图标显示我们正在运行Scala，引擎类型字符串标识为Scala 2.11：

![](/assets/i回复.jpg)

所以，通过将我们的笔记本命名为Scala Notebook并保存，我们就可以在主页上看到熟悉的笔记本显示，新笔记本被称为Scala Notebook.ipynb。

如果我们查看IPYNB文件，我们可以看到与其他笔记本类型相似的标记，具有Scala的特殊标记：




```
{

...

"metadata": { "kernelspec": {

"display_name": "Scala 2.11",

"language": "scala211",

"name": "scala211" }, "language_info": {

"codemirror_mode": "text/x-scala",

"file_extension": ".scala", "mimetype": "text/x-scala", "name": "scala211", "pygments_lexer": "scala",

"version": "2.11.8"

}

...

}
 







[ 180 ]


```
现在，我们可以在一些单元格中输入Scala编码。 以前的语言例子（从前面的章节），我们可以输入：



```
val name = "Dan" val age = 37

show(name + " is " + age)
```



show命令可能无法在某些环境中使用，您可以改为使用print命令。 Scala具有可变变量（var）和固定变量（val）。 我们不会改变字段，所以它们是val变量。 最后一条语句显示，是一个用于Scala中的Jupyter扩展来显示一个变量。

如果我们在Jupyter中运行这个脚本，我们看到以下内容：

请注意，目前有一个连接使用Safari的问题，连接到Firefox运行良好。 在单元格的输出区域，我们看到期望的Dan是37.有趣的是，Scala还显示了当前脚本中每个变量的当前类型和值。
 














[181]

