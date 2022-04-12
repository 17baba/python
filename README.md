# python
学习笔记
2022-4-12第一课

# 个人：王博
# 学习专用
# 学习时间：2022/4/12 0012 下午 9:39

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



#第二章
print(chr(0b100111001011000))  #chr是二进制01前面需要添加0b
print(ord('乘'))  #ord是十进制

import keyword
print(keyword.kwlist)  #查看保留字


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


#常用的数据类型有
#1整数类型-->int-->98
#2浮点数类型-->float-->3.14159
#3布尔类型-->bool-->True,False
#4字符串类型-->str-->'人生苦短，我用python'

#p12已看完
