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



#四舍五入用round
print(round(8/3))
#会显示3
print(round(8/3,2))
#会显示2.67
print(8//3)
# 会直接显示2，是整数

# 持续运算
result = 4 / 2
result /= 2
print(result)

score = 0
score += 1  #等同于score = score + 1
score += 2
score -= 4
print(score)

#f-string
score = 0
height = 1.8
isWinning = True
print(f"Your score is {score}, your height is {1.8} meters, you are winning is {isWinning}.")

#作业3
# 🚨 Don't change the code below 👇
age = input("What is your current age?")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

yearleft = 90 - int(age)
# print(yearleft)
monthleft = yearleft*12
weekleft = yearleft*52
dayleft = yearleft*365

print(f"You have {dayleft} days, {weekleft} weeks, and {monthleft} months left.")

#综合练习
#If the bill was $150.00, split between 5 people, with 12% tip. 

#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60

#Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.💪

#Write your code below this line 👇

print("Welcome to the tip calculator.")
bill = float(input("What was the total bill?\n"))
tippercentage = float(input("What percentage tip would you like to give? 10, 12, or 15?\n"))
numpeople = float(input("How many people to split the bill?\n"))

print(bill)
print(tippercentage)
print(numpeople)

#一种将整除数字强制保持小数后几位为0的办法。
tip = (bill*(1+tippercentage/100)/numpeople)
finaltip = "{:.2f}".format(tip)
print(f"Each one should pay ${finaltip}.")

```
## Day 3
if和else<br>
条件。<br>
```Python
print("Welcome to the rollercoaster!")
height = int(input("What is your height in cm? \n"))
if height>= 120:
  print("You can ride the rollercoaster!")
else:
  print("Sorry, you have to grow taller before you can ride.")
  
  
```


