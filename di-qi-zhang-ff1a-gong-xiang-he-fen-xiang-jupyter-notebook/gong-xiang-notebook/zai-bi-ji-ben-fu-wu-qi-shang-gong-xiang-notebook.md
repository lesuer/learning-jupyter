在笔记本服务器上共享笔记本

内置于Jupyter进程中的是将笔记本暴露为自己的Web服务器的能力。 假设服务器是其他用户可以访问的机器，可以配置Jupyter在该服务器上运行。 您必须向Jupyter提供配置信息，以便知道如何继续。 生成Jupyter安装配置文件的命令如下：

jupyter notebook --generate-config


这个命令会在你的〜。/ jupyter目录下生成一个jupyter_notebook_config.py文件。 对于Microsoft用户，该目录是您的家庭用户目录的子目录。

配置文件包含可用于将笔记本作为服务器公开的设置：


```
c.NotebookApp.certfile = u'/path/to/your/cert/cert.pem' c.NotebookApp.keyfile = u'/ path/to/your/cert/key.key' c.NotebookApp.ip = '*'

c.NotebookApp.password = u'hashed-password' c.NotebookApp.open_browser = False c.NotebookApp.port = 8888
 


[ 145 ]


```
![](/assets/图像 5.png)



每个网站都是通过IP地址在较低的层次上进行寻址的。 IP地址是一个由四部分组成的数字，用于标识涉及的服务器的语言环境。 IP地址可能类似于172.32.88.7。

与互联网软件一起使用的网络浏览器知道如何使用IP地址来定位感兴趣的服务器。 这套软件也知道如何翻译你在浏览器中提到的URL，比如http：// www。 microsoft.com，转换成IP地址。

请注意，所提供的示例配置不适用于企业。 您需要与您的安全人员协调配置正确。 一旦您正确地更改了设置，您应该能够将浏览器指向所配置的URL并访问您的笔记本电脑。 该URL将是HTTP或HTTPS（取决于您是否应用SSL证书），IP地址和端口的连接

例如，HTTPS://123.45.56.9:8888。
