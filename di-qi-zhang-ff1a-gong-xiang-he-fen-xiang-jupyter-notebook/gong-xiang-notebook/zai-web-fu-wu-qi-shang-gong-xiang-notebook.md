### 在Web服务器上共享笔记本

为了将笔记本添加到现有的Web服务器，您需要执行上述步骤，并向笔记本配置文件添加更多信息：



```
c.NotebookApp.tornado_settings = { 'headers': {

'Content-Security-Policy': "frame-ancestors

'https://yourwebsite.com' 'self' "

}

}


```


在这里，您将yourwebsite.com替换为您网站的网址。

一旦完成，你可以通过你的网站访问笔记本。