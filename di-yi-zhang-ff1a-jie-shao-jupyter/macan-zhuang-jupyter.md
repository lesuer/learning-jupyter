### 在Mac上安装Jupyter
****
在Mac上，您可以使用上一节所述的相同的Anaconda GUI（对于Mac）。 您也可以在Mac上使用适用于Linux的命令行工具。

您必须先安装Anaconda。 下载最新版本并执行嵌入式shell脚本进行安装。

在Mac上安装Jupyter是通过命令行使用conda install命令完成的：

bmac:~ dtoomey$	conda install	jupyter
Fetching package	metadata: ....
Solving	package	specifications: ....................................
Package	plan for	installation	in environment /Users/dtoomey/anaconda:

下列软件包将被下载：

package	|	build		
---------------------------	|	-----------------		
mistune-0.7.2	|	py27_1	178	KB
setuptools-20.3	|	py27_0	453	KB
conda-4.0.5	|	py27_0	185	KB
pexpect-4.0.1	|	py27_0	63	KB
traitlets-4.2.1	|	py27_0	108	KB
ipython-4.1.2	|	py27_2	931	KB
jupyter_core-4.1.0	|	py27_0	51	KB
jupyter_client-4.2.2	|	py27_0	96	KB
jupyter_console-4.1.1	|	py27_0	24	KB
notebook-4.1.0	|	py27_2	4.4	MB
qtconsole-4.2.1	|	py27_0	160	KB
jupyter-1.0.0	|	py27_2	2	KB

------------------------------------------------------------

Total:	6.6 MB

以下软件包将被更新：

conda:	3.19.3-py27_0 -->	4.0.5-py27_0
ipython:	4.1.2-py27_0  -->	4.1.2-py27_2
jupyter:	1.0.0-py27_1  -->	1.0.0-py27_2
jupyter_client:	4.1.1-py27_0  -->	4.2.2-py27_0
jupyter_console:	4.1.0-py27_0  -->	4.1.1-py27_0
jupyter_core:	4.0.6-py27_0  -->	4.1.0-py27_0
mistune:	0.7.1-py27_0  -->	0.7.2-py27_1
notebook:	4.1.0-py27_0	-->	4.1.0-py27_2
pexpect:	3.3-py27_0	-->	4.0.1-py27_0
qtconsole:	4.1.1-py27_0	-->	4.2.1-py27_0
setuptools:	20.1.1-py27_0 -->	20.3-py27_0
traitlets:	4.1.0-py27_0	-->	4.2.1-py27_0

Proceed ([y]/n)? y			
Fetching packages ...		
mistune-0.7.2- 100% |#################| Time: 0:00:00	1.87	MB/s
setuptools-20.	100% |#################| Time: 0:00:00	3.53	MB/s
conda-4.0.5-py 100%	|#################| Time: 0:00:00	2.47	MB/s
pexpect-4.0.1- 100%	|#################| Time: 0:00:00	1.26	MB/s
traitlets-4.2. 100%	|#################| Time: 0:00:00	1.71	MB/s
 

[ 20 ]

 
Introduction to Jupyter

ipython-4.1.2- 100% |#################| Time: 0:00:00	1.77	MB/s
jupyter_core-4 100% |#################| Time: 0:00:00	2.34	MB/s
jupyter_client 100% |#################| Time: 0:00:00	1.58	MB/s
jupyter_consol 100%	|#################| Time: 0:00:00	7.82	MB/s
notebook-4.1.0 100%	|#################| Time: 0:00:00	4.75	MB/s
qtconsole-4.2. 100%	|#################| Time: 0:00:00	1.37	MB/s
jupyter-1.0.0- 100%	|#################| Time: 0:00:00	2.71	MB/s

Extracting packages ...

[	COMPLETE ]|#############################################| 100%

Unlinking packages ...

[	COMPLETE ]|#############################################| 100%

Linking packages ...

[	COMPLETE ]|#############################################| 100%
你已经安装了Jupyter。






