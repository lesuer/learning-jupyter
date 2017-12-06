### Mac安装
 

要安装，我们从https：// spar k.apache.org/downloads.html的Spark下载页面下载最新的TGZ文件，解压缩TGZ文件，并将解压后的目录移动到我们的应用程序文件夹中。
 
Jupyter和大数据

Spark依靠Scala的可用性。 我们在第7章共享和转换Jupyter笔记本中安装了Scala。

打开Spark目录的命令行窗口并运行以下命令：

酿造安装sbt

可能还要等一下。

现在在你的.bash_profile文件中设置Spark（for Mac）的配置：


```
# location of spark code

export SPARK_HOME="/Applications/spark-2.0.0-bin-hadoop2.7"

# machine to run on

export SPARK_MASTER_IP=127.0.0.1 export SPARK_LOCAL_IP=127.0.0.1

# python location

export PYTHONPATH=$SPARK_HOME/python/:$PYTHONPATH export PYTHONPATH=$SPARK_HOME/python/lib/py4j-0.10.1-

src.zip:$PYTHONPATH

```
请注意，使用的路径将与您的安装相对应

您现在应该可以在Spark目录中运行此命令，并成功在Spark中打开一个命令行窗口：

bin/ pyspark

它看起来像这样（取决于版本）：


```
Welcome to

____	__

/ __/__  ___ _____/ /__

_\ \/ _ \/ _ `/ __/  '_/

/__ / .__/\_,_/_/ /_/\_\   version 2.0.0

/_/

Using Python version 2.7.12 (default, Jul 2 2016 17:43:17) SparkSession available as 'spark'.

>>>

```
你可以输入quit（）退出。

现在，当我们运行我们的笔记本时，当使用Python内核时，我们可以访问Spark。
 







[198]


