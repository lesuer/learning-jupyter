### 手术

我们现在可以直接从命令行启动JupyterHub：

jupyterhub

这将导致以下显示，这将显示在命令控制台窗口中：


```
[I 2016-08-28 14:30:57.895 JupyterHub app:643] Writing cookie_secret to

/Users/dtoomey/jupyterhub_cookie_secret

[W 2016-08-28 14:30:57.953 JupyterHub app:304]

Generating CONFIGPROXY_AUTH_TOKEN. Restarting the Hub will require restarting the proxy.

Set CONFIGPROXY_AUTH_TOKEN env or JupyterHub.proxy_auth_token config to avoid this message.

[W 2016-08-28 14:30:57.962 JupyterHub app:757] No admin users, admin interface will be unavailable.

[W 2016-08-28 14:30:57.962 JupyterHub app:758] Add any administrative users to `c.Authenticator.admin_users` in config.

[I 2016-08-28 14:30:57.962 JupyterHub app:785] Not using whitelist. Any authenticated user will be allowed.

[I 2016-08-28 14:30:57.992 JupyterHub app:1231] Hub API listening on http://127.0.0.1:8081/hub/

[E 2016-08-28 14:30:57.998 JupyterHub app:963] Refusing to run

JuptyterHub without SSL. If you are terminating SSL in another layer, pass

--no-ssl to tell JupyterHub to allow the proxy to listen on HTTP.

```
请注意，脚本已完成，并且您的默认浏览器中的窗口不会像标准Jupyter安装中那样打开。



这个最重要的功能是输出的最后一行（也在屏幕上以红色显示）拒绝运行没有SSL的JupyterHub。 JupyterHub是专门为多个用户登录和使用一台笔记本电脑而设计的，因此他们抱怨说它希望运行SSL（以确保用户交互）。

最后一行的后半部分给了我们一个线索，我们需要告诉JupyterHub我们没有使用证书/ SSL。 我们可以用--no-ssl参数来做到这一点，如下所示：

Jupyterhub - no-ssl

这导致在控制台中的预期结果，并保持服务器仍在运行：


```

[I 2016-08-28 14:43:15.423 JupyterHub app:622] Loading cookie_secret from /Users/dtoomey/jupyterhub_cookie_secret

[W 2016-08-28 14:43:15.447 JupyterHub app:304]
 

[ 167 ]

 
Multiuser Jupyter Notebooks

Generating CONFIGPROXY_AUTH_TOKEN. Restarting the Hub will require restarting the proxy.

Set CONFIGPROXY_AUTH_TOKEN env or JupyterHub.proxy_auth_token config to avoid this message.

[W 2016-08-28 14:43:15.450 JupyterHub app:757] No admin users, admin interface will be unavailable.

[W 2016-08-28 14:43:15.450 JupyterHub app:758] Add any administrative users to `c.Authenticator.admin_users` in config.

[I 2016-08-28 14:43:15.451 JupyterHub app:785] Not using whitelist. Any authenticated user will be allowed.

[I 2016-08-28 14:43:15.462 JupyterHub app:1231] Hub API listening on http://127.0.0.1:8081/hub/

[W 2016-08-28 14:43:15.468 JupyterHub app:959] Running JupyterHub without SSL. There better be SSL termination happening somewhere else...

[I 2016-08-28 14:43:15.468 JupyterHub app:968] Starting proxy @ http://*:8000/

14:43:15.867 - info: [ConfigProxy] Proxying http://*:8000 to http://127.0.0.1:8081

14:43:15.871 - info: [ConfigProxy] Proxy API at http://127.0.0.1:8001/api/routes

[I 2016-08-28 14:43:15.900 JupyterHub app:1254] JupyterHub is now running at http://127.0.0.1:8000/

```
如果我们现在转到输出最后一行显示的那个URL（http://127.0.0.1:8000/），我们进入JupyterHub的登录屏幕：

![](/assets/㔿.jpg)

所以，我们已经避免了要求SSL，但我们仍然需要为用户配置

系统。 请注意，不使用SSL将暴露您可能不想要的机器方面。

JupyterHub软件使用一个配置文件来确定它应该如何工作。 您可以使用JupyterHub生成配置文件，并使用以下命令提供默认值：

jupyterhub --generate-config

将默认配置写入：jupyterhub_config.py

该文件将在当前目录中生成。 您需要将文件移动到jupyterhub目录以执行您的更改。 生成的配置文件有近500行可用。 示例文件的开始如下所示：


```
#	Configuration file for jupyterhub. c = get_config()

#--------------------------------------------------------------------------

----

#	JupyterHub configuration

#--------------------------------------------------------------------------

----

#	An Application for starting a multiuser Jupyter Notebook server.

#	JupyterHub will inherit config from: Application

#	Include any kwargs to pass to the database connection. See

#	sqlalchemy.create_engine for details.

#	c.JupyterHub.db_kwargs = {}

#	The base URL of the entire application

#	c.JupyterHub.base_url = '/'

```
正如你所看到的，大部分配置设置都以井号（＃）为前缀，表示它们被注释掉了。 提到的设置是将应用的默认值。 如果您需要更改其中一个设置，您将删除前缀尖锐符号，并将等号（=）的右侧更改为新值。 顺便说一下，这是测试更改的好方法：进行一项更改，保存文件，尝试更改，然后继续进行任何其他更改。 随着你的进步，如果一个变化不能按预期工作，你只需要更换英镑符号，你就回到了工作位置。
 







[169]

 
多用户Jupyter笔记本

我们将看看一些可用的配置选项。 有趣的是，这个文件中的许多设置都是Python设置，而不是JupyterHub特有的。 项目清单包括以下内容：


![](/assets/图像 2.png)




