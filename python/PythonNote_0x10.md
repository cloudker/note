<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h2>异常</h2>

<h4>Python常见的异常</h4>
![]("./img/Python_except1.png")
![]("./img/Python_except2.png")

<h4>如何捕获并处理异常？</h4>
与Java类似，采用try-except-finally的语法，格式如下：

	try:
		检测范围
	except 异常类型[as reason]:
		对该异常进行处理的代码
	finally:
		无论如何都会被执行的代码
需要补充的是，as reason是可选的，其实reason是个变量，可以自己命名，这个变量存储着异常的信息。

直接给个栗子：
	
	try:
    	list0 = [1,2,3]
    	print(list0[4])
	except IndexError as reason:
		print("出错了!原因是：" + str(reason))

	>>>出错了!原因是：list index out of range

可以同时捕获多个异常：

	try:
		num = 1 + '1'
		list0[1,2,3]
		print(list0[4])
	except TypeError as reason:
		print("出错了!原因是:类型转换过程出现错误。")
	except IndexError as reason:
		print("出错了!原因是：序列下标索引错误。")

	>>>出错了!原因是:类型转换过程出现错误。

需要注意的是，一旦有一个异常被捕获，之后的代码都不会被执行，所以这里只捕获了TypeError的异常。还有一个问题，什么时候我们需要用到finally呢？具体情况具体使用了。但是这里还是要举个栗子：例如说进行文件操作时，无论这中间出现了什么异常，捕获完处理完之后，都需要一个close关闭文件指针，辣么就可以利用finally语句来实现了。

<h4>统一处理多类异常</h4>
格式如下：

	try:
		检测范围
	except (异常类型1,异常类型2,异常类型3···):
		统一处理的代码
	finally:
		无论如何都要执行的代码

<h4>我任性！我要自己引发异常！</h4>
是的，Python提供了一个关键字能让我们主动引发异常——raise。

	>>> raise TypeError
	Traceback (most recent call last):
  	File "<pyshell#0>", line 1, in <module>
    raise TypeError
	TypeError

5/20/2016 10:27:53 PM @author:Cloudking