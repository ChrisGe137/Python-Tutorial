# 字典（Dictionary）

## 什么是字典
list作为容器已经非常方便，但是引用list中的元素是依赖下标。字典也是一种容器：

+ 与list类似，作为容器，一个字典对象中可以存放多个其他元素
+ 与list不同，字典对象存放的是key-value键值对


现在我们要建立一个考生姓名与考生分数的映射字典，其中考生小张分数为80分，考生小李分数为90分。在 Python 中表示如下：

```python
Dic = {'小张' : 80, '小李' : 90}
```

## 字典的基本操作

### 定义字典
定义字典的方法有很多种，下面我们将依次介绍不同情况下建立字典的方法：

建立空字典：
```python
Dic = {}
```
建立含键值对的字典：
```python
Dic = {'name' : '小张', 'score' : 90}
```
使用 dict() 函数：
```python
Dic = dict({'小张' : 80, '小李' : 90})
```
### 访问字典
在 Python 中，我们可以直接将键放到方括号中获取值，也可以使用 get() 方法获取。

使用方括号：
```python
Dic['小张']
```
使用 get() 方法：
```python
Dic.get('小张')
```

### 修改字典
我们可以对字典中的键值对进行增加、更改或者删除。

其中对于增加和更改字典中的键值对，我们直接对键进行赋值，如果字典中不存在这个键，就会增加新的键值对，如果字典中已经存在这个键，字典中该键对应的值将会进行更新。具体方法如下：

```python
Dic['小张'] = 100
```
当需要对字典中的键值进行删除时，我们可以根据情况完成以下删除任务。

删除指定键值对：
```python
del Dic['小张']
```
使用 pop() 方法，根据键来删除字典中的元素。
```python
Dic.pop('小李')
```
删除全部键值对：
```python
Dic.clear()
```
删除整个字典：
```python
del Dic
```
## 遍历字典中的元素
字典对象中包含了items方法，这个方法会返回一个迭代器对象，我们可以使用 for...in 语法遍历这个迭代器对象。

每次遍历时，可以同时拿到key和value。

这里我们重新定义一个字典：
```python
Dic = dict({'小张' : 80, '小李' : 90, '小黄' : 100, '小耀' : 100})
```
下面，我们将遍历这个字典：
```python
for key, value in Dic.items():
    print(key, value)
```
到这里你将掌握以下内容：
+ 什么是字典。
+ 如何创建，访问以及修改字典。
+ 如何遍历字典中的元素。
