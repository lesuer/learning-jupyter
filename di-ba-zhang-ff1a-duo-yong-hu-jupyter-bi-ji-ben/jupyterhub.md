### JupyterHub

一旦Jupyter笔记本被共享，显然多用户问题必须得到解决。 开发了Jupyter软件的新版本，名为JupyterHub。 JupyterHub专为处理多个用户而设计，为每个用户提供自己的一组变量。 实际上，系统会给每个用户一个全新的Jupyter软件实例给每个用户 - 这是一种强力的方法，但是它是有效的。

当JupyterHub启动时，它启动一个集线器或控制代理。 集线器将为Jupyter请求启动侦听器或代理的实例。 当代理得到Jupyter的请求时，它将把它转到集线器。 如果集线器决定这是一个新用户，它将生成Jupyter服务器的一个新实例，并将该用户和Jupyter之间的所有进一步交互附加到他们自己的服务器版本。