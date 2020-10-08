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

### 运行结果
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
### 运行结果
```
1*1=1, 
2*1=2, 2*2=4, 
3*1=3, 3*2=6, 3*3=9, 
4*1=4, 4*2=8, 4*3=12, 4*4=16, 
5*1=5, 5*2=10, 5*3=15, 5*4=20, 5*5=25, 
6*1=6, 6*2=12, 6*3=18, 6*4=24, 6*5=30, 6*6=36, 
7*1=7, 7*2=14, 7*3=21, 7*4=28, 7*5=35, 7*6=42, 7*7=49, 
8*1=8, 8*2=16, 8*3=24, 8*4=32, 8*5=40, 8*6=48, 8*7=56, 8*8=64, 
9*1=9, 9*2=18, 9*3=27, 9*4=36, 9*5=45, 9*6=54, 9*7=63, 9*8=72, 9*9=81, 
```
