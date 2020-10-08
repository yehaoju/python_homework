### 1.利用datatime模块与if语句做一个课程提醒工具 
```
from datetime import datetime
today = input("请输入星期几的英文：")
if today == "Monday":
    print("8.00-9.30 写作训练 12.50-14.20 大学英语 14.30-16.50 用户视觉界面设计")
elif today == "Tuesday":
    print("12.50-14.20 AI软件应用 14.30-16.50 兵乒球")
elif today == "Wednesday":
    print("8.00-9.30 大学英语 9.45-12.00 毛概 18.45-20.50 Python语言")
elif today == "Thursday":
    print("18.45-20.50 毛概实践")
elif today == "Friday":
    print("12.50-14.20 常用药物知识 14.30-16.50 API、机器学习与人工智能")
elif today == "Saturday":
    print("完成一周的作业、学习、复习、锻炼身体")
elif today == "Sunday":
    print("学习、出去打打球、打打游戏、锻炼")
```

### 2.利用random 模块与if 语句做一个“猜猜的小游戏”
```
name = input("输入姓名")
import random
c = random.randint(1.,10)
if c>5:
    print("今天也要加油呀")
elif 5>c>3:
    print("你只管努力，剩下的交给时间")
elif c<3:
    print("加油呀，少年！！")
```

### 3.利用for循环与range内置函数打印一个9*9的乘法口诀”
```
for i in range(1, 10):
    print()
    for j in range(1, i + 1):
        print("%d*%d=%d," % (i, j, i * j), end=' ')
```
