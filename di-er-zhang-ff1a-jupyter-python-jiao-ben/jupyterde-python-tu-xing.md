### Jupyter Python脚本
****
Jupyter中的Python图形

Python图形如何在Jupyter中工作？

我为这个命名的Python图形开始了另一个视图，以区分以前的工作。

如果我们要建立一个宝宝名字的样本数据集，并在这个名字的一年内出生的人数，我们可以绘制数据。

Python编码很简单：


```
import pandas import matplotlib

%matplotlib inline

baby_name = ['Alice','Charles','Diane','Edward'] number_births = [96, 155, 66, 272]
dataset = list(zip(baby_name,number_births))

df = pandas.DataFrame(data = dataset, columns=['Name', 'Number']) df['Number'].plot()

```
脚本的步骤如下：

1.导入我们需要的图形库（和数据库）。

2.定义我们的数据。

3.将数据转换成允许简单图形显示的格式。

4.绘制数据。

我们会期望一个婴儿的名字出生人数的图表。
 



















[50]

 
Jupyter Python脚本

如果我们把前面的脚本放在Jupyter笔记本的单元格中，我们可以得到如下图所示的东西：

![](/assets/112.jpg)

为了便于阅读，我已将脚本分成不同的单元格。 拥有不同的单元格还允许您逐步开发脚本，并且可以显示迄今为止计算的值以验证结果。 我已经在大多数单元格中通过在这些单元格的底部显示数据集和DataFrame来完成此操作。
 











[51]

 
Jupyter Python脚本

当我们运行这个脚本（单元|全部运行）时，我们在脚本前进过程中看到每一步显示的结果：

![](/assets/113.jpg)

最后，我们看到我们的出生情节，如下图所示：

![](/assets/114.jpg)

我很好奇为这个脚本存储了什么元数据。 查看IPYNB文件，可以看到公式单元格的预期值。

DataFrame的表格数据显示以HTML方式存储：


```
{

"cell_type": "code", "execution_count": 43,

"metadata": { "collapsed": false

}, "outputs": [

{

"data": { "text/html": [

"<div>\n",

"<table border="1" class="dataframe">\n",

"<thead>\n",

"<tr style="text-align: right;">\n",

"<th></th>\n",

"<th>Name</th>\n",

"<th>Number</th>\n",

"</tr>\n",

"</thead>\n",
 

[ 53 ]

 
Jupyter Python Scripting

"<tbody>\n",

"<tr>\n",

"<th>0</th>\n",

"<td>Alice</td>\n",

"<td>96</td>\n",

"</tr>\n",

"<tr>\n",

"<th>1</th>\n",

"<td>Charles</td>\n",

"<td>155</td>\n",

"</tr>\n",

"<tr>\n",

"<th>2</th>\n",

"<td>Diane</td>\n",

"<td>66</td>\n",

"</tr>\n",

"<tr>\n",

"<th>3</th>\n",

"<td>Edward</td>\n",

"<td>272</td>\n",

"</tr>\n",

"</tbody>\n",

"</table>\n",

"</div>"

],

"text/plain": [

"	Name  Number\n",

"0	Alice	96\n",
"1	Charles	155\n",
"2	Diane	66\n",
"3	Edward	272"

]

},

"execution_count": 43, "metadata": {},

"output_type": "execute_result"

}

],

(... continued as above)

}

The graphic output cell is stored like this:

{

"cell_type": "code",

"execution_count": 27,

"metadata": { "collapsed": false
 

[ 54 ]

 
Jupyter Python Scripting

},

"outputs": [

{

"data": { "text/plain": [

"<matplotlib.axes._subplots.AxesSubplot at 0x47cf8f0>"

]

}, "execution_count": 27,

"metadata": {},

"output_type": "execute_result"

},

{

"data": {

"image/png":

"<a few hundred lines of hexcodes>

.../wc/B0RRYEH0EQAAAABJRU5ErkJggg==\n",

"text/plain": [ "<matplotlib.figure.Figure at 0x47d8e30>"

]

},

"metadata": {},

"output_type": "display_data"

}

],

"source": [

"# plot the data\n",

"df['Number'].plot()\n"

]

}

], (... similar coding as above for the file trailer)


```
“image / png”标签包含屏幕上显示的图形图像的大十六进制数字字符串表示（我缩写为所示编码中的显示）。 所以，实际生成的图像存储在页面的元数据中。

所以，Jupyter不是缓存，而是记住每个单元格上次执行时的输出。
