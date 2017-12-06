### 安装小部件

小部件包是对标准Jupyter安装的升级。 您可以使用以下命令更新小部件包：

pip install ipywidgets

请注意，如果您的计算机上已经安装了ipywidgets，则可能需要使用以下命令才能使升级生效：

pip install -upgrade ipywidgets

完成后，您必须使用以下命令升级Jupyter安装：

jupyter nbextension enable --py widgetsnbextension

您可能需要重新启动笔记本才能使分机生效。




如果您不安装软件包和升级，那么当您运行小部件脚本时，您将在显示屏中看到警告消息 - 安装的小部件JavaScript是

错误的版本：
 ![](/assets/kj.jpg)



我更新了我的安装，但仍收到一些屏幕的警告消息。 我认为在未来版本的软件中解决此警告消息错误是时间问题。









[123]