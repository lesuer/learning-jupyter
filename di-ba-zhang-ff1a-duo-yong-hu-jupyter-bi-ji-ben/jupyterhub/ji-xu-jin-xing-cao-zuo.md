### 继续进行操作

我没有更改配置文件来启动和运行我的安装。默认情况下，配置使用PEM系统，该系统将使用手动添加到正在运行的表单和操作系统的用户凭据来传递凭证（就像它们正在登录到计算机中一样）以进行验证。请注意，在这个步骤中会出现SSL错误，这将要求您重命名

./jupyter目录。

如果在尝试登录到JupyterHub安装时看到消息JupyterHub单用户服务器需要在控制台日志中记录> = 4.0，则需要使用以下命令更新基本Jupyter：

pip3 install jupyter


这将更新您的基础jupyter到最新版本，目前4.1。

如果你没有安装pip3，你需要升级到Python 3或更新版本。有关系统的步骤，请参阅https://www.python.org/上的文档。
 


[170]

 
多用户Jupyter笔记本

现在，您可以使用以下命令行启动JupyterHub：

jupyterhub --no-ssl

或者，您可以使用上一章中的证书。使用登录到机器的相同凭据登录登录屏幕（请记住，JupyterHub正在使用PEM，它会调用您的操作系统来验证凭据）。你最终会看起来非常像你的标准Jupyter主页：

![](/assets/不v.jpg)

它看起来非常相似，除了在屏幕右上方现在有两个额外的按钮：

  Control Panel 
  Logout

点击注销按钮将您注销JupyterHub并将您重定向到登录屏幕。

点击“控制面板”按钮，您将看到一个新的屏幕，其中有两个选项，如下所示：

   Stop My Server 
   My Server
   
 ![](/assets/评论.jpg)
 
 点击“停止我的服务器”按钮可停止Jupyter安装，并通过一个按钮进入页面：My Server（如本节所示）。 您可能也注意到了命令行的控制台日志中发生的更改：
 



```
[I 2016-08-28 20:22:16.578 JupyterHub log:100] 200 GET /hub/api/authorizations/cookie/jupyter-hub-token-dtoomey/[secret]

(dtoomey@127.0.0.1) 13.31ms

[I 2016-08-28 20:23:01.181 JupyterHub orm:178] Removing user dtoomey from proxy

[I 2016-08-28 20:23:01.186 dtoomey notebookapp:1083] Shutting down kernels

[I 2016-08-28 20:23:01.417 JupyterHub base:367] User dtoomey server took 0.236 seconds to stop

[I 2016-08-28 20:23:01.422 JupyterHub log:100] 204 DELETE /hub/api/users/dtoomey/server (dtoomey@127.0.0.1) 243.06ms


```
![](/assets/闩.jpg)

点击“我的服务器”按钮可以将您带回Jupyter主页。 如果您之前点击了“停止我的服务器”按钮，则会重新启动底层的Jupyter软件，您可能会注意到在控制台输出中（我已经在此显示）：




```
I 2016-08-28 20:26:16.356 JupyterHub base:306] User dtoomey server took

1.007 seconds to start

[I 2016-08-28 20:26:16.356 JupyterHub orm:159] Adding user dtoomey to proxy /user/dtoomey => http://127.0.0.1:50972

[I 2016-08-28 20:26:16.372 dtoomey log:47] 302 GET /user/dtoomey (127.0.0.1) 0.73ms

[I 2016-08-28 20:26:16.376 JupyterHub log:100] 302 GET

/hub/user/dtoomey (dtoomey@127.0.0.1) 1019.24ms

[I 2016-08-28 20:26:16.413 JupyterHub log:100] 200 GET /hub/api/authorizations/cookie/jupyter-hub-token-dtoomey/[secret] (dtoomey@127.0.0.1) 10.75ms



```







