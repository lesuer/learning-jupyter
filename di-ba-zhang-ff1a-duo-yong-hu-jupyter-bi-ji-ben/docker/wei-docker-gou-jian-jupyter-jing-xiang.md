### 为Docker构建Jupyter镜像

Docker知道包含运行应用程序所需的整个软件堆栈的映像。 我们需要用笔记本建立一个图像并放置在Docker中。
 





[174]

 
多用户Jupyter笔记本

我们需要下载所有需要的Jupyter-Docker编码。 在Docker终端窗口中，我们运行docker pull jupyter / all-spark-notebook命令：


```
docker pull jupyter/all-spark-notebook

Using default tag: latest

latest: Pulling from jupyter/all-spark-notebook 8b87079b7a06: Pulling fs layer

872e508604af: Pulling fs layer

8e8d83eda71c: Pull complete

...
这是一个大的下载，需要一些时间。 它正在下载并安装在映像中运行Jupyter所需的所有必要组件。 请记住，每个图像是完全独立的，所以每个图像都有运行Jupyter所需的所有软件。

下载完成后，我们可以使用以下命令为笔记本启动映像：



```
docker run -d -p 8888:8888 -v /disk-directory:/virtual-notebook jupyter/all-spark-notebook

```
这个命令的部分如下：

   docker run：Docker开始执行映像的命令。

   -d：将图像作为服务器（守护进程）运行，该服务器将继续运行，直到用户手动停止。

   -p 8888：8888：将内部端口8888暴露给具有相同端口地址的外部用户。 笔记本默认情况下已经使用8888端口，所以我们只是说相同的端口。

   -v / disk-directory：/ virtual-notebook：从磁盘目录取出笔记本，并将其显示为虚拟笔记本名称。

   最后一个参数是使用全火花笔记本作为这个图像的基础。

就我而言，我使用了下面的命令：


```
$ docker run -d -p 8888:8888 -v /Users/dtoomey: /dan-notebook jupyter/all-spark-notebook

b59eaf0cae67506e4f475a9861f61c01c5af3556489992104c4ce39343e8eb02

```
显示的十六进制数字是图像标识符。
 






[175]

 
多用户Jupyter笔记本

我们可以使用docker ps -l命令来确保图像正在运行，该命令列出了Docker中的图像：


```


$ docker ps	-l		
CONTAINER ID	IMAGE		COMMAND
CREATED	STATUS	PORTS	
NAMES			
b59eaf0cae67	jupyter/all-spark-notebook	"tini -- start-
notebo"   8	seconds ago	Up 7 seconds	0.0.0.0:8888-
>8888/tcp	modest_bardeen		

```
显示器的部分如下：

   名字b59eaf0cae67是容器的分配ID。 Docker中的每个映像都分配给一个容器。

   图像是Jupyter /全火花笔记本电脑 - 它包含运行笔记本所需的所有软件。

   该命令告诉Docker启动映像。

   端口访问点如我们所料：8888。

   最后，Docker将随机名称分配给每个正在运行的映像; 我们是谦虚的巴丁（我不知道他们为什么这样做）。

在这一点上，我们应该能够从外部浏览器访问该笔记本电脑在http：// 192.168.99.100：8888。 当Docker启动时（192.168.99.100），我们看到了这个IP地址，我们正在使用我们指定的端口8888。 随后可以关闭现有的服务器：


![](/assets/3位v.jpg)
您可以在左上角看到该网址。 下面我们有一个标准的空白笔记本。
 

[176]

 
多用户Jupyter笔记本

所使用的Docker镜像具有所有最新的软件，因此您无需执行任何特殊操作即可获取笔记本电脑的更新软件或组件。 您可以通过下拉菜单来查看语言选项：

![](/assets/我哦位vv.jpg)

我们将在下一章讨论在笔记本中使用Scala。




