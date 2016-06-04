<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h4>Python的优点</h4>
1.	跨平台：Windows/Mac/WWW/Linux
2.	应用范围广：操作系统、Web、3D动画、云计算、企业应用
3.	脚本语言，语法精简

<h2>简单了解</h2>
IDLE是一个Python Shell，一个通过键入文本与程序交互的途径。<br/>
BIF是内置函数，为了方便程序员快速编写脚本程序，Python提供了非常丰富的内置函数。<br/>


<h2>函数记录</h2>
	print()			#会在输出窗口中显示一些文本
	input()			#接收shell输入
	数据类型()		#根据数据类型对括号内的参数进行转换
	random.randint(a,b)	#返回一个随机的整数,带参数则返回a~b之间的随机数
	type()			#返回数据类型
	isinstance(a,b)	#返回a、b两个对象类型是否相同
	range(a,b)		#迭代方式返回a~b的数值
	range(a,b,c)	#以c为步长,迭代方式返回a~b的数值	

<h2>Python细节知识</h2>
1.	Python使用的注释语法是#和三引号""";
2.	可以用dir(__builtins__)查询Python提供的内置方法列表;
3.	缩进是Python的灵魂;
4.	“Python”没有“变量”，只有“名字”;
5.	字符串可以是单引号也可以是双引号;
6.	使用原字符串，可以在字符串前面加r;
7.	引入模块时语法为import 模块名
8.	一行写多个代码语句是可以用分号隔开
9.	一行代码分多行写的话可以在后面加\
10.	**算术运算符在Python中用来进行幂运算
11.	Python中/运算符是进行精确除法，而//是进行地板除法
12.	逻辑操作符优先级 not > and > or
13.	运算优先级：逻辑 < 比较 < 算数 < 正负号 < 幂运算
14.	in成员资格运算符，用来检查一个值是否在序列中


<h2>Python基本语法</h2>
	==========================================
	if 条件:
		条件为真(true)
	elif 条件:
		条件为真(true)
	else:
		条件为假(false)
	==========================================
	while 条件:
		条件为真(true)
	==========================================
	for a in b:
		进行b-a次循环;(类似java中的foreach)
	for i in 5:
	for i in range()
	==========================================


<h3>输入检测有关</h3>
	s为字符串
	s.isalnum()	所有字符都是数字或是字母，为真返回True，为假返回False
	s.isalpha() 所有字符都是字母，为真返回True，为假返回False
	s.isdigit() 所有字母都是数字，为真返回True，为假返回False
	s.islower() 所有字符都是小写，为真返回True，为假返回False
	s.isupper() 所有字符都是大写，为真返回True，为假返回False
	s.istitle()	所有单词都是首字母大写，为真返回True，为假返回False
	s.ispace()	所有字符都是空白符，为真返回True，否则返回False
	s.isinstance(str) 判断s数据类型是否为字符串
	type(s)		返回s的数据类型，也可以用来作为验证方法

5/14/2016 6:38:08 PM @author: CloudKing