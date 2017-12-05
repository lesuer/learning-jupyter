### Jupyter的配置选项
****
您可以配置显示笔记本时使用的一些显示参数。由于使用产品（CodeMirror）来呈现和修改笔记本，因此这些配置是可配置的。 CodeMirror是一个基于JavaScript的编辑器，可在网页（笔记本）中使用。

可配置选项列表仍在开发中。一些选项如下：

  lineSeparator：用于分隔文本行的字符

  主题：笔记本中使用的整体主题indentUnit：多少个空格来缩进编码块
 


[34]

 
Jupyter简介

要更改其中一个选项的配置，请打开浏览器的JavaScript窗口，输入编码修改选项，然后加载笔记本。然后，您所做的修改将应用于笔记本演示文稿。还有更多

文档可在nit。

例如，要更改笔记本的缩进（indent-unit），可以使用以下JavaScript：



```
var mycell = Jupyter.notebook.get_selected_cell（）; var cell_config = mycell.config;

var code_patch = {

CodeCell：{cm_config：{indentUnit：2}

}

}

cell_config.update（code_patch）
```



现在你已经看到Jupyter Notebook中的所有标准操作。