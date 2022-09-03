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

# Treasure Island
print('''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.") 

#https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Treasure%20Island%20Conditional.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1oDe4ehjWZipYRsVfeAx2HyB7LCQ8_Fvi%26export%3Ddownload

#Write your code below this line 👇

direction = input("You go left or right? L, or R\n").lower()


if direction == "L" or "l":
  island = input("Swim to island or wait for a boat? Swim, or wait.\n").lower()
  if island == "wait" or "Wait":
    door = input("Which door you are going to open? Red, yellow, or blue?\n").lower()
    if door ==  "red":
      print("You were burned by fire. \nGame Over.")
    elif door == "yellow":
      print("You win!")
    elif door == "blue":
      print("You were eaten by beasts. \nGame Over.")
    else:
      print("Game Over.")
  else:
    print("You were attached by a trout. \n Game Over.")

else:
  print("You falled into a hole.\nGame over")


```

## Day4
### 随机


```Python
# 插入其它module里面的值
import my_module
print(my_module.pi)

#导入某块“随机”
import random

#一个随机整数，1到10（含）
random_integer = random.randint(1,10)
print(random_integer)

#一个随机浮点数(0,1) 0.0000到0.99999
random_float = random.random()
print(random_float)



# 作业1
#Remember to use the random module
#Hint: Remember to import the random module here at the top of the file. 🎲
import random	 
# 🚨 Don't change the code below 👇
test_seed = int(input("Create a seed number: "))
random.seed(test_seed)
 # 🚨 Don't change the code above 👆 It's only for testing your code.
	 
#Write the rest of your code below this line 👇

number = random.randint(0,1)
# print(number)

if number == 1:
    print("Heads")
elif number == 0:
    print("Tails")
    
```
### List
```Python
# 储存的list会保存数据顺序
states_of_america = ["Delaware", "Pennsylvania", "New Jersey", "Georgia", "Connecticut", "Massachusetts", "Maryland", "South Carolina", "New Hampshire", "Virginia", "New York", "North Carolina", "Rhode Island", "Vermont", "Kentucky", "Tennessee", "Ohio", "Louisiana", "Indiana", "Mississippi", "Illinois", "Alabama", "Maine", "Missouri", "Arkansas", "Michigan", "Florida", "Texas", "Iowa", "Wisconsin", "California", "Minnesota", "Oregon", "Kansas", "West Virginia", "Nevada", "Nebraska", "Colorado", "North Dakota", "South Dakota", "Montana", "Washington", "Idaho", "Wyoming", "Utah", "Oklahoma", "New Mexico", "Arizona", "Alaska", "Hawaii"]

# print(states_of_america)
# 打印某一位上的值
print(states_of_america[12])
# 方括号输入负数，倒着数
print(states_of_america[-12])

# 可以按照顺序更改序列中的某个值
states_of_america[2] = "NJ"
print(states_of_america)

# 在序列后面增加
states_of_america.append("Shitland")

print(states_of_america)

# 在list后面增加list
states_of_america.extend(["aaa", "bbb", "ccc"])

print(states_of_america)

# 作业2

import random

# 🚨 Don't change the code below 👇
test_seed = int(input("Create a seed number: "))
random.seed(test_seed)

# Split string method
names_string = input("Give me everybody's names, separated by a comma. ")
names = names_string.split(", ")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

# to get total number of item in the list

number_of_item = len(names)
# print(number_of_item)
random_choice = random.randint(0, number_of_item - 1)
person_to_pay = names[random_choice]
print(person_to_pay + " is going to buy the meal today!")

# 用random.choice
# person = random.choice(names)
# # print(person)

# print(f"{person} is going to buy the meal today!")

# 嵌套列表nested list
# dirty_dozen = [
#     "Strawberries", "Spinach", "Kale", "Nectarines", "Apples", "Grapes",
#     "Peaches", "Cherries", "Pears", "Tomatoes", "Celery", "Potatoes"
# ]

fruits = ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"]
vege = [
    "Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"]
dirty_dozen = [fruits, vege]
print(dirty_dozen)
# print嵌套列表总第几个列表的第几个值
# print嵌套列表中第1个列表的第2个值
print(dirty_dozen[0][1])

# 作业3
# 🚨 Don't change the code below 👇
row1 = ["⬜️","️⬜️","️⬜️"]
row2 = ["⬜️","⬜️","️⬜️"]
row3 = ["⬜️️","⬜️️","⬜️️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")
# 🚨 Don't change the code above 👆

#Write your code below this row 👇

x = position[0]
y = position[1]

# print(type(x))
# print(type(y))

x_int = int(x)
y_int = int(y)

# print(type(x_int))
# print(type(y_int))


map[y_int-1][x_int-1] = 'X'



#Write your code above this row 👆

# 🚨 Don't change the code below 👇
print(f"{row1}\n{row2}\n{row3}")


# Game:
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇

Human_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))

if Human_choice == 0:
  print(rock)
elif Human_choice == 1:
  print(paper)
elif Human_choice == 2:
  print(scissors)
else:
  print("You typed an invalid number, you lose!")

import random

game = [rock, paper, scissors]
computer_choice = random.randint(0,2)

# print(computer_choice)
print("Computer chose:" + game[computer_choice])

if (Human_choice == 0 and computer_choice == 2) or (Human_choice == 1 and computer_choice == 0) or (Human_choice == 2 and computer_choice == 1):
  print("You win!")
elif (Human_choice == 2 and computer_choice == 0) or (Human_choice == 1 and computer_choice == 2) or (Human_choice == 0 and computer_choice == 1):
  print("You lose.")
elif Human_choice == computer_choice:
  print("It's a draw.")


```

## Day 5

```Python
# loop 多次执行同一段代码
# for loop 
fruits = ["aaa", "bbb", "ccc"]
for fruit in fruits:
 # 注意缩进，缩进后是在loop中 
  print(fruit)
  print(fruit + " Pie")
#在缩进外，只print一次
print (fruits)

# 练习 1

# 🚨 Don't change the code below 👇
student_heights = input("Input a list of student heights ").split()
for n in range(0, len(student_heights)):
  student_heights[n] = int(student_heights[n])
# 🚨 Don't change the code above 👆


#Write your code below this row 👇
sum = 0
for height in student_heights:
  sum += height
print(sum)

number_of_student = 0
for student in student_heights:
  number_of_student += 1
print(number_of_student)

Mean = sum/number_of_student
print(Mean)

# mean = sum / len(student_heights)
# # 整除情况下保留两位小数
# finalmean = "{:.2f}".format(mean)
# print(finalmean)


# 作业2 Highest score
# 🚨 Don't change the code below 👇
student_scores = input("Input a list of student scores ").split()
for n in range(0, len(student_scores)):
  student_scores[n] = int(student_scores[n])
print(student_scores)
# 🚨 Don't change the code above 👆

#Write your code below this row 👇

highest_score = 0

for score in student_scores:
    if score > highest_score:
        highest_score = score
# print(highest_score)

HS = str(highest_score)
print("The highest score in the class is: " + HS)




```

