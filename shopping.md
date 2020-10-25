## __购物车python代码__
```
product_list = [
    ('Python书籍', 120),
    ('自行车', 600),
    ('iPhone 12 Pro', 9999),
    ('奶茶', 12),
    ('暗影精灵6', 7000),
    ('水蜜桃', 20),
]

shopping_list = []
salary = input("请输入你的支付宝余额:")
if salary.isdigit():
    salary = int(salary)
    while True:
        print("------❥商品列表❥-------")
        for index, item in enumerate(product_list):
            # print(product_list.index(item),item)
            print(index,item)
        user_choice = input("请选择你购买的商品，或输入【退出】即可退出购物并查看已经购买商品的购物清单：")
        if user_choice.isdigit():
            user_choice = int(user_choice)
            if user_choice < len(product_list) and user_choice >= 0:
                p_item = product_list[user_choice]
                if p_item[1] <= salary:
                    shopping_list.append(p_item)
                    salary -= p_item[1]
                    print("added %s into shopping cart,your balance is %s" % (p_item, salary))
                else:
                    print("你的余额只剩%s,无法购买" % salary)
            else:
                print("商品不在商品列表")
        elif user_choice == '退出':
            print('--------☆消费列表☆----------')
            for p in shopping_list:
                print(p)
            print("您的余额是：", salary)
            exit()
        else:
            print("输入错误，如果要退出 请输入（退出）"):
```            
