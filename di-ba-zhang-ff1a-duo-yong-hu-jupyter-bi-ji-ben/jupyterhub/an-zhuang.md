### 安装

JupyterHub需要Python 3.3或更新版本，我们将使用pip3 Python工具来安装JupyterHub。 您可以通过在命令行中输入Python来检查您正在运行的Python版本; 序言会回显出当前版本：


```
Python

Python 3.6.0a4 (v3.6.0a4:017cf260936b, Aug 15 2016, 13:38:16)

[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin

Type "help", "copyright", "credits" or "license" for more information.


```
如果您需要升级到新版本，请参考https://www.python.or/go/上的说明，因为操作系统和Python版本特定。

JupyterHub与其他软件一样安装，使用以下命令：



```
npm install -g configurable-http-proxy pip3 install jupyterhub
```



首先，我们安装代理。 代理安装上的-g使得该软件可供所有用户使用：


```

npm install -g configurable-http-proxy

/usr/local/bin/configurable-http-proxy -> /usr/local/lib/node_modules/configurable-http-proxy/bin/configurable-http-proxy

/usr/local/lib

└─┬ configurable-http-proxy@1.3.0
├─┬ commander@2.9.0

│ └── graceful-readlink@1.0.1
 

[ 165 ]

 
Multiuser Jupyter Notebooks

├─┬ http-proxy@1.13.3

│	├── eventemitter3@1.2.0

│	└── requires-port@1.0.0 ├─┬ lynx@0.2.0

│	├── mersenne@0.0.3
│	└── statsd-parser@0.0.4
├── strftime@0.9.2 └─┬ winston@2.2.0 ├── async@1.0.0

├── colors@1.0.3
├── cycle@1.0.3
├── eyes@0.1.8
├── isstream@0.1.2 ├── pkginfo@0.3.1

└── stack-trace@0.0.9

Then we install JupyterHub:

pip3.6 install jupyterhub Collecting jupyterhub

Downloading jupyterhub-0.6.1-py3-none-any.whl (1.3MB)

100% |████████████████████████████████| 1.4MB
789kB/s

Collecting requests (from jupyterhub)

Downloading requests-2.11.1-py2.py3-none-any.whl (514kB)

100% |████████████████████████████████| 522kB
1.5MB/s

Collecting traitlets>=4.1 (from jupyterhub)

Downloading traitlets-4.2.2-py2.py3-none-any.whl (68kB)

100% |████████████████████████████████| 71kB
4.3MB/s

Collecting sqlalchemy>=1.0 (from jupyterhub)

Downloading SQLAlchemy-1.0.14.tar.gz (4.8MB)

100% |████████████████████████████████| 4.8MB
267kB/s

Collecting jinja2 (from jupyterhub)

Downloading Jinja2-2.8-py2.py3-none-any.whl (263kB)

100% |████████████████████████████████| 266kB
838kB/s

...
 



```



