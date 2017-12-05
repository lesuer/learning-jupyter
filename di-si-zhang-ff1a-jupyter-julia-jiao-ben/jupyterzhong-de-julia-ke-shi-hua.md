### Jupyter中的Julia可视化

在Julia中最流行的可视化工具是Gadfly包。 我们可以使用add函数添加Gadfly包（如本章开头所述）：

Pkg.add("Gadfly")

从此，我们可以使用以下命令在任何脚本中引用Gadfly包：


using Gadfly
