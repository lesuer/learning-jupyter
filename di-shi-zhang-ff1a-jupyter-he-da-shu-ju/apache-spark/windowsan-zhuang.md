### Windows安装

本书早些时候，我们已经安装了Python作为Jupyter安装的一部分。 我们需要从http：//spark.apache下载并安装最新的Spark版本
.ORG/ downloads.html。 解压缩TGZ文件并将生成的目录移动到
C：\ spark目录。

您还需要安装winutils.exe（这似乎是Hadoop安装中的一个问题，但可能会在某个时候得到解决）。 从http：// pub lic-repo-1.hortonworks.com/hdp-win-alpha/winutils.exe下载该文件并安装在

C：\ winutils\ bin中。

现在需要为所有这些设置环境变量：


```
HADOOP_HOME=C:\winutils

SPARK_HOME=C:\spark

PYSPARK_DRIVER_PYTHON=ipython

PYSPARK_DRIVER_PYTHON_OPTS=notebook

```




你可以使用pyspark命令启动Jupyter。 你不应该注意到你的笔记本有什么不同。

我们使用Python脚本来调用Spark功能，所以语言格式需要符合Python。