### Jupyter中的Python数据访问
****
现在我们已经看到了Python如何在Jupyter中工作，包括底层编码，那么Python如何在Jupyter中访问大型数据集？

我开始使用Python数据访问作为名称的大熊猫的另一种观点。 从这里，我们将读入一个大的数据集，并计算一些标准的数据统计。 我们感兴趣的是如何在Jupyter中使用熊猫，脚本的表现如何，元数据中存储了哪些信息（特别是如果它是一个更大的数据集）。

我们的脚本访问内置于其中一个Python包中的虹膜数据集。 我们所要做的就是读取略微多的项目并计算数据集上的一些基本操作。 我们真的很感兴趣，看看有多少数据被缓存在IPYNB文件中

Python代码如下：


```

#	import the datasets package from sklearn import datasets

#	pull in the iris data

iris_dataset = datasets.load_iris()

#	grab the first two columns of data

X = iris_dataset.data[:, :2]

#	calculate some basic statistics

x_count = len(X.flat) x_min = X[:, 0].min() - .5 x_max = X[:, 0].max() + .5 x_mean = X[:, 0].mean()

# display our results x_count, x_min, x_max, x__mean
```
我在Jupyter中将这些步骤分解成了几个单元格，如下图所示：

![](/assets/46.jpg)



