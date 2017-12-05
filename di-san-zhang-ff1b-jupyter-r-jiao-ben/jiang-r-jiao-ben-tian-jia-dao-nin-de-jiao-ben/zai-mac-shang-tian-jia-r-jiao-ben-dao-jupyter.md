### 在Mac上添加R脚本到Jupyter

如果您正在使用Mac，则可以使用命令行添加R脚本：
 

conda安装-c r r-essentials
 
Jupyter R脚本

这将从R环境的大型安装开始，其中包含许多常见的软件包：


```
bos-mpdc7:~ dtoomey$ conda install -c r r-essentials

Fetching package metadata: ......

Solving package specifications: .........

Package plan for installation in environment /Users/dtoomey/miniconda3:

The following packages will be downloaded:		
package	|	build		
---------------------------|-----------------		
jbig-2.1	|	0	31	KB
jpeg-8d	|	2	210	KB
libgcc-4.8.5	|	1	785	KB
... <<many packages>>			
r-caret-6.0_62	|	r3.2.2_0a	4.3	MB
r-essentials-1.1	|	r3.2.2_1a	726 B
------------------------------------------------------------
		Total:	101.0	MB
The following NEW packages will be INSTALLED:		
jbig:	2.1-0			
jpeg:	8d-2			
... <<many packages>>			
r-xts:	0.9_7-r3.2.2_0a			
r-yaml:	2.1.13-r3.2.2_1a			
r-zoo:	1.7_12-r3.2.2_1a			
zeromq:	4.1.3-0			

Proceed ([y]/n)? y Fetching packages ...

jbig-2.1-0.tar 100% |################################| Time: 0:00:00

1.59 MB/s

jpeg-8d-2.tar. 100% |################################| Time: 0:00:00 2.69 MB/s

... <<many packages>>

r-caret-6.0_62 100% |################################| Time: 0:00:00

11.16 MB/s

r-essentials-1 100% |################################| Time: 0:00:00 537.43 kB/s

Extracting packages ...

[	COMPLETE

]|###################################################| 100%

Linking packages ...

[ COMPLETE ]|###################################################| 100%
 






[ 59 ]

 
从那里，你像往常一样调用你的笔记本：

ipython notebook


```

