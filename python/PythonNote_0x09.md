<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h2>pickle模块</h2>
可以通过pickle模块将你的数据对象“腌制”成二进制文件，存储在磁盘上。这个模块略微强大，至于为什么要叫“泡菜”，我就不知道了。

<h4>pickle的方法</h4>
	pickle.dunmp(data,file)
	#前者是待存储的数据对象,后者是目标存储的文件对象
	pickle.load(file)
	#参数是目标存储的文件对象

<h4>经典例子</h4>
	
	#将数据利用该模块以二进制形式存储到磁盘
	file_data = {2016,"云都小生","Cloudker",3.141592654}
	import pickle
	file = open("file_data.plk","wb")
	pickle.dump(file,file_data)
	pickle.dump(file_data,file)
	file.close()

	#将数据利用该模块以二进制形式读取到程序中
	file = open("file_data.plk","rb")
	file_data1 = pickle.load(file)
	 print(file_data1)
	>>>{3.141592654, 2016, 'Cloudker', '云都小生'}
	file.close()
	

需要注意的是，打开的文件指针记得close掉。
为了让程序更加简洁美观，所以尽量将大型的数据封装起来，对，利用pickle模块，腌制成泡菜。

5/20/2016 10:28:04 PM @author:Cloudking