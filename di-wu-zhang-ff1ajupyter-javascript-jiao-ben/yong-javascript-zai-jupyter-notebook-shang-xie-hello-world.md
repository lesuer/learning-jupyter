JavaScript的世界Jupyter笔记本

一旦安装完成，我们可以通过点击New菜单并选择JavaScript来尝试第一个JavaScript笔记本。 我们命名笔记本Hello World Javascript，并在脚本中添加以下几行：

var msg =“你好，世界！”执行console.log（味精）

这个脚本设置一个变量并显示变量的内容。 进入脚本并运行（Cell | Run All）后，我们将看到如下图所示的笔记本屏幕：

![](/assets/fever.jpg)

我们应该指出这个页面的一些亮点：

   我们在右上方有现在熟悉的语言标识，描述了正在使用的脚本的类型。

   从笔记本的每一行都有输出（Out）。 这似乎是一个正在进行的工作，因为行号是没有意义的。

   更重要的是，我们看到笔记本的真实输出（在前面的截图中的第2行），其中字符串被回显。

   否则，笔记本电脑看起来与我们所看到的其他类型很熟悉。
 







[104]

 
Jupyter JavaScript编码

如果我们看一下磁盘上笔记本的内容，我们也会看到类似的结果：


```
{

"cells": [

<<same format as seen earlier for the cells>>

],

"metadata": { "kernelspec": {

"display_name": "Javascript (Node.js)",

"language": "javascript",

"name": "javascript"

},

"language_info": { "file_extension": ".js",

"mimetype": "application/javascript",

"name": "javascript",

"version": "4.2.4"

}

},

"nbformat": 4,

"nbformat_minor": 0

}

```
因此，使用JSON文件格式的相同笔记本，通过适当地更改元数据和language_info值，Jupyter提供了用于笔记本的另一种语言。
