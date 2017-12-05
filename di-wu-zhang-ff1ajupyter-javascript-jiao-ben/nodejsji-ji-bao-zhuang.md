### Node.js积极包装
****
积极地是一个工作与大多数不同的包。 要使用他们的软件，您必须注册一个用户名，并提供一个API密钥（在https://plot.ly/）。 然后，您将用户名和API密钥放置在您的脚本中。 在这一点上，你可以使用所有的情节特征。

首先，像其他软件包一样，我们需要安装它：

npm安装情节

一旦安装完毕，我们可以根据需要参考剧情包。 使用一个简单的脚本，我们可以绘制一个直方图：


```
//set random seed

var seedrandom = require('seedrandom'); var rng = seedrandom('Jupyter');

//setup plotly

var plotly = require('plotly')(username="<username>", api_key="<key>") var x = [];

for	(var i = 0; i < 500; i ++) { x[i] = Math.random();

}

require('plotly')(username, api_key); var data = [

{

x: x,

type: "histogram"

}

];

var graphOptions = {filename: "basic-histogram", fileopt: "overwrite"}; plotly.plot(data, graphOptions, function (err, msg) {

console.log(msg);

});
 
















[ 114 ]


```
Jupyter JavaScript编码

一旦加载并运行在Jupyter作为笔记本，我们得到以下截图：


![](/assets/人.jpg)

不是创建本地文件，或者只是在屏幕上显示图形，任何图形都会创建并存储在绘图站点上，而plot命令的输出是图形创建时的一组返回值。 最重要的是您可以访问图形的URL。
 








[115]

 
Jupyter JavaScript编码

所以理想情况是，我应该能够使用提供的URL（https://plot.ly/~dantoomey/1）来访问我的图形（直方图）。 返回的URL按预期工作，在URL中插入波形符号。 但是，当我环顾四周，我确实发现我的图形与预期略有不同。 所有的图形都在你的主页上，例如https://plot.ly/~dantoomey。 我现在可以访问我所有的图形和直方图显示：

![](/assets/成.jpg)
