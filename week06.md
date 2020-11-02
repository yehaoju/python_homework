## **总结关于字典、集合的所有方法**
### 1. 字典

| dict.clear() | 删除字典内所有元素 |
| dict.copy() | 返回一个字典的浅复制 |
| dict.get(key, default=None) | 返回指定键的值，如果值不在字典中返回default值 |
| dict.has_key(key) | 如果键在字典dict里返回true，否则返回false |
| dict.items() | 以列表返回可遍历的(键, 值) 元组数组 |
| dict.keys() | 以列表返回一个字典所有的键 |
| dict.update(dict2) | 把字典dict2的键/值对更新到dict里 |
| dict.values() | 以列表返回字典中的所有值 |
| popitem() | 返回并删除字典中的最后一对键和值。 |
| pop(key[,default]) | 删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。 |
| dict.setdefault(key, default=None) | 和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default |
| dict.fromkeys(seq[, val]) | 创建一个新字典，以序列 seq 中元素做字典的键，val 为字典所有键对应的初始值 |

字典是另一种可变容器模型，且可存储任意类型对象。

字典的每个键值 key=>value 对用冒号 : 分割，每个键值对之间用逗号 , 分割，整个字典包括在花括号 {} 中 ,格式如下所示：
```
d = {key1 : value1, key2 : value2 }
```
键一般是唯一的，如果重复最后的一个键值对会替换前面的，值不需要唯一。
```
>>> dict = {'a': 1, 'b': 2, 'b': '3'}
>>> dict['b']
'3'
>>> dict
{'a': 1, 'b': '3'}
```
值可以取任何数据类型，但键必须是不可变的，如字符串，数字或元组。

一个简单的字典实例：
```
dict = {'Alice': '2341', 'Beth': '9102', 'Cecil': '3258'}
```
也可如此创建字典：
```
dict1 = { 'abc': 456 }
dict2 = { 'abc': 123, 98.6: 37 }
```
访问字典里的值
把相应的键放入熟悉的方括弧，如下实例:

```
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
 
print "dict['Name']: ", dict['Name']
print "dict['Age']: ", dict['Age']
```
以上实例输出结果：
```
dict['Name']:  Zara
dict['Age']:  7
```
修改字典
向字典添加新内容的方法是增加新的键/值对，修改或删除已有键/值对如下实例:

实例
```
 
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
 
dict['Age'] = 8 # 更新
dict['School'] = "lalalala" # 添加
 
 
print "dict['Age']: ", dict['Age']
print "dict['School']: ", dict['School']
```
以上实例输出结果：
```
dict['Age']:  8
dict['School']:  lalalala
```
### 2. 集合
集合初始化

集合是一个拥有确定（唯一）的、不变的的元素，且元素无序的可变的数据组织形式。

你可以使用「set()」操作初始化一个空集。
```
emptySet = set()
```
如果要初始化一个带有值的集合，你可以向「set()」传入一个列表。
```
dataScientist = set(['Python', 'R', 'SQL', 'Git', 'Tableau', 'SAS'])

dataEngineer = set(['Python', 'Java', 'Scala', 'Git', 'SQL', 'Hadoop'])
```
如果你观察一下上面的「dataScientist」和「dataEngineer」集合中的变量，就会发现集合中元素值的顺序与添加时的顺序是不同的，这是因为集合是无序的。

集合包含的值也可以通过花括号来初始化。
```
dataScientist = {'Python', 'R', 'SQL', 'Git', 'Tableau', 'SAS'}​

dataEngineer = {'Python', 'Java', 'Scala', 'Git', 'SQL', 'Hadoop'}​
```
向集合添加值或删除值

要想向集合中添加值或从中删除值，你首先必须初始化一个集合。

```
graphicDesigner = {'InDesign', 'Photoshop', 'Acrobat', 'Premiere', 'Bridge'}​
```
向集合中添加值

你可以使用「add」方法向集合中添加一个值。
```
graphicDesigner.add('Illustrator')
```
需要注意的一点是，你只能将不可变的值（例如一个字符串或一个元组）加入到集合中。举例而言，如果你试图将一个列表（list）添加到集合中，系统会返回类型错误「TyprError」。
```
graphicDesigner.add(['Powerpoint', 'Blender'])
```
从集合中删除值

有好几种方法可以从集合中删除一个值：


可以使用「pop」方法从集合中删除并且返回一个任意的值。
```
graphicDesigner.pop()
```
需要注意的是，如果集合是空的，该方法会返回一个「KeyError」。

删除集合中所有的值

你可以使用「clear」方法删除集合中所有的值。
```
import random

num = random.randint(1, 100)
guess_chances = 6
print('请你在1到100之间猜一个数字，您只有6次猜数字的机会哦！')

for i in range(1, guess_chances + 1):
    print('这是第' + str(i) + '次猜数字')
    guess = input('请输入数字：')
    if guess.isdigit():
        guess = int(guess)
        if guess < num:
            print('您输入的数字太小了，您还有' + str(guess_chances - i) + '次机会，请重新输入：')
        elif guess > num:
            print('您输入的数字太大了，您还有' + str(guess_chances - i) + '次机会，请重新输入：')
        elif guess == num:
            print('恭喜您猜对了')
            break
    elif guess == 'q':
        print('退出游戏！')
        break
    else:
        print('输入的内容必须为整数，请重新输入：')
while (guess_chances - i) == 0:
    print('您输入已经超过6次，但你还未猜对数字，游戏结束！')
    break
```
运行结果：
```
请你在1到100之间猜一个数字，您只有6次猜数字的机会哦！
这是第1次猜数字
请输入数字：50
您输入的数字太小了，您还有5次机会，请重新输入：
这是第2次猜数字
请输入数字：70
您输入的数字太小了，您还有4次机会，请重新输入：
这是第3次猜数字
请输入数字：80
您输入的数字太小了，您还有3次机会，请重新输入：
这是第4次猜数字
请输入数字：90
您输入的数字太小了，您还有2次机会，请重新输入：
这是第5次猜数字
请输入数字：95
恭喜您猜对了

Process finished with exit code 0

```

## **课本代码练习（关于第三章p95～p144的代码）**
## **4、字典查询练习：Azure API 提供一张含有>=3张脸（3个以上faceid）的图片，先用json()获取内容（results），在用数据结构查询的方式查找到：眼镜、肤色、微笑指数、头发颜色、年龄、性别这几项数据，并分别存进变量/自定义数据结构（如字典等）当中。**

