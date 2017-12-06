### 通过Docker共享笔记本

Docker是一个用于分发软件的开放轻量级容器。 一个典型的Docker实例有一台完整的Web服务器和一台运行在机器端口上的特定Web应用程序。 有关在Docker实例中运行的软件的具体细节由Dockerfile文件管理。 该文件向Docker环境提供关于哪些组件用于配置此实例的命令。 Jupyter实现的示例Dockerfile内容如下所示：


```
ENV TINI_VERSION v0.6.0

ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini

/usr/bin/tini

RUN chmod +x /usr/bin/tini

ENTRYPOINT ["/usr/bin/tini", "--"] EXPOSE 8888

CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0"]
 















[ 148 ]


```
以下是关于Dockerfile中每个命令的讨论：

  ENV命令告诉Docker使用专门的操作系统。这是为了克服Jupyter不断获取和释放机器资源的不足所必需的。 TINI是提供最小化Docker初始化的第三方软件。

  ADD命令告诉Docker tini代码的位置。

  RUN命令正在改变对tini目录的访问权限。

  ENTRYPOINT命令告诉Docker作为Docker实例的操作系统。

  EXPOSE命令告诉Docker打开你的笔记本的端口。

  CMD命令告诉Docker运行哪些命令（一旦环境被设置）。

  将Docker实例部署到Docker机器后，您可以在指定的端口（8888）上访问机器上的Docker实例，例如，

http://machinename.com:8888。

前面提到的说明假设你是Docker的新手。如果您有一个现有的Docker安装Dockerfile配置和Docker中的Jupyter实例的访问，说明可能会改变。
