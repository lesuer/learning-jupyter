### 在Mac上添加JavaScript脚本到Jupyter

在Mac上的Jupyter中使用JavaScript需要几个步骤。 Mac上的Jupyter也被称为

IJavascript。 明确的网站是https://www.npmjs.com/package/ijavascript，专门为Jupyter提供了JavaScript内核。

在安装页面（http://n-riesco.github.io/ijavascript/doc/install.md.ht ml），我们可以遵循macOS（当前Mac操作系统）的指导原则：


```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" brew install pkg-config node zeromq

sudo easy_install pip

sudo pip install -U jupyter npm install ijavascript

```
我们可以用ijs命令启动我们的笔记本。

该命令在OSX下不可用，除非指定了-g选项。
 

















[102]

 
Jupyter JavaScript编码

你应该看到一个JavaScript笔记本可用，如下图所示：
![](/assets/你.jpg)

