### 在Windows上将R脚本添加到Jupyter

如果你正在使用Windows机器，那么你需要在Jupyter中获得R的几个步骤。 这个环境确实是为Linux开发的。

在我的机器上，Anaconda安装在我的用户目录中。 这可能是因为我选择只为自己安装它。 如果您在Anaconda / scripts目录中打开命令行窗口，则应首先使用以下命令确保笔记本软件是最新的：

conda更新笔记本

这会产生以下输出（对我来说 - 您的结果可能会不同，以根据需要更新不同的方面）：


```
C:\Users\Dan\Anaconda2\Scripts>conda update notebook

Using Anaconda Cloud api site https://api.anaconda.org

Fetching package metadata: ....

Solving package specifications: .........

Package plan for installation in environment C:\Users\Dan\Anaconda2:

The	following packages will be downloaded:		
	package	|	build	
	---------------------------|-----------------	
	notebook-4.2.0	|	py27_0	5.2 MB
The	following packages will be updated:		

notebook: 4.1.0-py27_2 --> 4.2.0-py27_0 Proceed ([y]/n)? y

Fetching packages ...

notebook-4.2.0 100% |###############################| Time: 0:00:04 1.12 MB/s

Extracting packages ...

[	COMPLETE	]|########################################| 100%
Unlinking packages ...
[	COMPLETE	]|########################################| 100%
Linking packages ...	
[	COMPLETE	]|########################################| 100%
 







[ 60 ]


```
然后我们冒险并添加R脚本：

conda安装-c r笔记本r-irkernel

这会产生更新的软件包的详细视图。 就我而言，即使我之前在机器的其他地方使用了R，它也安装了一整套R包和运行时：


```
C:\Users\Dan\Anaconda2\Scripts>conda install -c r notebook r-irkernel

Using Anaconda Cloud api site https://api.anaconda.org

Fetching package metadata: ......

Solving package specifications: .........

Package plan for installation in environment C:\Users\Dan\Anaconda2:

The following packages will be downloaded:

package	|	build			
---------------------------|-----------------			
msys2-conda-epoch-20160418 |	0		420 B	
m2w64-expat-2.1.1	|	1		164 KB	
m2w64-gmp-6.1.0	|	1		638 KB	
m2w64-gsl-2.1	|	1		2.3 MB	
... <<many packages>>					
r-evaluate-0.8.3	|	r3.2.4_0		44 KB	
r-irkernel-0.6	|	r3.2.4_0		78 KB	
------------------------------------------------------------	
		Total:	100.5 MB	
The following NEW packages will be INSTALLED:			
m2w64-bwidget:	1.9.10-1				
m2w64-bzip2:	1.0.6-5				
m2w64-expat:	2.1.1-1				
r-stringi:	1.0_1-r3.2.4_0			
r-stringr:	1.0.0-r3.2.4_0			
r-survival:	2.38_3-r3.2.4_0			
r-uuid:	0.1_2-r3.2.4_0			
... <<many packages>>					
Proceed ([y]/n)? y					
Fetching packages ...					
msys2-conda-ep 100% |#####################| Time: 0:00:00	26.25	kB/s
m2w64-expat-2. 100% |#####################| Time: 0:00:00	1.19	MB/s
m2w64-gmp-6.1. 100% |#####################| Time: 0:00:00	1.90	MB/s
m2w64-gsl-2.1- 100% |#####################| Time: 0:00:00	3.27	MB/s
m2w64-libiconv 100% |#####################| Time: 0:00:00	2.82	MB/s
... <<many packages>>					

r-evaluate-0.8	100%	|#####################| Time: 0:00:00 964.72 kB/s
r-irkernel-0.6	100%	|#####################| Time: 0:00:00 508.94 kB/s
Extracting packages ...
[	COMPLETE		]|########################################| 100%
Linking packages ...	
[	COMPLETE		]|########################################| 100%
 

[ 61 ]


```


