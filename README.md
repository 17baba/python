# 个人：王博
# 学习专用
# 学习时间：2022/4/12 0012 下午 9:39
#第一章
#python的自诉
#   https://user-images.githubusercontent.com/103509367/163393866-e0c17930-753a-4e75-9f8d-11f33a3dbce2.png


#print（）函数
#可以输出数字
print(520)
print(98.5)

#可以输出字符串
print('helloworld')
print("helloworld")    #单引号和双引号都可以输出引号里的内容

#含有运算符的表达式
print(3+1)


#将数据输出文件中  ,注意点:1.所指定的盘符必须存在，2：使用file=fp
fp=open('D:/text.txt','a+')#a+的含义是如果不存在就创建，存在就在文件内容的后面继续追加
print('helloworld',file=fp)
fp.close()


#不进行换行输出（输出内容在一行当中）
print('hello','world','python')

#转义字符

#   https://user-images.githubusercontent.com/103509367/163395433-7ff428bb-d2c1-41d2-a848-e79e4797571b.png
print('hello\nworld') #\   加转义功能的首字母   n-->newline的首字母表示换行
print('hello\tworld')  #\  加t表示水平制表符  简单理解就是空4个字符的意思
print('helloooo\tworld')
print('hello\rworld') #world将hello进行了覆盖
print('hello\bworld') #\b是退一个格，将o退没了


print('http:\\\\www.baidu.com')
print('老师说：\'大家好\'')

#原字符，不希望字符串中的转义字符起作用，就使用原字符，就是在字符串之前加上r或R
print(r'hello\nworld')
#注意事项，最后一个字符不能是反斜线
#print(r'hello\nworld\')
print(r'hello\nworld\\')

#总结
#  https://user-images.githubusercontent.com/103509367/163395622-d28c5657-f7c4-4622-83b6-fad4360ec19e.png

#第二章

#   https://user-images.githubusercontent.com/103509367/163395885-3b39c320-2e6a-4784-9a2b-cf9c8973db2f.png


print(chr(0b100111001011000))  #chr是二进制01前面需要添加0b
print(ord('乘'))  #ord是十进制

import keyword
print(keyword.kwlist)  #查看保留字


#  https://user-images.githubusercontent.com/103509367/163395885-3b39c320-2e6a-4784-9a2b-cf9c8973db2f.png

#变量有三部分组成：标识，类型，值
name='马丽亚'
print(name)
print('标识',id(name))
print('类型',type(name))
print('值',name)


#变量可以多次赋值，多次赋值后会指向新的空间
name='马丽亚'
name='十七爸爸'
print(name)



#2022-4-13第二天学习笔记
#数据类型
# https://user-images.githubusercontent.com/103509367/163396664-3f492313-96a1-494e-924f-f4498b4913e1.png
#常用的数据类型有
#1整数类型-->int-->98
#2浮点数类型-->float-->3.14159
#3布尔类型-->bool-->True,False
#4字符串类型-->str-->'人生苦短，我用python'

#整数类型
#https://user-images.githubusercontent.com/103509367/163396878-dc6f7e3a-3e5e-4542-881e-9284f4ecd811.png
#可以表示，正数，负数，0
n1=90
n2=-76
n3=0
print(n1,type(n1))
print(n2,type(n2))
print(n3,type(n3))
#整数可以表示为二进制，十进制，八进制，十六进制
print('十进制',118)
print('二进制',0b10101111)  #二进制以0b开头
print('八进制',0o176)  #八进制以0o开头
print('十六进制',0x1EAF) #十六进制以0x开头


#浮点类型
#浮点数存储有一定不精确性，使用浮点数进行计算时，可能会出现小数位数不确定的情况
a=3.14159
print(a,type(a))
n1=1.1
n2=2.2
n3=2.1
print(n1+n2)
print(n1+n3)

from decimal import Decimal
print(Decimal('1.1')+Decimal('2.2'))


f1=True
f2=False
print(f1,type(f1))
print(f2,type(f2))

#布尔值可以转成整数计算
print(f1+1) #2   1+1的结果为2  True表示1
print(f1+2) #1   0+1的结果位1，False表示0

#数据类型
#字符串类型字符串又被称为不可变的字符序列
#可以使用单引号”双引号””三引号”.或””””"来定义
#单引号和双引号定义的字符串必须在一行
#三引号定义的字符串可以分布在连续的多行
str1='人生苦短，我用python'
str2="人生苦短，我用python"
str3="""人生苦短，
我用python"""
str4='''人生苦短，
我用python'''
print(str1,type(str1))
print(str2,type(str2))
print(str3,type(str3))
print(str4,type(str4))


#数据转换类型
#  https://user-images.githubusercontent.com/103509367/163397250-48a434db-1999-4d18-959b-1f54fce5956c.png
name='张三'
age=20

print(type(name),type(age))   #说明name与age的数据类型不相同
#print('我叫‘+name’今年,‘+age+’岁‘）   #当将str类型与int类型进行连接时，报错，解决方案，类型转换
print('我叫'+name+'今年,'+str(age)+'岁')   #将int类型通过str()函数转成了str类型

print('-----------------str()将其它类型转成str类型-------------')
a=10
b=198.8
c=False
print(type(a),type(b),type(c))
print(str(a),str(b),str(c),type(str(a)),type(str(b)),type(str(c)))

print('---------int()将其它的类型转int类型----------')
s1='128'
f1=98.7
s2='76.77'
ff=True
s3='hello'
print(type(s1),type(f1),type(s2),type(ff),type(s3))
print(int(s1),type(int(s1)))  #将str转成int类型，字符串为 数字串
print(int(s1),type(int(s1)))  #将float转成int类型，截取整数部分，舍掉小数部分
#print(int(s2),type(int(s2)))  #将str转成int类型，报错，因为字符串为小数串
print(int(ff),type(int(ff)))
#print(int(sqlite3),type(int(s3)))   #将str转成int类型时，字符串必须为数字串（整数），非数字串是不允许转换

print('----------float()函数，将其它数据类型--------------')

s1='128.98'
s2='76'
ff=True
s3='hello'
i=98
print(type(s1),type(s2),type(ff),type(s3),type(i))
print(float(s1),type(float(s1)))
print(float(s2),type(float(s2)))
print(float(ff),type(float(ff)))
#print(float(s3),type(float(s3)))  #字符串中的数据如果是非数字串，则不允许转换
print(float(i),type(float(i)))


#输出功能（单行注释）
print('hello')
'''嘿嘿，我是多
行注释
哦'''

#总结
#  https://user-images.githubusercontent.com/103509367/163397612-93e9031c-c292-4374-93f1-bdbb7472fd2d.png


#第三章

#输入函数input
#  https://user-images.githubusercontent.com/103509367/163397744-1f68e105-b075-4934-889f-2fd7f7f201d3.png
present=input('大圣想要什么礼物呢？')
print(present,type(present))

#从键盘录入两个整数，计算两个整数的和
a=int(input('请输入一个加数：'))
#a=int(a) #将转换之后的结果存储到a中
b=int(input('请输入另一个加数'))
print(type(a),type(b))
print(a+b)

#运算符

#  https://user-images.githubusercontent.com/103509367/163398099-35528282-712c-49d1-a8c8-4b2e51c0eef4.png

print(1+1)  #加法运算
print(1-1)  #减法运算
print(2*4)  #乘法运算
print(1/2)  #除法运算
print(11/2) #除法运算
print(11//2) #5  整除运算
print(11%2) #取余运算
print(2**2)  #表示的是2的2次方    幂运算
print(2**3)  #表示的是2的3次方    幂运算

print(9//4)  #2
print(-9//-4) #2


print(9//-4)  #3
print(-9//4)  #3    一正一负的整数公式，向下取整

print(9%-4)  #3      公式   余数=被除数-除数*商     9-（4）*（-3）  9-12-->  -3
print(-9%4)  #3                                 -9-4*（-3）  -9+12-->  3

#  https://user-images.githubusercontent.com/103509367/163324110-89fcd9e9-7a64-4f0e-85d8-df8d1002ec57.png

#赋值运算符，运算顺序从右到左
i=3+4
print(i)
a=b=c=20  #链式赋值
print(a,id(a))
print(b,id(b))
print(c,id(c))
print('------------支持参数赋值----------------')
a=20
a+=30   #相当于a=a+30
print(a)
a-=10   #相当于a=1-10
print(a)
a*=2    #相当于a=a*2
print(a)   #int
print(type(a))
a/=3
print(a)
print(type(a))   #float
a//=2
print(a)
print(type(a))
a%=3
print(a)
print('------------解包赋值---------------')
a,b,c,=20,30,40
print(a,b,c)

#a,b=20,30,40    报错，因为左右变量的个数和值的个数不对应
print('--------交换两个变量的值----------')
a,b=10,20
print('交换之前：',a,b)
#交换
a,b=b,a
print('交换之后：',a,b)


#比较运算符，比较运算符的结果为bool类型
#  https://user-images.githubusercontent.com/103509367/163399391-eea79880-40a4-4b9c-8e57-f548ac0fa619.png
a,b=10,20
print('a>b吗',a>b)   #False
print('a<b吗',a<b)   #True
print('a<=b吗',a<=b) #True
print('a>=b吗',a>=b) #False
print('a==b吗',a==b) #False
print('a!=b吗',a!=b) #True

'''一个  =  称为赋值运算符，== 称为比较运算符
  一个变量有三部分组成，标识，类型，值
  == 比较的是值还是标识呢？  比较的是值
 比较对象的标识使用的是  is
'''
a=10
b=10
print(a==b)   #True  说明，a与b的value（值）相等
print(a is b )  #True 说明，a与b的id标识，相等
#以下代码没学过，后面会给大家讲解
lst1=[11,22,33,44]
lst2=[11,22,33,44]
print(lst1==lst2)  #value   -->True
print(lst1 is lst2)  #id   -->False
print(id(lst1))
print(id(lst2))
print(a is not b ) #False  a的id与b的id是不相等的
print(lst1 is not lst2) #True


#布尔运算符
#  https://user-images.githubusercontent.com/103509367/163402911-4952ff31-8c27-45a8-af4e-5dd65c409900.png

a,b=1,2
print('------------and 并且-------------')
print(a==1 and b==2)  #True  True and True-->True
print(a==1 and b<2)   #False True and False-->False
print(a!=1 and b==2)  #False False and True-->False
print(a!=1 and b!=2)  #False False and False-->False

print('-------------or 或者-----------')
print(a==1 or b==2)  #True or True  -->True
print(a==1 or b<2)   #True or True  -->True
print(a!=1 or b==2)  #False or True -->True
print(a!=1 or b!=2)  #False or False -->False

print('---------not 对bool类型操作数取反-----------')
f=True
f2=False
print(not f)
print(not f2)


print('---------------in 与not in-------------------')   #in代表什么什么里  not in代表不在什么什么里
s='helloworld'
print('w' in s)
print('k' in s)
print('w' not in s)  #False
print('k' not in s)  #True


#位运算符
#  https://user-images.githubusercontent.com/103509367/163405805-dbf69cdb-8593-47be-8753-33bcf9b4c20a.png

print(4&8)  #按位与&，同为1时结果为1
print(4|8)  #按位或|，同为0时结果为0
print(4<<1) #向左移动1位（移动一个位置） 相当于乘以2
print(4<<2) #向左移动2位（移动两个位置） 相当于乘以4

print(4>>1) #向右移动1位，相当于除以2
print(4>>2) #向右移动2位，相当于除以4

#运算符的优先级
#  https://user-images.githubusercontent.com/103509367/163407304-a224ce44-1ea9-48ab-b843-b46a0fa6e327.png


#总结
#  https://user-images.githubusercontent.com/103509367/163407153-b729942c-d2a7-4505-a2ca-2da9d9368171.png


# p28  第四章
#顺序结构
'''把大象装冰箱一共分几步'''
print('------------程序开始------------')
print('1.把冰箱门打开')
print('2.把大象放冰箱里')
print('3.把冰箱门关上')
print('----------程序结束------------')

#p29
#测试对象的布尔值
print('----------以下对象的布尔值均为False-------------------')
print(bool(False))     #False
print(bool(0))         #False
print(bool(0.0))       #False
print(bool(None))      #False
print(bool(''))        #False
print(bool(""))        #False
print(bool([]))        #空列表
print(bool(list()))    #空列表
print(bool(()))        #空元组
print(bool(tuple()))   #空元组
print(bool({}))        #空字典
print(bool(dict()))    #空字典
print(bool(set()))     #空集合

print('---------其他对象的布尔值均为True------------')
print(bool(18))
print(bool(True))
print(bool('helloworld'))



#p30
#单分支结构
money=1000  #余额
s=int(input('请输入取款金额'))  #取款金额
#判断余额是否充足
if money>=s:
    money=money-s
    print('取款成功，余额为：',money)


#p31
#双分支结构if...else,二选一执行
'''从键盘录入一个整数，编写程序让计算机判断是奇数还是偶数'''
num=int(input('请输入一个整数'))

#条件判断
if num%2==0:
    print(num,'是偶数')
else:
    print(num,'是奇数')


#p32
'''多分支结构，多选一执行
  从键盘录入一个整数  成绩
  90-100  A
  80-89   B
  70-79   C
  60-69   D
  0-59    E
  小于0或者大于100  为非法数据（不是成绩的有效范围'''
score=int(input('请输入一个成绩：'))
#判断
if score>=90 and score<=100:
    print('A级')
elif score>=80 and score<=89:
    print('B级')
elif score>=70 and score<=79:
    print('C级')
elif score>=60 and score<=69:
    print('D级')
elif score>=0 and score<=59:
    print('E级')
else:
    print('对不起，成绩有误，不在成绩的有效范围')

#第二种简单的写法
if 90<=score<=100:
    print('A级')
elif 80<=score<=89:
    print('B级')
elif 70<=score<=79:
    print('C级')
elif 60<=score<=69:
    print('D级')
elif 0<=score<=59:
    print('E级')
else:
    print('对不起，成绩有误，不在成绩的有效范围')


#p33
'''会员   >=200   8折
         >=100   9折
               不打折
    非会员   >=200  9.5折
               不打折'''
answer=input('您是会员吗？y/n')
money=float(input('请输入您的购物金额：'))
#外层判断是否是会员
if answer=='y':   #会员
    if money>=200:
        print('打8折，付款金额为：',money*0.8)
    elif money>=100:
        print('打9折，付款金额为：',money*0.9)
    else:
        print('不打折，付款金额为：',money)
else:  #非会员
    if money>=200:
        print('打9.5折，付款金额为：',money*0.95)
    else:
        print('不打折，付款金额为：',money)

#p34
#条件表达式
'''从键盘录入两个整数，比较两个整数的大小'''
num_a=int(input('请输入第一个整数'))
num_b=int(input('请输入第二个整数'))
#比较大小
'''if num_a>=num_b:
    print(num_a,'大于等于',num_b)
else:
    print(num_a,'小于',num_b)
'''
print('使用条件表达式进入比较')
print(str(num_a)+'大于等于'+str(num_b)  if num_a>=num_b else str(num_a)+'小于'+str(num_b))

#p35
#pass语句，什么都不做，只是一个占位符，用到需要写语句的地方
answer=input('您是会员吗？y/n')

#判断是否是会员
if answer=='y':
    pass
else:
    pass


#第四章总结   第四章结束
#  https://user-images.githubusercontent.com/103509367/163575358-0064c5ed-c5ee-4d50-9778-ad1b31de8ecc.png
