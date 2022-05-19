# Python

# 基本使用



## 小拓展

### import this

### PEP

* Python改进提案 

  即代码规范

  Python Enhancement Proposal，PEP

## 变量与基本数据类型

### 字符串

```python
"hello 'good' nice"
'hello "good" nice'

a = "hello "
a += "World"
# a == "hello World"

a.title()
a.upper()
a.lowwer()
```

### 变量

```python
b="world"
c=f"{a} {b}"
print(c.title)
```

### 空白

```python
\n \t 

a.strip()
a.rstrip()
a.lstrip()
```

### 数字

* 任意两数相除，结果总为浮点数

* 易读的下划线

  ```python
  1000 == 1_000
  ```

* 同时赋值

  ```python
  a , b , c = 0 , 0 , 0 
  ```

* 常量（大写）

  ```python
  MAX = 500
  ```
  
* 幂次

  ```python
  2*2*2 == 2 ** 3
  ```

### 注释 #

```python
#
"""hhh"""
```







## 列表

### 定义

```python
list = [ 'A' , 'B' , 'C' ······ ]
```

### 修改 添加 删除

* 访问

* 修改

* 添加

  append

  > v. <正式>附加，增补

  ```python
  list.append( A )
  ```

  insert

  ```python
  list.insert( 0 , A )
  ```

* 删除

  del
  
  ```python
  del list[0]
  ```

* 弹出

  pop

  ```python
  a = list.pop( ) #默认弹出最后一个
  a = list.pop(0)
  ```

### 排序

#### 永久排序

```python
list.sort() 
list.sort(reverse == True)
```

#### 临时排序

```python
sorted(list)
```

#### 反转

```python
list.reverse()
```

#### 列表长度

```python
len( list )
```

### 索引

```python
list[-1]  #返回倒数第一个元素
```





## 操作列表 

### 遍历

使用缩进跳出循环

```python
for plant in plants:
	do sth
```

### 数值列表

#### 创建数值列表 range()

* 创建 b-a 个数

  ```python
  range(a,b) 
  ```

* 指定步长

  ```python
  range(a,b,c) #for（a ; a<11 ; a += c )
  ```

#### 简单统计

```python
min(list)
max(list)
sum(list)
```

#### 列表解析

```python
squares = [value**2 for value in range(1, 11)]
print(squares)
```

### 使用列表的一部分

#### 切片

```python
list[ a : b ]
```

#### 复制列表

```python
listA = listB[ : ] 	 #将B复制给A（两个列表）
listA = listB		#让A指向B（一个列表，两个名字）
```

### 元组

* 概念

  不可变/不可修改的 列表被称为元组 。
  
* 定义元组

  元组由 逗号 标识 ，可以不使用圆括号

  ```python
  tuple = ( a , b , c ····)
  tuple =   a , b , c ···· 
  ```

* 遍历

* 修改元组变量

   重新定义



## if 

### 条件检查

* 检查多个条件

  ```python
  A and B
  A  or  B
  ```

* 检查特定值是否  包含 在列表中

  ```python
  if A in listA
  ```

* 检查特定值是否 不包含 在列表中

  ```python
  if A not in listA
  ```

### if语句

* 作用范围

  判断缩进（ 同 for ）

* if-else

  ```python
  if balabala:
  		do sth
  else baba:
  		do sth
  ```

* if-elif-else

  elif == else if

### 使用 if 处理列表

* 确定列表不是空的

  ```python
  if list:(不为空)
  if not list:(为空)
  ```
  
  

## 字典

### 概念

类似java类

### 定义与基本使用

```python
dictionary = { 'A' : ' a', 'B' : 2, ······ }

print ( dictionary [ 'A' ] )

dictionary [ 'C' ] = 'c'

del dictionary [ 'A' ]
```

获取值 get

```python
a_value = dicitionary.get [ 'A' , ' A no value' ]
```

### 遍历字典

```python
for key,value in dictionary.items() :
for key in dictionary.keys() :
for value in dictionary.values() :
```

### 集合 set

不可重复

```python
set = { 'A' , 'B' , 'C'  ·····}
for value in set ( dictionary.values() )
```

### 嵌套

* 列表套字典
* 字典套列表
* 字典套字典



## 输入 和 while

### 输入 input

```python
Input = input("this is hint: ") 
```

input 获得的值为字符

将字符转为int

```python
a = int(Input)
```

### while

## 函数

### 定义

```python
def fun1():
    print("fun1")
    
fun1()
```

### 参数

#### 传参数

可以为 简单变量、列表 

```python
def fun(Type,Name):
    print(f"my {Type} is called {Name}")
    
fun('dog','buster')
fun(Name = 'buster',Type = 'dog')
```

#### 设置默认参数

```python
def fun(Type ='dog' , Name):
    print(f"my {Type} is called {Name}")
    
fun('slinky')
fun('horse','pony')
fun(Type = 'horse',Name = 'pony')
```

#### 让参数变成可选的

```python
def get_formatted_name(first_name, last_name, middle_name=''):
    if middle_name:
		full_name = f"{first_name} {middle_name} {last_name}"
    else:
		full_name = f"{first_name} {last_name}"
	return full_name.title()
```

#### 禁止函数修改列表参数

使用 [:] 为列表创建副本

```python
def fun(list[:])
	do sth
```

#### 传递任意数量的参数

* 传递任意数量的实参

  使用 * 创建空元组 

  ```python
  def fun(*a)
  	do sth
  ```

* 传递任意数量的关键字实参

  使用 ** 接收键值对

  ```python
  def fun(**a)
  	do sth
  ```

### 返回值

值：简单变量 字典 列表



## 类

class

### 基本使用

#### 定义

_ _ init _ _ == 构造器
self == this

```python
class A:
	def __init__(self,a,b):
		self.a = a
		self.b = b
		self.c = 0 #新定义一个属性
        
	def fun1():
		do sth
```

#### 调用

```python
# 新建一个实例
my_a = A("a","b")

# 调用方法
my_a.fun1()
```

#### 修改属性的值

直接修改
方法修改

### 继承



## 文件

### 打开文件

```
open('file','?') 
```

`'w'` 	： 写入模式 write
`'r'`	 ： 读取模式 read
`'a'`	 ：附加模式 append
`'r+'`	：读写模式 read + write

### 写入文件

```
file.write()
```

### 读取文件

```python
file.read()
file.readlines()
```

### 存储数据

JSON : **J**ava**S**cript**O**bject**N**otation

* ```python
  import json
  ```

* 写入 json.dump()

  ```python
  json.dump(contents,filename)
  ```

* 读取 json.load()

  ```python
  contents = json.load(filename)
  ```

  



## 异常

如果try正常 执行else `(A+C)`
如果try异常 执行except `(B)`

```python
try:
	do A
except sth:
	do B
else :
	do C
```

* pass 

  do nothing 什么都不做

  

## 导入

### 导入其他 .py文件 

```python
import A.py文件

# 使用A文件的a函数
A.a()
```

### 导入函数

* 导入其他文件的全部函数

  ```python
  from A import *
  
  # 使用A文件的a函数
  a()
  ```

* 导入特定的函数

  ```python
  from A import a
  from A import a,b,c
  
  a()
  ```

### 起别名

```python
import A as A_module
from A import a as a_fun
```

### 导入类

```python
from A_file import A_class
```

### 导入文件

```python
with open(file_name) as name:
	contents = name.read()
	contents = name.readlines()
```



### 标准库 

自动包含





## 测试代码

> **看不懂**
>
> ```
>  if __name__ == '__main__':
>  unittest.main()
> ```
>
> ```
> 我们将直接运行这个文件，但需要指出的是，很多测试框架都会先导入测试文件再运行。导入文件时，解释器将在导入的同时执行它。❹处的if 代码块检查特殊变量__name__ ，这个变量是在程序执行时设置的。如果这个文件作为主程序执行，变量__name__ 将被设置为'__main__' 。在这里，调用unittest.main() 来运行测试用例。如果这个文件被测试框架导入，变量__name__ 的值将不是'__main__' ，因此不会调用unittest.main() 。
> ```

### 测试函数

* 导入模块 unittest
* 导入函数
* 创建 Test(unittest.TestCase) 类
* 创建方法（test_开头）
* 调用函数
* 断言方法

### 测试类

* 导入模块 unittest
* 导入类
* 创建 Test(unittest.TestCase) 类
* 创建方法（test_开头）
* 调用类（里的方法）
* 断言方法

### 断言方法

<img src="https://s2.loli.net/2022/05/15/xJmYfPVguGB4W3j.png" alt="image-20220515160355870"  />

### setUp方法

在多个test\_函数里面，有可能会重复创建对象
setUp函数在各个test\_之前被调用，并为之后的测试提供已经创建的对象



# 外星人

## PyGame

可用于管理图形、动画乃至声音。通过使用Pygame来处理在屏幕上绘制图像 等任务，可将重点放在程序的高级逻辑上。

## 创建窗口

```python
self.screen = pygame.display.set_mode((1200, 800))
```

赋给属性self.screen 的对象是一个surface 。在Pygame中，surface是屏幕的一 部分，用于显示游戏元素。在这个游戏中，每个元素（如外星人或飞船）都是一个 surface。display.set_mode() 返回的surface表示整个游戏窗口。激活游戏的 动画循环后，每经过一次循环都将自动重绘这个surface，将用户输入触发的所有变 化都反映出来。

```python
self.screen = pygame.display.set_mode((0, 0), pygame.FULLSCREEN)
self.settings.screen_width = self.screen.get_rect().width
self.settings.screen_height = self.screen.get_rect().height
```

创建屏幕时，传入了尺寸(0, 0) 以及参数pygame.FULLSCREEN （见❶）。这让 Pygame生成一个覆盖整个显示器的屏幕。由于无法预先知道屏幕的宽度和高度，要 在创建屏幕后更新这些设置（见❷）：使用屏幕的rect 的属性width 和height 来更新对象settings 。



* 在Pygame中，原点(0, 0)位于屏幕左上角
* 在 Python中，辅助方法的名称以单个下划线打头
* 

