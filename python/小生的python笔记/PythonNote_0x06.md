<link rel="stylesheet" href="./css/layout.css" type="text/css" />
<h2>集合</h2>
在我的世界里，你就是唯一。

是的没错，集合在Python中的作用就是“唯一”。<br/>
在数学上，把set称做有不同的元素组成的集合。<br/>
集合对性爱那个是一组<strong>无序排序</strong>的可哈希的值。<br/>
集合支持用in和not in操作符检查成员。<br/>

<h4>集合的类型</h4>
集合有两种不同的类型，可变集合(set)和不可变集合(frozenset)，对于可变集合来说，可以添加(add)和删除元素(remove)，而对不可变集合来说，则不允许这么做。

<h4>集合的特点</h4>
你需要知道的一点是，集合不允许有相同元素的出现。
	>>> num = set({1,1,12,56})
	num
	{1,12,56}
	>>> num = set({1,1.0})
	num
	{1.0}

<h4>集合的创建</h4>
创建列表，我们用的是[]；创建元组我们用的是(,);创建字典我们用的是{:};而现在创建一个集合所用的是{,} 一般这样的都被看成set类型，即集合类型。

	>>> num = {1,2,3,4,5,6}
	>>> type(num)
	<class 'set'>
	>>> num1 = [1,2,3,4,5,6]
	>>> type(num1)
	<class 'list'>
	>>> num2 = (1,2,3,4,5,6)
	>>> type(num2)
	<class 'tuple'>
	>>> num3 = {'1':'Cloudker'}
	>>> type(num3)
	<class 'dict'>
创建一个集合的时候，可以通过工厂方法set()。

<h4>集合元素的添加与删除</h4>
骚年，记得区分set与frozenset的不同点，只有前者才可以进行元素的添加与删除。

	num = set({1,2,3,4,5,6})
	>>> type(num)
	<class 'set'>
	>>> num.add(7)
	num
	{1, 2, 3, 4, 5, 6, 7}
	num.remove(7)
	>>> num
	{1, 2, 3, 4, 5, 6}

由于集合并不是很重要，所以等以后需要深入研究再来更新笔记就可以了。

5/14/2016 6:41:48 PM @author: CloudKing