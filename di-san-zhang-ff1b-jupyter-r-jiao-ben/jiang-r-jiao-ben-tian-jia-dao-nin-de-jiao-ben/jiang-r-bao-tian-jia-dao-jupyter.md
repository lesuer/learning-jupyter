Jupyter R脚本

将R包添加到Jupyter

在Jupyter下R的标准安装有很多R程序中常用的软件包。 但是，如果您确实需要添加其他软件包，则需要执行以下步骤：

1.关闭笔记本电脑（包括服务器）。

2.在命令行窗口中，输入以下内容：


```
R

install.packages("name of the R package you want to add") quit()

#	answer Yes to save

```

3.重新启动你的笔记本，这个软件包应该可以在你的R脚本中使用。 要使用已安装的软件包，请键入library（要添加的R软件包的名称）。

请注意，如果您安装的R的核心版本已过期，并且您需要升级以使用特定的库，则在R中可能仍然存在问题。