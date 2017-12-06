### 启动Docker
****
如果你运行Docker快速入门，你会被带到Docker终端窗口，显示如下：


```
bash --login '/Applications/Docker/Docker Quickstart Terminal.app/Contents/Resources/Scripts/start.sh'

Last login: Tue Aug 30 08:25:11 on ttys000 bos-mpdc7:Applications dtoomey$ bash --login

'/Applications/Docker/Docker Quickstart

Terminal.app/Contents/Resources/Scripts/start.sh'

Starting "default"...
 

[ 173 ]

 
Multiuser Jupyter Notebooks

(default) Check network to re-create if needed...

(default) Waiting for an IP...

Machine "default" was started.

Waiting for SSH to be available...

Detecting the provisioner...

Started machines may have new IP addresses. You may need to re-run the

`docker-machine env` command.

Regenerate TLS machine certs?  Warning: this is irreversible. (y/n):

Regenerating TLS certificates

Waiting for SSH to be available...

Detecting the provisioner...

Copying certs to the local machine directory...

Copying certs to the remote machine...

Setting Docker configuration on the remote daemon...

	##	.
##	## ##	==
## ##	## ## ##	===

/"""""""""""""""""\___/ ===

~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~

\______ o	__/

\	\	__/

\____\_______/

docker is configured to use the default machine with IP 192.168.99.100 For help getting started, check out the docs at https://docs.docker.com

```
（显示结尾附近的奇数图形是鲸鱼的字符表示 - Docker的标志。）

您可以从输出中看到以下内容：

   Docker机器已经启动 - Docker机器控制你的空间中运行的图像。

   如果您正在使用证书，证书将被复制到您的Docker空间。

   最后，它告诉你在访问你的Docker实例时使用的IP地址 - 它应该是你正在使用的机器的IP地址。
