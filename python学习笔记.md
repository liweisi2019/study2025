
## python的安装与环境变量  (待定)

## 基本运算

加    +
减    -
乘    *
除    //
取模  %
平方  **

### 自变量
```python
赋值方法1. a=1,b=2,c=3
        2. a,b,c=1,2,3
```

        
### while和for循环

##利用对齐来判断while循环位置

#### while      
```python
condition =1;
while condition <10:
  condition+=1
  print(condition)
print(a)
```
   

### for

```python
array=[1,3,5,6,7,8]
for i in array:
    print(i)

for i in range(1,10)    ##输出1-9
    print(i)

for i in range(1,10,2) ##1-9步长为2

```
##框选对齐的语句后  
ctrl+[  左tab  
ctrl+]  右tab

### if elif else 
break跳出循环  
continue跳过这次循环 今日下一次循环
```python
a,b,c=1,2,3
if a>b :
    print('a>b')
elif c<b :
    print('c<b')
else :
    print('a<b')
```

### def
```python
def function():##定义函数  自定义函数名
    a=1+2
    print(a)
function()     ##调用函数

```
### 函数参数 默认参数

```python
def book(price,name='book1'):    ##注:默认参数必须放在普通参数后面
    print(name+'\'s price is '+str(price))

book(200)

```
### 全局变量和局部变量

局部变量 local  仅作用于函数内部  
全局变量 global
```python
 a=None
def sum()
    a=20            ##global a=20  时 才说明使用的全局变量a 否则是函数内部的a
    return a+100
print(sum())    ##120
print(a)        ##None

```

## python库的安装
linux pip  
windows 百度 

## 读写 与  接收
```python
##写入模式
text="this is a text\nthis is the second line"
my_file=open('text.txt','w')   ##  后面为读写方式
my_file.write(text)
my_file.close()

##添加模式
appended_text="\nthis is the appended line"
my_file=open('text.txt','a')   ##  appended添加模式
my_file.write(appended_text)
my_file.close()

##读取模式
## readline 一行一行进行读取  readlines读取全部
file=open('text.txt','r')
firstline=file.readline()    ##第一次读取第一行
secondline=file.readline()   ##第二次读取第二行 
thirdlin=file.readline()    ##第三次读取第三行
print(firstline,secondline,thirdline)

##接收
a_input=input('please give me a number\n')  ##接收到string类型数据
##a_input=int(input('please give me a number\n'))   int 数据

if a_input=='1':
    print('u choose one')
elif a_input =='2':
    print('u choose two')
else :
    print('u choose other')


```

## 类
```python
class Calculator:

    def __init__(self,name,price=20):    ##类似于构造函数  需要引入参数时使用 无参数无法构建类  可以使用默认参数
        self.name=name
        self.price=price
    def sum(self,x,y):
        print(self.name)  ##self指向自身
        print(x+y)
    def mult(self,x,y):
        print(x*y)

calculator=Calculator()    ##创建对象 
self.price
self.name

```
## 元组() 和 列表(数组)[]
元组不可变  
列表可变
```python
a_arr1=(1,3,5,7,9)  
a_arr2=2,4,6,8,10

#遍历
for i in a_arr1 :
    print(i)

for index in range(len(a_arr2)) :  ##index为索引
    print(a_arr2[index])

##列表list
a=[1,2,4,5,6,7]
a.appended(8)   #在末尾添加8
a.insert(3,4)  #在索引值为3的地方添加4
a.remove(4)    #删除第一个4
print(a[-1])   #最后一位 
print(a[3:4])  #打印索引值为3 4的值
a.index(3)   #第一个3的索引
a.count(3)  #出现3的次数
a.sort()    #默认从小到大 参数为reverse=True时 从大到小
```

## 二维数组

```python
a_multarr=[ [1,2,3],
            [4,5,6],
            [7,8,9] ]

for i in a_multarr:
    print(i)

```

## 字典(无顺序){}



```python
a_list=[1,2,3,4,5]

d1={'apple':1,'pear':2,'orange':3}
d2={1:'a',2:'b'}
print(d1['apple']) #1 

print(d2[1])     # a

del d1['orange']   #删除元素

print(d1)  #{'apple': 1, 'pear': 2}

d1['qwer']=50  #增加元素队

print(d1)  #{'apple': 1, 'pear': 2, 'qwer': 50}

#字典的内容可以是数组、字典、或函数

dic={'a':1,'b':[1,3,5],'c':function,'d':{'q':2,'w':4}}

print(dic['d']['q'])   #  2


```

## import载入模块  与 本地模块

```python
#时间模块
import time   ##  import time as t    简称

print(time.localtime()) #显示当前时间   t.localtime()
print(time.time()) #表示从 1970 年 1 月 1 日 00:00:00 UTC 到现在的秒数  用来计算代码耗时 结束时间减去开始时间

from  time  import time,localtime      #仅仅使用time中的这两个函数
print(localtime())

from time import *    #忽略time导入所有功能

#本地模块(在同一目录下) (或放在sitepackage目录下)
#localproject.py
#def shownum():
#    print('number')        
import localproject

localproject.shownum()


```
## 错误处理及通用的打开文件流程

```python
try :                                 #接下来代码可能会出错  如果出错 跳转到except部分
    file=open('text1.txt','r+')       # r+ 读写模式但文件必须存在
except Exception as e:     #Exception用来捕获异常原因  告诉程序如果出错别崩溃 交给我  
    print('出错原因:',e)
    response = input('do u want to create it? y/n')
    if response=='y':
        file=open('text1.txt','w')
    else:
        pass
else:
    file.write('ssss')
    file.close()  
  

```

##  zip lambda map
```python
##zip 合并
a=[1,2,3]
b=[4,5,6]
c=list(zip(a,a,b))  #  zip执行合并动作  list将其转为列表
print(c)      ##[(1, 1, 4), (2, 2, 5), (3, 3, 6)]

## lambda定义简单表达式
def func1(x,y):
    return (x+y)

func2=lambda x,y:x+y
func1(2,3)
func2(2,3)

##map 把迭代器里的每个对应元素依次交给函数处理 返回处理后结果
list(map(func1,[2,3],[4,5]))  # [2+4,3+5] [6,8]
```

## 深浅拷贝copy deepcopy

```python
import copy
#浅拷贝 第一层不一样 二层及以上相同 只复制对象本身，不递归复制它内部嵌套的可变对象
#从地址来看 a中的内容如下[1,2,address[4,5]] 因为复制了地址 所以内部嵌套结构未改变？
a=[1,2,[4,5]]
b=copy.copy(a)
b[0]=6
b[2].append(7)
print(a)      ## [1,2,[4,5,7]]
print(b)      ##[6,2,[4,5,7]]

##深拷贝   完全复制 不相同

```
## 多线程 thread
待补充

## 多核
待补充

## tkinter 简单窗口视图
待补充

## pickle存放数据 及便捷文件处理
```python
import pickle
dict={'a':1,'b':[1,2,3],3:{'q':[3,4,5],'w':667}}
file=open('pickle_data.pickle','wb')   #计算机可以识别的语言
pickle.dump(dict,file) #将dict的内容存入file
file.close()

#打开
with open('pickle_data.pickle','rb') as file :     #使用with不用考虑关闭
    dict2=pickle.load(file)  #将文件载入到新的字典中
print(dict2)   



```
## set找不同
set中的元素不重复且无序
```python
list1=['a','b','c','b','a']
print(set(list1))   # {'c', 'a', 'b'}   无序
unique_char=set(list1) # {'c', 'a', 'b'}
unique_char.add('x')    #{'c', 'a', 'b','x'}
unique_char.add('a')    #无操作{'c', 'a', 'b','x'}
print(unique_char.remove('a'))    #有则删除a 无则报错  unique_char.remove('a')返回值为None
print(unique_char.discard('a'))  #有则删除 无则不报错   unique_char.discard('a')返回值为None
unique_char.clear()     #set()     空

list2=['x','y']
print(list2.difference(list1))  ##两字典不同的地方
print(list2.intersection(list1))  ##两字典相同的地方
```

## 正则表达式Regex

```python
import re
#一般形式找
pattern1="cat"
pattern2="dog"
string ="there is a dog"
print(pattern1 in string)   # Flase
print(pattern2 in string)   # True

#正则表达式查找

print(re.search(pattern1,string)) # None
print(re.search(pattern2,string)) # <re.Match object; span=(11, 14), match='dog'>  在[11，14）索引值位置

#r之后不考虑转义
ptn=r"r[au]n"    # run /ran
print(re.search(r"r[au]n","there is a dog"))
print(re.search(r"r[A-Z]","there is a dog"))  # r"r[0-9]n"   r"r[0-9A-Z]n"
##下面视频没看 直接复制笔记  用到再说

\d 匹配数字形式
\D 匹配除了数字形式

\s 匹配所有空白符
\S 匹配除了所有空白符


\w 匹配所有字母数字
\W 匹配除了所有字母数字

\b 匹配文字前一个空白字符
\B 匹配文字前空白字符

\\匹配反斜杠\

注意：上述\表示为去除字母/数字本身含义

. 匹配除了\n的任何
^ 匹配句首
$ 匹配句尾
？ 匹配是否
多行匹配 re.M

*：0或多次
+：1或多次
可选次数


group组
group（1）指定第一个括号里的东西
给group组加个名字 ？P<id>
findall寻找所有匹配
|或者

re.sub()替换
re.split()分裂
compile编译




```



