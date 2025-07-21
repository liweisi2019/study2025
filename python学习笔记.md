
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

## 读写
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
```

## 类
```python
class Calculator:
    price = 18
    name = 'Good Calculator'
    def sum(self,x,y):
        print(self.name)  ##self指向自身
        print(x+y)
    def mult(self,x,y):
        print(x*y)

calculator=Calculator()    ##创建对象 
self.price
self.name

```



