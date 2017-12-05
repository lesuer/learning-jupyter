R聚类分析

在这个例子中，我们使用R的聚类分析函数来确定来自http://www.ics.uci.edu/的小麦数据集中的聚类。
 






[72]

 
Jupyter R脚本

我们想要在Jupyter中使用的R脚本如下：


```
# load the wheat data set from uci.edu wheat <-

read.csv("http://archive.ics.uci.edu/ml/machine-learning-databases/00236/se eds_dataset.txt", sep="\t")

# define useful column names

colnames(wheat) <-c("area", "perimeter", "compactness", "length", "width", "asymmetry", "groove", "undefined")

#	exclude incomplete cases from the data wheat <- wheat[complete.cases(wheat),]

#	calculate the clusters

fit <- kmeans(wheat, 5) fit

Once entered into a notebook, we have something like this:

```
![](/assets/463.jpg)

由此产生的聚类信息是具有五个大小为29,57,65,15和32的簇的K均值聚类。（请注意，由于我没有设置用于随机数的种子值，因此您的结果可能会有所不同。）

集群手段是：


```

			area perimeter compactness		length		width asymmetry			
	1	16.45345		15.35310		0.8768000	5.882655	3.462517	3.913207			
	2	14.06456		14.17175		0.8788158	5.463825	3.211526	2.496354			
	3	11.91292		13.26692		0.8496292	5.237477	2.857908	4.844477			
	4	19.58333		16.64600		0.8877267	6.315867	3.835067	5.081533			
	5	18.95781		16.39563		0.8862125	6.250469	3.742781	2.719813			
Clustering vectors are:														
		1	2	3	4	5	6	9	10	11	12	13	14	15	16	17	18	19	20
21	22																		
		2	2	2	2	2	2	1	1	1	2	2	2	2	2	2	2	2	2

2	2

...

Within cluster sum of squares by cluster are:

[1]	54.16095 146.71080 147.29278  25.81297  30.06596

(between_SS / total_SS =  85.0 %)

The available components are:

[1]	"cluster"	"centers"	"totss"	"withinss"
"tot.withinss"			
[6]	"betweenss"	"size"	"iter"	"ifault"

所以，我们生成了五个集群的信息（在fit语句中传递的参数）。
```

