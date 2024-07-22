# Python学习知识点

## 第一章--基本输出函数

### 1.print介绍

```python
a = 100
b = 50
print(a)
print(b)
print((a+b))
print('北京欢迎你')
print("你好")
print(a,b,'i am')
#chr字符转换
print(chr(98))
#ord函数
print(ord('北'))
#end=不换行
print('first',end='-->')
print('second')
#+连接符,同种类型连接
print(a+b)
print('2'+'00')
```

### 2.input介绍

```python
#连接,先输入，后输出，input为字符串
name = input('请输入名字叫')
print('My name is ' + name)
name = int(name)
print('转换=' ,name)
```

### 3.注释了解

```python
#连接,先输入，后输出，input为字符串
name = input('请输入名字叫')
print('My name is ' + name)
name = int(name)
print('转换=' ,name)
```

### 4.代码缩进

```python
#缩进是为了留有空格，比较整齐

#类的缩进
class student:
    pass
#函数缩进
def fun():
    pass
```

### 5.文件写入

```python
1.
fp = open('text.txt','w')
print('人生苦短，我用python',file = fp)
fp.close()

```

## 第二章--数据类型与运算符

### 2.1--保留字与标识符

```python
#保留字
import keyword
print(keyword.kwlist)#保留字符区分大小写
'''
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']

'''
print(len(keyword.kwlist))#保留个数
#标识符--区分大小写，不能用保留字，就是便于区分的名称，用下划线区分

```

### 2.2--变量与常量

```python
#变量
my_name = 'duzhengjin'
print('luck数据类型',type(my_name)) #字符串
num = 3
print('num数据类型',type(num))
print(id(num)) #id为地址符

#常量
'''
不允许修改的量，用大写字符与下划线表示
'''
```

### 2.3--数值类型

```python
#整数表示
num1 = 987 #十进制
num2 = 0b1010101 #二进制表示
num3 = 0o765 #八进制表示
num4 = 0x87ABF #十六进制表示
print(num1)
print(num2)
print(num3)
print(num4)
#浮点型
height = 187.6
print(height)
print(type(height))
x=0
y = 10.0
print('x type=',type(x))
print('y type=',type(y))
z = 1.99E1413
print('科学计数法=',z,type(z))
print(round(0.01+0.03,3)) #round保留3位小数,指定位数
#实部虚部
x = 123 + 8j
print('实部 =',x.real,' 虚部 =',x.imag)

```

### 2.4--字符串类型

```python
#字符串类型,三引号用于多行字符串
info ='''
     1
     2
     3
'''
info1 = """
     4
     5
     6
"""
print((info))
print(info1)

print('1+2= \n 3')
print('hellooooo')
print('hello\toooo')
print('老师说：\'好好学习天天向上\'.') #转义字符
#r,R使转义字符失效
print('beijin\nnihao\n')
print(r'beijin\nnihao\n')

#索引
s = 'helloworld'
print(s[0],s[-10])
print(s[0:7]) #从0开始到7，不包含七
print(s[0:]) #0到结尾
print(s[:10]) #开始到结尾
x = 'me'
y = 'you'
print(x+y)#x，y连接
print(x*5)#copy五次

```

### 2.5--布尔类型

```python
flag = True
print(type(flag))
print(10+True)
print(10+False)
print('--------------------')
print(bool(18))
print(bool(0),bool(0.0))
print('--------------------')
print(bool(''))
print(bool('nihai'))
```

### 2.6--类型转换

```python
x = 76
print(int(x)) #转整数
print(float(x)) #转浮点数
print(str(x)) #转字符串
print(chr(x)) #转一个字符
#print(ord(x)) #转整数
print(hex(x)) #十六进制
print(oct(x)) #八进制
print(bin(x)) #二进制
```

### 2.7--eval函数

```python
#eval去掉字符串左右的引号
s = '5 + 9'
print(s,type(s))
x = eval(s)
print(x, type(x))
#input ,eval一起使用
age = eval(input('your name:'))#不能为字符串，里面为整数
print(age)

```

### 2.8--运算符

```python
'''
   算术运算符
   '+ - * /'
'''
print('冥运算',2**4)
print(10/0) #error
print('整除',10//3)
print('求余',10%3)

#赋值运算符
-= *= += //= %= /=

#比较运算符
> < == != >= <= 

#逻辑运算符
and(&&) or(||) not(!)
print(True and False) #False
print(True or False)  #True
print(not True or False) #False
print(True and True)  #True

#位运算符
&:位与运算符 |:位或运算符
print('按位与',12&8)  #有0为0，双1为1
print('按位或',4|8)   #有1为1
print('按位异或',2^4)  #同为0，异为1
print('按位取反',~4)   #0->1,1->0
print('左移位<<',2<<2)    #向左移动两位 2*2*2,高位溢出,相当于乘法操作
print('右移位>>',8 >> 2) #向右移位 8 // 2，4 // 2 ，相当于除法操作
```

## 第三章--程序的流程与控制

### 3.1--程序的描述方式

**Input,Progress,Output**：解决方法

流程图：判断循环

伪代码：解释

### 3.2--程序的组织结构

```python
#顺序结构
'''
   按顺序执行操作，赋值，输出等等
'''
#选择结构
'''
   if...else
'''
a = 10
if a>0:
    print('这个数大于0')
else:
    print('这个数小于0')
    
x = 2
y = 5
if x<y:max=y
print('maxx=',max)
print('true'if x > y else 'false)
#多分支结构
'''
    if  x:
    else if x1:
    else:
'''
#嵌套if
      '''
         if里面if
      '''
#多个条件的连接
      '''
         多个条件连接在一起
         and，or的使用
      '''
```

### 3.3--模式匹配 match = switch

```python
score = input('请输入你的成绩：')
match score:
    case 'A':
        print('优秀')
    case 'B':
        print('良好')
    case 'C':
        print('中等')
    case 'D':
        print('及格')
    case 'E':
        print('不及格')
```

### 3.4--for循环

```python
#遍历
for i in 'hello':
    print(i)
#range()函数产生[n,m)整数序列，s为字符串，s[0,5）从0到5，不包含5 ----look->2.5bool
for i in range(1,12):
    if i%2==0:
        print(i)
```

### 3.5--while结构

```python
answer = input('你要上课吗?y/n')
while answer == 'y':
    print('good body')
    answer = input('你要上课吗?/n')
print('not good')
#while...else..正常执行完会执行else
```

### 3.6--打印菱形

```python
row = eval(input('请输入菱形行数'))
while row%2==0:
    print('重新输入菱形行数')
    row = eval(input('请输入菱形行数'))
top_row=(row+1)//2
for i in range(1,top_row+1):
    for j in range(1,top_row+1-i):
        print(' ',end='')
    for k in range(1,i*2):
        print('*',end='')
    print()
button_row=row//2
for i in range(1,button_row+1):
    for j in range(1,i+1):
        print(' ',end='')
    for k in range(1,button_row*2 - 2*i +2):
        print('*',end='')
    print()

```

### 3.7--break，continue，pass用法

```python
break
continue
#pass占位，结构完整
if True:
    pass
while True:
    pass
```

## 第四章--组合数据类型***

### 4.1序列与索引--切片

编号：有正向与反向，0-N-1，-N--1

```python
#正向
s = 'helloworld'
for i in range(0,len(s)):
    print(i,s[i],end='\t\t')
print()
#反向
for i in range(-len(s),0):
    print(i,s[i],end='\t\t')

#切片操作
print()
s1 = s[0:5:2] #省略start，end，step，都从极值出发
print(s1)
```

![Snipaste_2024-07-16_08-57-40](D:\视频及壁纸\截屏\Snipaste_2024-07-16_08-57-40.png)



### 4.2序列相关操作--查找次数

![Snipaste_2024-07-16_09-13-04](D:\视频及壁纸\截屏\Snipaste_2024-07-16_09-13-04.png)

```python
#in
s='helloworld'
print('e是否存在？',('e'in s))
#not in
print('e是否存在？',('e' not in s))
#len,max,min
print('len=',len(s))
#index
print('s.index()=',s.index('o'))
#s.count()
print('s.count(0)=',s.count('l'))
```



### 4.3列表的基本操作--enumerate,list(),[]

```python
#4.1都可以用
lst = ['hello','wos',98]
print(lst)
print(lst*3) #序列相乘
lst1=list('helloworld')
lst2=list(range(1,10,2)) #步长
print(lst1)
print(lst2)

#delete
lst3=[10,20,40]
print(lst3)
del lst3
#print(lst3)删除不可使用

#列表的遍历操作
lst=['hello','world','python']
for item in lst:
    print(item)

for i in range(0,len(lst)):
    print(i,'->',lst[i])

#enumerate函数
for index,item in enumerate(lst,start=1):  #手动设置起始位置
    print(index,item)

```

### 4.4列表的特有操作--sort

![微信图片_20240716095115](D:\视频及壁纸\微信\微信图片_20240716095115.jpg)

```python
lst = ['hello','world','python']
print(lst)
lst.append('am')
print(lst)
lst.remove('hello')
print(lst)
lst.pop(1)
print(lst)
#lst.clear()
lst.reverse()
print(lst)

new_list = lst.copy()
print(new_list)
#排序----------------------------
lst1 = [2,5,1,4,2,5]
lst1.sort()
print('升序',lst1)
lst1.sort(reverse=True)
print('降序',lst1)
#字符排序,先排大写，再拍小写，多32.A65,a97
lst2 = ['ssd','Tsfg','wiiw','po']
lst2.sort()
print(lst2)
lst2.sort(reverse=True)
print(lst2)
lst2.sort(key=str.lower) #将大小写看作小写排序
print(lst2)
#sorted排序,产生新列表
num = [1,6,4,9,23]
print(num)
asc_lst=sorted(num)
print('升序',asc_lst) #升序---------------
desc_lst=sorted(num,reverse=True)
print('降序',desc_lst) #降序----------
```

### 4.5--列表生成式及二维列表--random

```python
import random
lst=[item for item in range(1,11)]
print(lst)

lst=[item*item for item in range(1,11)]
print(lst)

lst=[random.randint(1,100) for _ in  range(10)]
print(lst)

lst=[i for i in range(10) if i%2==0]
print(lst)

lst=[[1,2,3],[4,5,6],[7,8,9]]
print(lst)
for row in lst:
    for item in row:
        print(item,end='\t')
    print()
#生成四行五列
lst=[[j for j in range(5)]for i in range(4)]
print(lst)
```

### 4.6--元组的创建与删除--**不可改变--turple()

```python
#带个括号，将个数输出
t = (10,[10,29,56],'helloworld','python')
print(t)

t = tuple(t)
print(t)

s = tuple('helliworld')
print(s) #('h', 'e', 'l', 'l', 'i', 'w', 'o', 'r', 'l', 'd')

t = tuple([10,20,40,20])
print(t) #(10, 20, 40, 20)
print('是否存在10',(10 in t))
print('是否不存在10',(10 not in t))
print('maxx = ',max(t))
print('minn = ',min(t))
print('len = ',len(t))
print('t.index = ',t.index(10))
print('t.count = ',t.count(20))
x=(10)
print(x,type(x)) #int
y = (10,)
print(y,type(y)) #tuple
#delete
del y
```

### 4.7--元组的访问与遍历

```python
t = ['123','hello','world','python']
#get  value
for item in t:
    print(item)
#get index
for i in range(len(t)):
    print(i,' ',t[i])
#enumerate函数,get value,index
for index,item in enumerate(t,start=1): #切片操作，可修改index
    print(index," ",item)
```

### 4.8--元组生成式**

```python
t = (i for i in range(1,4))
# print(t)
# t = tuple(t)
# print(t)
# #遍历
# for item in t:
#     print(item)
# #_next()_去元素
print(t.__next__())
print(t.__next__())
```

### 4.9字典的创建与删除--dict()

无序，键值对，key->value,可以用列表中的方法·

```python
#first
d = {1:'e',2:'oo',2:'ahh'}
print(d) #相同的话会覆盖，{1: 'e', 2: 'ahh'}

#second
lst1 = {10,20,30,40}
lst2 = {'cat','dog','zoo','kee','jii'}
zipobj=zip(lst1,lst2)
print(zipobj)
#print(list(zipobj)) #[(40, 'cat'), (10, 'jii'), (20, 'kee'), (30, 'zoo')]
d = dict(zipobj)
print(d) #{40: 'kee', 10: 'jii', 20: 'dog', 30: 'cat'}

d = dict(cat=10,dog=20)
print(d) #{'cat': 10, 'dog': 20}

t = (10,20,30)
print({t:20}) #{(10, 20, 30): 20}

lst = {10,20,30}
```

### 4.10字典的遍历

```python
d = {'hello':1,'python':2,'world':3}
print(d.get('hello')) #get value
#元组遍历
for item in d.items():
    print(item)
'''
('hello', 1)
('python', 2)
('world', 3)
'''
#get key,value
for key,value in d.items():
    print(key,"-->",value)
'''
hello --> 1
python --> 2
world --> 3
'''
```

### 4.11字典的操作方法

```python
d={1:'me',2:'you',3:'he'}
print(d) #{1: 'me', 2: 'you', 3: 'he'}
print(d.items()) #dict_items([(1, 'me'), (2, 'you'), (3, 'he')])
#add
d[4]='she'
print(d) #{1: 'me', 2: 'you', 3: 'he', 4: 'she'}
keys = d.keys()
print(keys) #dict_keys([1, 2, 3, 4])
print(list(keys)) #[1, 2, 3, 4]
print(tuple(keys)) #(1, 2, 3, 4)

values=d.values()
print(values)
print(list(values))
print(tuple(values))
'''
dict_values(['me', 'you', 'he', 'she'])
['me', 'you', 'he', 'she']
('me', 'you', 'he', 'she')
'''
lst=list(d.items())
print(lst)
d=dict(lst)
print(d)
'''
[(1, 'me'), (2, 'you'), (3, 'he'), (4, 'she')]
{1: 'me', 2: 'you', 3: 'he', 4: 'she'}
'''
#合并
d1={}
d2={}
print(d1|d2)
```

### 4.12集合的创建与删除--set()

```python
s={10,20,30}
print(s)
s=set()
print(s)
s1=set(range(1,10))
print(s1)
'''
{10, 20, 30}
set()
{1, 2, 3, 4, 5, 6, 7, 8, 9}
'''
```

### 4.13集合的操作符

![Snipaste_2024-07-16_15-46-37](D:\视频及壁纸\截屏\Snipaste_2024-07-16_15-46-37.png)

```python
A={10,20,30,40,50}
B={30,50,88,76,20}
print(A&B) #交集
print(A|B) #并集
print(A-B) #差集
print(A^B) #补集
'''
{50, 20, 30}
{40, 10, 76, 50, 20, 88, 30}
{40, 10}
{10, 88, 40, 76}
'''
```

### 4.14集合的操作方法及集合的遍历

```python
s={1,2,3}
s.add(6)
print(s)
s.remove(1)
print(s)
# s.clear()
# print(s)
for item in s:
    print(item)
for index,item in enumerate(s):
    print(index," ",item)
'''
2
3
6
0   2
1   3
2   6
'''
s={i for i in range(1,10)}
print(s)
```

### 4.15总结

![Snipaste_2024-07-16_16-06-08](D:\视频及壁纸\截屏\Snipaste_2024-07-16_16-06-08.png)

## 第五章--字符串及正则表达式

### 5.1--字符串使用方法

![Snipaste_2024-07-16_17-02-31](D:\视频及壁纸\学习\Snipaste_2024-07-16_17-02-31.png)

```python
s1='hello,world'
new_s1=s1.lower()
print(new_s1)
new_s2=s1.upper()
print(new_s2)
#split
email='@qq.com'
new_list=email.split('@')
print(new_list)
print(s1.count('o'))
print(s1.find('e'))
print(s1.endswith('ld'))
print(s1.startswith('heoo'))
hello,world
HELLO,WORLD
'''
['', 'qq.com']
2
1
True
False
'''
```

![image-20240716171849989](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240716171849989.png)

```python
s1='hello,world'
s2=s1.replace('llo',',python')
print('replace=',s2) #he,python,world
print('s.center=',s1.center(20)) #s.center     hello,world
print(s1.center(20,'*')) #****hello,world*****
s2='   hello    '
print(s2.strip()) #去掉前后的空格
print(s2.lstrip())#去掉前面
print(s2.rstrip())#去掉后面
s3='ld-heldo-ld'
print(s3.strip('ld')) #ld前后去掉
```

### 5.2--格式化字符串

![Snipaste_2024-07-16_21-39-08](D:\视频及壁纸\截屏\Snipaste_2024-07-16_21-39-08.png)

```python
name='马冬梅'
age=19
score=98.9
print('姓名：%s,年龄：%d,成绩：%f' %(name,age,score))
#姓名：马冬梅,年龄：19,成绩：98.900000
#second
print(f'姓名{name},年龄：{age},成绩：{score}')
#third
print('姓名：{0},年龄：{1},成绩：{2}'.format(name,age,score)) #0,1,2对应name，age，score
```

### 5.3--format字符串的使用

![Snipaste_2024-07-16_21-59-47](D:\视频及壁纸\学习\Snipaste_2024-07-16_21-59-47.png)

```python
s='helloworld'
print('{0:*<20}'.format(s)) #左对齐，0代表format，：为引导符号，*补齐
print('{0:*>20}'.format(s))
print('{0:*^20}'.format(s))

print('{0:,}'.format(83262817467)) #三位一体
print('{0:.3f}'.format(3.1415984)) #保留小数
print('{0:.5}'.format('djuduihu')) #5个长度,只能用于字符串

a=16
print('二进制：{0:b},十进制：{0:d},八进制：{0:o},十六进制：{0:X}'.format(a))

b=3.1415644
print('{0:.2f},{0:.2E},{0:.2e},{0:.2%}'.format(b)) #3.14,3.14E+00,3.14e+00,314.16%
```

### 5.4--字符串的编码与解码

![image-20240716223432917](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240716223432917.png)

```python
#编码
s='伟大的中国梦'
scode=s.encode(errors='replace')
print(scode) #utf-8中文站三个字节

scode_gbk=s.encode('gbk',errors='replace')
print(scode_gbk) #中文站三个字节
'''
b'\xe4\xbc\x9f\xe5\xa4\xa7\xe7\x9a\x84\xe4\xb8\xad\xe5\x9b\xbd\xe6\xa2\xa6'
b'\xce\xb0\xb4\xf3\xb5\xc4\xd6\xd0\xb9\xfa\xc3\xce'
'''
#--------------------------------------------
#解码
print(bytes.decode(scode_gbk,'gbk'))
print(bytes.decode(scode,'utf-8'))
'''
伟大的中国梦
伟大的中国梦
'''
```

### 5.5--数据的验证（判断是否为某个东西)

![image-20240716224523001](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240716224523001.png)

```python
print('123'.isdigit()) #True
print('一二三'.isdigit()) #False
print('-'*50)
print('123'.isnumeric()) #True
print('一二三'.isnumeric()) #True
#istitle这能首字母大写，其他的不能
```

### 5.6--字符串的拼接

![Snipaste_2024-07-17_08-55-55](D:\视频及壁纸\学习\Snipaste_2024-07-17_08-55-55.png)

```python
#first
s1='helloworld'
s2='python'
print(s1+s2)
print(''.join([s1,s2]))
print('*'.join(['nihao','hello','name']))
'''
helloworldpython
helloworldpython
nihao*hello*name
'''
#second
print('hrllo''sjjs')
#third
print('%s%s' %(s1,s2))
print(f'{s1}-{s2}')
print('{0}-{1}'.format(s1,s2))
```

### 5.7--字符串的去重

```python
s='helloworld'
new_s1=''
for item in s:
    if item not in new_s1:
        new_s1+= item
print(new_s1)
new_s2=''
for i in range(len(s)):
    if s[i] not in new_s2:
        new_s2+=s[i]
print(new_s2)
new_s3=set(s)
lst=list(new_s3)
lst.sort(key=s.index)
print(''.join(lst))
```

### 5.8--正则表达式的简介及相关符号

![image-20240717095506015](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717095506015.png)

![image-20240717100026529](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717100026529.png)

![image-20240717101041859](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717101041859.png)

### 5.9--re模块中match函数的使用

match只在起始位置

![image-20240717101143598](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717101143598.png)

```python
import re
pattern='\d\.\d+'
s='hello 8288'
match=re.match(pattern,s,re.I)
print(match)
s1='9.23djjad'
match1=re.match(pattern,s1)
print(match1)
print('起始位置',match1.start())
print('终止位置',match1.end())
print('两者位置之间的位置元素',match1.span())
print('待匹配的字符串',match1.string)
print('待匹配的数据',match1.group())
'''
None
<re.Match object; span=(0, 4), match='9.23'>
起始位置 0
终止位置 4
两者位置之间的位置元素 (0, 4)
待匹配的字符串 9.23djjad
待匹配的数据 9.23
'''
```

### 5.10--re模板中search函数和findall函数的使用

都是在全体查找，一个为基本输出，另一个为列表

search第一个

```python
import re
pattern='\d\.\d+' #定义为数字标准,数字+.+数字，加号代表\d可出现多次
s='hello82.88gyuu'
match=re.search(pattern,s)
print(match) #<re.Match object; span=(6, 10), match='2.88'>
print(match.group())

s1='4.2314dad'
match1=re.search(pattern,s1)
print(match1) #<re.Match object; span=(0, 6), match='4.2314'>
print(match1.group())

s2='djahd'
match2=re.search(pattern,s2)
print(match2) #None
#print(match2.group())

m1=re.findall(pattern,s)
m2=re.findall(pattern,s1)
m3=re.findall(pattern,s2)
print(m1)
print(m2)
print(m3)
'''
['2.88']
['4.2314']
[]
'''
```

### 5.11--re模板中sub函数和split函数的使用

sub替换，split分割，避免一些敏感词

```python
import re
pattern='破解|黑客|反爬'
s='wo study python,破解vip video'
new_s=re.sub(pattern,'***',s)
print(new_s) #wo study python,***vip video
x'x'x'x'x'x'x'x'x'x'x'x'x'x'x'x'x'x'x
s2='hrbfrjj%hshsdhjc&chjshj*dc'
pattern2='[%|&|*]'
lst=re.split(pattern2,s2)
print(lst) #['hrbfrjj', 'hshsdhjc', 'chjshj', 'dc']
```

### 5.12--本章总结

![image-20240717144112431](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717144112431.png)

![image-20240717144306223](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717144306223.png)

## 第六章--异常处理

### 6.1--Bug的由来与分类

中英文，冒号(:),类型的变化，赋值与运算符，

### 6.2异常处理--try

![Snipaste_2024-07-17_20-51-24](D:\视频及壁纸\截屏\Snipaste_2024-07-17_20-51-24.png)

```python
try:
    num1=eval(input('input a number'))
    num2=eval(input('input other number'))
    result=num1/num2
    print('result=',result)
except ZeroDivisionError:
    print('error')
'''
input a number2
input other number0
error
'''
#valueError输出错误，baseException好多异常
#finally无论如何都要要执行，else前面不成立就执行这个
```

### 6.3--raise异常处理

曝出异常

```python
try:
    gender=input('输入你的性别')
    if gender != '男' and gender != '女':
        raise Exception('你是啥？')
    else:
        print('男')
except Exception as e:
    print(e)
```

### 6.4--异常类型

![Snipaste_2024-07-17_21-08-01](D:\视频及壁纸\截屏\Snipaste_2024-07-17_21-08-01.png)

![Snipaste_2024-07-17_21-10-12](D:\视频及壁纸\截屏\Snipaste_2024-07-17_21-10-12.png)

```python
#ValueError
##print(int('a'))
#AttributeError
# i=10
# print(i.name)
#TypeError
#print('hello'+192)
#IndentationError
  print('sjj')
```

### 6.5--调试

断点一般在循环处

![Snipaste_2024-07-17_21-20-02](D:\视频及壁纸\学习\Snipaste_2024-07-17_21-20-02.png)

![image-20240717212713529](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717212713529.png)

## 第七章--函数及常用的内置函数

### 7.1--函数的定义及调用

![Snipaste_2024-07-17_21-29-24](D:\视频及壁纸\学习\Snipaste_2024-07-17_21-29-24.png)

```python
n=10
def get_sum(n):
    sum=0
    for i in range(1,n+1):
        sum+=i
    return sum
print(get_sum(n))
```

### 7.2--参数传递

传入个数，类型，

![image-20240717214306366](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717214306366.png)

![image-20240717214006730](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717214006730.png)

*直接在函数里面赋值，可以直接使用*



![image-20240717214519516](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717214519516.png)

```python
#*,为位置传参，**分开传参
def fun(*para):
    print(type(para))
    for item in para:
        print(item)

fun(10,10,30)
fun(*[10,20,304])
fun([10,20,404])
'''
<class 'tuple'>
10
10
30
<class 'tuple'>
10
20
304
<class 'tuple'>
[10, 20, 404]
'''
```

### 7.3--匿名函数lambda

![image-20240717215431197](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717215431197.png)

```python
#匿名函数就是只有一个返回值，简单的函数
s=lambda a,b:a+b
print(type(s))
print(s(10,20))
#<class 'function'> 30
lst=[10,20,30,40,50]
for i in range(len(lst)):
    print(lst[i])

for i in range(len(lst)):
    result=lambda x:x[i]
    print(result(lst))

```

### 7.4--递归函数

```python
def fac(n):
    if n == 1:
        return 1
    else:
        return n*fac(n-1)

print(fac(6))

def fun(n):
    if n==1 or n==2:
        return 1
    else:
        return fun(n-1)+fun(n-2)
print(fun(9))
```



### 7.5--内置函数--转换类型(各种类型)

#### 1.-------------

![image-20240717221955914](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717221955914.png)

#### 2.--数学函数(round,sum,divmod,pow)

![image-20240717222554517](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717222554517.png)

#### 3.--迭代器函数

![image-20240717223033156](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717223033156.png)

```python
def fun(n):
    return n%2==1
l=filter(fun,range(1,11))
print(list(l))
#[1, 3, 5, 7, 9]
```

#### 4.其他函数

![image-20240717224004315](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240717224004315.png)

## 第八章--面向对象设计

### 8.1--类和对象，Class

类是有对象组成的，类相当于某个种类，类型

![image-20240718153424820](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240718153424820.png)

```python
class Student:
    school='dengzheng senior'
    def __init__(self,name,age):
        self.name='duzhengjin'
        self.age=18
    def show(self):
        print('name=',self.name,'age=',self.age)
    @staticmethod
    def sm():
        print('not finish')

    @classmethod
    def cm(cls):
        print('not finish')
stu=Student('duzheng',18)
stu.show()
print(stu.school)
print(stu.name,stu.age)
stu.sm()
stu.cm()
'''
name= duzhengjin age= 18
dengzheng senior
duzhengjin 18
not finish
not finish
'''
```

### 8.2--动态绑定属性与方法

函数加小括号是调用，不加为复制

```python
class Student:
    school='dengzheng senior'
    def __init__(self,name,age):
        self.name='duzhengjin'
        self.age=18
    def show(self):
        print('name=',self.name,'age=',self.age)
stu=Student('duzhengjin',17)
stu.show()
def introduce():
    print('我是新增的')
stu.add=introduce
stu.add()
'''
name= duzhengjin age= 18
我是新增的
'''
```

### 8.3--面向对象的三大特征

![image-20240718175605993](C:\Users\20148\AppData\Roaming\Typora\typora-user-images\image-20240718175605993.png)

```python
class Student:
    school='dengzheng senior'
    def __init__(self,name,age,gender):
        self._name=name
        self.__age=age
        self.gender=gender
    def _fun1(self):
        print('子类都可以访问')
    def __fun2(self):
        print('只有在类的里面才可以访问')
    def show(self):
        self._fun1()
        self.__fun2()
        print(self._name)
stu=Student('duzhengjin','19','nan')
print(stu._name) #根本无法找到age
print(stu.gender)
stu._fun1()
#stu.__fun2()找不到
stu.show()  #不显示这个类，但可以借助函数使用
#特殊访问
print(stu._Student__age)
stu._Student__fun2()
```

### 8.4--属性的设置--setter

```python
class Student:
    school='dengzheng senior'
    def __init__(self,name,gender):
        self.name=name
        self.__gender=gender
    #可以在外界使用
    @property
    def gender(self):
        return self.__gender
    #可以修改传入的值
    @gender.setter
    def gender(self,value):
        if value != 'man' and value != 'woman':
            print('性别有雾,默认值为男')
            self.__gender='man'
        else:
            self.__gender=value

stu=Student('duzhengjin','man')
print(stu.name,' ',stu.gender) #duzhengjin   man
stu.gender='woman'
print(stu.gender)
```

### 8.5--继承

```python
#父类----------------------------------
class Person:  #默认继承object
    def __init__(self,name,age):
        self.name=name
        self.age=age
    def show(self):
        print(self.name,' ',self.age)
#继承父类--------------------------------
class Student(Person):
    def __init__(self,name,age,id):
        super().__init__(name,age)
        self.id=id
class Doctor(Person):
    def __init__(self,name,age,depa):
        super().__init__(name,age)
        self.depa=depa
        
stu=Student('duzhengjin',17,7206)
stu.show()
print(stu.id)
doc=Doctor('wei',18,'99')
doc.show()
print(doc.depa)
```

### 8.6--多继承

```python
#多继承
class Father1:
    def __init__(self,name1):
        self.name1=name1
    def fun1(self):
        print('Father1')
class Father2:
    def __init__(self,name2):
        self.name2=name2
    def fun2(self):
        print('Father2')
class Son(Father1,Father2):
    def __init__(self,name1,name2,id):
        Father1.__init__(self,name1)
        Father2.__init__(self,name2)
        self.id=id
#----------------------------------------
son=Son('du','zhang','66')
son.fun1()
son.fun2()
print(son.id)

```

### 8.7--方法重写

![Snipaste_2024-07-19_09-39-47](D:\视频及壁纸\学习\Snipaste_2024-07-19_09-39-47.png)

```python
# 父类----------------------------------
class Person:  # 默认继承object
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def show(self):
        print(self.name, ' ', self.age)
# 继承父类--------------------------------
class Student(Person):
    def __init__(self, name, age, id):
        super().__init__(name, age)
        self.id = id
    def show(self):
        super().show()
        print(self.id,'我叼用自己')


class Doctor(Person):
    def __init__(self, name, age, depa):
        super().__init__(name, age)
        self.depa = depa
    def show(self):
        print('我自己写的',f'我的名字是{self.name},我的年龄是{self.age},我的公寓是{self.depa}')

stu = Student('duzhengjin', 17, 7206)
stu.show()
doc = Doctor('wei', 18, '99')
doc.show()
'''
duzhengjin   17
7206 我叼用自己
我自己写的 我的名字是wei,我的年龄是18,我的公寓是99
'''
```

### 8.8--多态

![Snipaste_2024-07-19_09-52-46](D:\视频及壁纸\学习\Snipaste_2024-07-19_09-52-46.png)

不关心是否继承，只关心是否与函数有同名方法

优点：可以在使用过程中动态带用哪种方法

```python
class Cat():
    def eat(self):
        print('i am a cat')
class Dog():
    def eat(self):
        print('i am a dog')
#--------------------
#实现是否有同名方法
def fun(obj):
    obj.eat()
cat=Cat()
dog=Dog()
fun(cat)
fun(dog)
'''fun(cat)
   fun(dog)'''
```

### 8.9--object类

![Snipaste_2024-07-19_10-06-38](D:\视频及壁纸\学习\Snipaste_2024-07-19_10-06-38.png)
