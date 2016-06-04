<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h2>丰富的else语句</h2>
在Python中的else语句略强大，不仅能搭配if语句，还能搭配循环语句for和while、还有异常处理try-except。

<h4>与循环语句搭配</h4>

	def showMaxFactor(num):
    	count = num // 2
    	while count > 1:
        	if num % count == 0:
            	print('%d最大的约数是%d' % (num, count))
            	break
        	count -= 1
    	else:
        	print('%d是素数！' % num)

	num = int(input('请输入一个数：'))
	showMaxFactor(num)
这个程序用来计算一个数的约数，只要找到约数就break，如果找不到呢就直接执行else语句的内容。只有在循环结束的时候才会执行else语句，如果中途break就不会执行了。由于for循环跟while循环都差不多，可以相互转换，所以这里for循环就不写例子了。

<h4>与异常处理搭配</h4>

	try:
		检测范围
	except:
		异常处理代码
	else:
		语句···
	finally:
		无论如何都必须执行
	
这样的话，只有当try中的代码没有出现异常，才会执行else中的语句，而finally中的代码无论怎样都会被执行。

<h2>简洁的with语句</h2>
平时写文件操作的代码时，经常需要close文件流，有时候会忘记写。而with语句提供了一个简洁的功能能够帮助我们关闭文件流。

	try:
    	with open('data.txt', 'w') as f:
        	for each_line in f:
            	print(each_line)
	except OSError as reason:
    	print('出错啦：' + str(reason))

这样的话，with语句会帮助我们关闭文件流。


5/20/2016 10:27:21 PM @author:Cloudking