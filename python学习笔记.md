
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

##python库的安装
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
## 元组 和 列表[]
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
字典的内容可以是数组、字典、或函数  
jj


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


```
