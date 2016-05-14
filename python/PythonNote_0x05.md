<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h2>字典</h2>

<p>字典是Python中唯一的映射类型，平时谈论的“映射”、“哈希、“散列”或者是“关系数组”的时候，事实上都是指“字典”。</p>

<h4>如果创建字典和给字典赋值</h4>
	#创建一个字典
	dict1 = {'IP':'192.168.1.101','PORT':80}
	#添加一个新的数据项
	dict1['STATUS'] = 'True'
	#修改一个已经存在的数据项
	dict1['PORT'] = 81
	#删除一个键
	del dict1['STATUS']
	#删除一整个字典
	del dict1
列表用的是中括号，字典用的是大括号吗？NO，冒号之前代表“键”，冒号之后代表“值”。

<h4>如果迭代访问字典中的值</h4>
	dict2 = {'名字':'云都小生','爱好':'编程'}

	for key in dict2.keys():
		print('名字=%s, 爱好=%s' % (ket,dict2[key]))

<h4>相关函数</h4>
dict([container])创建字典的工厂函数。如果提供了容器类(container) ，就用其中的条目填充字典，否则就创建一个空字典。<br/>
len(mapping)  返回映射的长度(键-值对的个数) <br/>
hash(obj) 返回 obj 的哈希值<br/>

<h4>字典运用经典例题</h4>
	
	print('|--- 欢迎进入通讯录程序 ---|')
	print('|--- 1：查询联系人资料  ---|')
	print('|--- 2：插入新的联系人  ---|')
	print('|--- 3：删除已有联系人  ---|')
	print('|--- 4：退出通讯录程序  ---|')

	contacts = dict()

	while 1:
    	instr = int(input('\n请输入相关的指令代码：'))
    	
		if instr == 1:
       		name = input('请输入联系人姓名：')
        	if name in contacts:
            	print(name + ' : ' + contacts[name])
        	else:
            	print('您输入的姓名不再通讯录中！')

    	if instr == 2:
        	name = input('请输入联系人姓名：')
        	if name in contacts:
            	print('您输入的姓名在通讯录中已存在 -->> ', end='')
            	print(name + ' : ' + contacts[name])
            	if input('是否修改用户资料（YES/NO）：') == 'YES':
                	contacts[name] = input('请输入用户联系电话：')
        	else:
            	contacts[name] = input('请输入用户联系电话：')

    	if instr == 3:
        	name = input('请输入联系人姓名：')
        	if name in contacts:
            	del(contacts[name])         # 也可以使用dict.pop()
        	else:
            	print('您输入的联系人不存在。')
            
    	if instr == 4:
       		break

	print('|--- 感谢使用通讯录程序 ---|')
    

