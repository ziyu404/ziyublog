
# 列表，元组
[列表、元组基础-白月黑羽](https://www.byhy.net/tut/py/basic/07/)
##  熟练
 1. 列表，元组支持切片选择
 2. 列表添加数据和修改数据一样，直接选择赋值即可
 3. 判断是否元素在列表中，in关键字
 4. 元组内容不可变

## 待加强

### 连接两个列表
直接加号连接即可

### 列表、元组多赋值
列表、元组的元素个数和变量数量相同的时候可以实现多赋值
```python
list=[1,2,3]  
x,y,z=list  
print(x,y,z)

## 1 2 3
```
### 切片实现列表的倒排等
切片一般选取为`star:end`，因次`::`表示选取全部，当`::number`表示以number步长选择列表元素
```python
list1=[1,2,3,4]  
print(list1[::-1])

##[4, 3, 2, 1]
```

## 列表内置方法

### 列表最后添加数据：append
`list.(data)`方法在原来列表最后面添加数据,返回none
```python
list=[1,2,3]  
list.append(4)  
print(list)

##[1, 2, 3, 4]
```

### 列表指定位置插入数据：insert
`list.insert(idx,data)`在列表的指定索引位置插入数据，返回none
```python
list=[1,2,3]  
list.insert(1,4)  
print(list)

##[1, 4, 2, 3]
```

### 由索引删除列表元素：pop
`list.pop(idx)`根据填入的索引删除列表元素,返回值为找打的元素
```python
list=[1,2,3]  
returndata=list.pop(1)  
print(list)  
print(returndata)

## [1, 3]
## 2
```

### 由值删除列表元素：remove
`list.remove(value)`根据填入的值找到第一个符号的删除列表元素，返回值为none
```python
list=[1,2,3]  
returndata=list.remove(1)  
print(list)  
print(returndata)

## [2, 3]
## None
 
```

### 翻转列表：reverse
`list.reverse()`翻转原列表，返回为none
```python
list=[1,2,3]  
returndata=list.reverse()  
print(list)  
print(returndata)

## [3, 2, 1]
## None

```

### 返回值的索引：index
`list.index(value)` 返回值在列表中的位置，也就是索引

```python
var1 = [1,2,3,4,5,6,7]
idx = var1.index(5)
print(idx)

## 4
```

### 根据自定义函数对列表进行排序：sort
`list.sort(reverse=False|True,key=myfun)`  根据myfun函数的返回值进行排序

|  参数   | 类型       | 描述                    |
|:-------:| ---------- | ----------------------- |
| reverse | 可选       | 默认False升序，True降序 |
|  myfun  | 函数、可选 | 自定义的排序函数        |
```python

def myfun(value):  
    return  len(value)  
  
list=['abcd','ab','abcde','a','abc']  
returndata=list.sort(key=myfun,reverse=False)  
print(returndata)  
print(list)

##None
## ['a', 'ab', 'abc', 'abcd', 'abcde']
```

[[遇到问题#对可迭代对象进行排序：sorted]]
