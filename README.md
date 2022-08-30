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

# Comparison Operator
# > greater than
# < less than 
# >= greater than or equal to
# <= less than or equal to
# == equal to
# != not equal to

#作业1
# 🚨 Don't change the code below 👇
number = int(input("Which number do you want to check? "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

remainder = number % 2
if remainder == 0:
    print("This is an even number.")
else:
    print("This is an odd number.")

# 作业2
# 🚨 Don't change the code below 👇
height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

bmi = round(weight/(height**2))
# print(bmi)

if bmi <= 18.5:
    print(f"Your BMI is {bmi}, you are underweight")
elif 18.5 < bmi <= 25:
    print(f"Your BMI is {bmi}, you have a normal weight.")
elif 25 < bmi <= 30:
    print(f"Your BMI is {bmi}, you are slightly overweight.")
elif 30 < bmi <= 35:
    print(f"Your BMI is {bmi}, your are obese.")
else:
    print(f"Your BMI is {bmi}, your are clinically obese.")

# 作业3
# 🚨 Don't change the code below 👇
year = int(input("Which year do you want to check? "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

if year % 4 ==0:
    if year % 100 == 0:
        if year % 400 == 0:
            print ("Leap year.")
        else:
            print("Not leap year.")
    else:
        print("Leap year.")
else:
    print("Not leap year.")

# 作业4，Pizza order
# 🚨 Don't change the code below 👇
print("Welcome to Python Pizza Deliveries!")
size = input("What size pizza do you want? S, M, or L ")
add_pepperoni = input("Do you want pepperoni? Y or N ")
extra_cheese = input("Do you want extra cheese? Y or N ")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇
bill = 0

if size == "S":
    bill += 15
    if add_pepperoni == "Y":
        bill += 2
elif size == "M":
    bill += 20
    if add_pepperoni == "Y":
        bill += 3
else:
    bill += 25
    if add_pepperoni == "Y":
        bill += 3
if extra_cheese == "Y":
    bill += 1

print(f"Your final bill is: ${bill}.")

# 作业5，love score
# 🚨 Don't change the code below 👇
print("Welcome to the Love Calculator!")
name1 = input("What is your name? \n")
name2 = input("What is their name? \n")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

lower_name1 = name1.lower();
lower_name2 = name2.lower();

# print(lower_name1);
# print(lower_name2);

x = lower_name1.count("t") + lower_name1.count("r") + lower_name1.count("u") + lower_name1.count("e") + lower_name2.count("t") + lower_name2.count("r") + lower_name2.count("u") + lower_name2.count("e")
y = lower_name1.count("l") + lower_name1.count("o") + lower_name1.count("v") + lower_name1.count("e") + lower_name2.count("l") + lower_name2.count("o") + lower_name2.count("v") + lower_name2.count("e")

# print(x)
# print(y)

strX = str(x)
strY = str(y)

# print(type(strX))
# print(type(strY))

combine = strX + strY
score = int(combine)
if (score < 10) or (score > 90):
    print(f"Your score is {score}, you go together like coke and mentos.")
elif 40 < score < 50:
    print (f"Your score is {score}, you are alright together.")
else:
    print(f"Your score is {score}.")



```


