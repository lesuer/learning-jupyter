### 在Jupyter R 3D散点图
****
R格子包装具有将产生3D散点图的云功能。 我们将使用的脚本如下：


```
#	make sure lattice package is installed install.package("lattice")

#	in a standalone R script you would have a command to download the lattice library - this is not needed in Jupyter

library("lattice")

#	use the automobile data from ics.edu

mydata <-
 

[ 70 ]

 
Jupyter R Scripting

read.table("http://archive.ics.uci.edu/ml/machine-learning-databases/auto-m pg/auto-mpg.data")

# define more meaningful column names for the display

colnames(mydata) <- c("mpg", "cylinders", "displacement", "horsepower", "weight", "acceleration", "model.year", "origin", "car.name")

# 3-D plot with number of cylinders on x axis, weight of the vehicle on the y axis and miles per gallon on the z axis.

cloud(mpg~cylinders*weight, data=mydata)

运行之前，我们有这样的东西：
```
![](/assets/461.jpg)


请注意，我们正在使用标记类型单元格来评论脚本步骤。 它们也在左侧列中没有脚本行号。
 







[71]

 
Jupyter R脚本

如果您将R脚本复制到Jupyter窗口中，则可能会遇到以下问题：您使用的打印副本具有非标准的双引号字符（左侧的引号向左倾斜，右侧的引号向右倾斜）。 一旦复制到Jupyter，你需要改变这个正常的双引号（他们不倾斜，但是垂直）。

运行这个之后，我们看到下面的显示：

![](/assets/462.jpg)