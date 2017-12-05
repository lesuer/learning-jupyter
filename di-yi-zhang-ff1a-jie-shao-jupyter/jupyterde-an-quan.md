### Jupyter的安全
****
Jupyter笔记本电脑是为了与其他用户共享而创建的，通常在互联网上共享。 但是，Jupyter笔记本可以执行任意代码并生成任意代码。 如果恶意方面被放置在笔记本中，这可能是一个问题。 Jupyter笔记本的默认安全机制包括：

   原始HTML总是消毒（检查恶意编码）。 更多信息可以在https://developers.google.com/caja找到。

   你不能运行外部JavaScript。

Jupyter简介

   单元格内容（尤其是HTML和JavaScript）不可信（需要用户验证才能继续）。

   任何单元格的输出都不可信。

   所有其他的HTML或JavaScript永远不会被信任。 清除输出将导致笔记本在保存时变得可信。