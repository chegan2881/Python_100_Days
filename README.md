# Python_100_Days
======

```Python
Print ('Hello world') //Python

```
## Day 1

```Python
Print ('Hello World!') #引号中是字符串

#input问句和回答换行，问句后加上\n
input("what is name of your pet?\n")

#在print函数中，显示打印内容某一位的字母，从0开始计算。
print("Hello"[0])

```
## Day 2

### Data Types
```Python
#在print函数中，显示打印内容某一位的字母，从0开始计算。
print("Hello"[0])


#type函数，检测变量的属性。
#变量包括String, Integer, Float, Boolean
#String，字符串
#Integer，整数
#Float，浮点数，相当于小数
#Boolean，布尔值，只有Ture和False。

Pet_name = len(input("What's your pet's name?\n"))
print(type(Pet_name))
#连接符不能连接string和integer
String_Pet_name = str(Pet_name)
print(type(String_Pet_name))
print("Your pet name has " + String_Pet_name + " characters.")

#作业1
# 🚨 Don't change the code below 👇
two_digit_number = input("Type a two digit number: ")
# 🚨 Don't change the code above 👆

####################################
#Write your code below this line 👇

X = two_digit_number[0]
Y = two_digit_number[1]
print(type(X))
print(type(Y))

IntX= int(X)
IntY = int(Y)

print(type(IntX))
print(type(IntY))

print(IntX+IntY)

```

### Math Operation PEMDAS
加法 +<br>
减法 -<br>
乘法 *<br>
除法 /，用完除法后出来的都是Float<br>
指数运算 **<br>
四舍五入用round


```Python

#作业2
# 🚨 Don't change the code below 👇
height = input("enter your height in m: ")
weight = input("enter your weight in kg: ")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇
# print(type(height))
# print(type(weight))
H = float(height)
W = float(weight)
# print(type(H))
# print(type(W))
BMI =int(W/(H**2))
# print(type(BMI))
print(BMI)
```

