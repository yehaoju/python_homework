### 1.尝试用户输入学生一周的课表信息，尝试用 占位符、2种format打印学生信息（可设计）
#### 使用占位符打印学生信息
```
name = input("请输入名字；")
monday = input("请输入周一的课程及时间段:")
tuesday = input("请输入周二的课程及时间段:")
wednesday= input("请输入周三的课程及时间段:")
thursday= input("请输入周四的课程及时间段:")
friday= input("请输入周五的课程及时间段:")
saturday= input("请输入周六的课程及时间段:")
sunday= input("请输入周七的课程及时间段:")
info = '''-------CLASS FOR %s -------
Name:%s
monday:%s
tuesday:%s
Wednesday:%s
Thursday:%s
Friday:%s
Saturday:%s
Sunday:%s
'''% (name,name,monday,tuesday,wednesday,thursday,friday,saturday,sunday,)

print(info)
```

#### 使用format打印学生信息
```
name = input("请输入名字：")
monday = input("请输入周一的课程及时间段：")
tuesday = input("请输入周二的课程及时间段：")
wednesday = input("请输入周三的课程及时间段：")
thursday = input("请输入周四的课程及时间段：")
friday = input("请输入周五的课程及时间段：")
saturday = input("请输入周六的课程及时间段：")
sunday = input("请输入周七的课程及时间段：")

info2 =  '''-------CLASS FOR {0} -------
Name:{0}
Monday:{1}
Tuesday:{2}
Wednesday:{3}
Thursday:{4}
Friday:{5}
Saturday:{6}
Sunday:{7}
'''.format(name,monday,tuesday,wednesday,thursday,friday,saturday,sunday,)
print(info2)
```

### 2. 用户输入查询日期和时间，可返回对应的课表信息；用户查询当前时间，可返回当前课表信息

```
a=input("输入星期几的课表，可打印当天的课表")
if a == "monday":
    print(monday)
elif a == "tuesday":
    print(tuesday)
elif a == "wednesday":
    print(wednesday)
elif a == "thursday":
    print(thursday)
elif a == "friday":
    print(friday)
elif a == "saturday":
    print(saturday)
elif a == "sunday":
    print(sunday)
```

### 3. Python内置数据结构 列表 切片、方法练习








