# Python





## 变量与基本数据类型

### 字符串

* 大小写

```python
"hello 'good' nice"
'hello "good" nice'

a = "hello"

a.title()
a.upper()
a.lowwer()
```

* 变量

```python
b="world"
c=f"{a} {b}"
print(c.title)
```

* 空白

```python
\n \t 

a.strip()
a.rstrip()
a.lstrip()
```

### 数字

* 任意两数相除，结果总为浮点数

* 易读的下划线

  > 1000 = 1_000

* 同时赋值

  > a , b , c = 0 , 0 , 0 

* 常量（大写）

  > MAX = 500
  
* 幂次

  > * *

### 注释

> #

### import this





## 列表

### 修改 添加 删除

* 访问
* 修改
* 添加

> append
> insert

* 删除

  > del
  >
  > pop

### 排序

#### 永久排序

> list.sort 
>
> > sort(reverse == True)

#### 临时排序

> sorted(list)

#### 反转

> reverse

#### 列表长度

> len





### 操作列表 （第四章）

#### 遍历

> <u>for</u> plant in plants:
>
> 使用缩进跳出循环

#### 创建数值列表

* range

  > range(a,b) 
  >
  > > 创建 b-a 个数
  >
  > range(a,b,c)
  >
  > > for（a ; a<11 ; a += c )

* 简单统计

  > min
  >
  > max
  >
  > sum

* 列表解析

  > ```python
  > squares = [value**2 for value in range(1, 11)]
  > print(squares)
  > ```
  >
  > 

#### 使用列表的一部分

* 切片

  > list[ a : b ]

* 复制列表

  > listA = listB[ : ]

#### 元组

* 概念

  > Python将不能修改的值称为不可变的
  >
  > 而不可变的列表被称为元组 。

* 定义元组

  > tuple = ( a , b , c ····)
  >
  > tuple =   a , b , c ····
  >
  > > 元组由 逗号 标识 ，可以不使用圆括号

* 遍历

* 修改元组变量

  > 重新定义

#### PEP

* Python改进提案 

  > Python Enhancement Proposal，PEP





### if （第五章）

#### 条件测试

* 检查多个条件

  > A and B
  >
  > A  or  B

* 检查特定值是否  包含 在列表中

  > A in listA

* 检查特定值是否 不包含 在列表中

  > A not in listA

#### if语句

* 作用范围

  > 判断缩进（ 同 for ）

* if-else

  > if balabala:
  > 		do sth
  > else baba:
  > 		do sth

* if-elif-else

  > elif == else if

#### 使用 if 处理列表

* 确定列表不是空的

  > if list:
  >
  > ​		(不为空)
  >
  > if not list:
  >
  > ​		(为空)





### 字典（第六章）

#### 概念

> java类

#### 定义与基本使用

> dictionary = { 'A' = ' a', 'B' = 2, ······ }
>
> print ( dictionary [ 'A' ] )
>
> dictionary [ 'new C' ] = 'c'
>
> del dictionary [ 'A' ]

* get

  > a_value = dicitionary.get [ 'A' , ' A no value' ]

#### 遍历字典

> for key,value in dictionary.items() :
> for key in dictionary.keys() :
> for value in dictionary.values() :
>
> 

