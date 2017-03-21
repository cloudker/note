<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h2>文件系统</h2>

模块是可用代码段的打包，是一个包含所有你定义的函数和变量的文件，模块可以被别的程序引入，只有当被引入时，该模块中的函数等功能才能被使用。例如说：

	import random
	secret = random.randint(1,10)

<h4>OS模块</h4>
对于文件系统的访问，Python一般是通过OS模块来实现，因为Python跨屏体，所以说这种文件操作在不同的操作系统是可以同样实现的。<br/>

常用函数如下：
![](./img/os_function.png)


<h4>OS.Path模块</h4>
常用函数如下：
![](./img/os.path_function.png)

5/20/2016 10:28:16 PM @author:Cloudking