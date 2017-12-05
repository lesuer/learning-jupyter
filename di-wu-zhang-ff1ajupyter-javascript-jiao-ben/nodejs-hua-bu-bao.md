### Node.js画布包

画布包用于在Node.js中生成图形。 我们可以使用Canvas主页中的示例（https://www.npmjs.com/package/canvas）。

首先，我们需要安装画布及其依赖项。 主页上有不同操作系统的指示，但是我们之前看到的工具（我们已经看到它们是macOS）非常熟悉：

npm安装画布

brew安装pkg-config cairo libpng jpeg giflib

通过在您的机器上安装画布包，我们可以使用一个小的Node.js脚本来创建一个图形：


```
//	create a canvas 200 by 200 pixels var Canvas = require('canvas')

,	Image = Canvas.Image

,	canvas = new Canvas(200, 200)

,	ctx = canvas.getContext('2d')

,	string = "Jupyter!";

//	place our string on the canvas ctx.font = '30px Impact'; ctx.rotate(.1); ctx.fillText(string, 50, 100); var te = ctx.measureText(string);

ctx.strokeStyle = 'rgba(0,0,0,0.5)'; ctx.beginPath();

ctx.lineTo(50, 102); ctx.lineTo(50 + te.width, 102); ctx.stroke();

//create an html img tag, with embedded graphics console.log('<img src="' + canvas.toDataURL() + '" />');

```
这个脚本创建一个画布，写字符串Jupyter！ 穿过画布，然后用图形生成一个HTML img标签。
 












[112]

 
Jupyter JavaScript编码

在笔记本中运行脚本之后，我们将img标签作为输出：

![](/assets/他.jpg)

我们可以将img标签保存到HTML页面，然后用浏览器打开HTML文件以显示我们的图形：
![](/assets/与.jpg)
