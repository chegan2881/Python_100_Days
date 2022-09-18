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

# range
for number in range (1, 10): #不包括10
  print(number)

for number in range (1, 10, 3): # 1到10（不含）间隔3个数
  print(number)
# 1到100的和
total = 0
for number in range(1, 101):
  total += number
print(total)

# 作业3，求1到100内偶数的和

#Write your code below this row 👇

sum = 0
for n in range(2, 101, 2):
    sum += n
print(sum)

# 第二种方法
total = 0
for n in range(1,101):
    if n % 2 == 0:
        total += n
print(total)

#作业3 FizzBuzz
#Write your code below this row 👇

for n in range (1,101):
    if n % 15 == 0:
        print("FizzBuzz")
    elif n % 3 == 0:
        print("Fizz")
    elif n % 5 == 0:
        print("Buzz")
    else:
        print(n)

# Practice
#Password Generator Project
import random

letters = [
    'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o',
    'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D',
    'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S',
    'T', 'U', 'V', 'W', 'X', 'Y', 'Z'
]
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters = int(input("How many letters would you like in your password?\n"))
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Eazy Level - Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91
import random

# 创建一个空的string
password = ""

# 将n个随机选择的letter加入password
for x in range(1, nr_letters + 1):
    password = password + random.choice(letters)

# 将n个随机选择的symbol加入password
for y in range(1, nr_symbols + 1):
    password = password + random.choice(symbols)

# 将n个随机选择的number加入password
for z in range(1, nr_numbers + 1):
    password = password + random.choice(numbers)

print(f"Your first password is {password}")

#Hard Level - Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P

# 创建空的list
pw_list = []

# # 将n个随机选择的letter加入list
for x in range(1, nr_letters + 1):
    pw_list.append(random.choice(letters))

# # 将n个随机选择的symbol加入list
for y in range(1, nr_symbols + 1):
    pw_list.append(random.choice(symbols))

# # 将n个随机选择的number加入list
for z in range(1, nr_numbers + 1):
    pw_list.append(random.choice(numbers))

# print(pw_list)

# list重新排序
random.shuffle(pw_list)

# print(pw_list)


# 创建空的password2
password2 = ""
for x in pw_list:
    password2 = password2 + x

print(f"Your second  password is {password2}")


```
## Day 6
``` Python
#Day 6
# def定义新的函数，自带的为built-in function

def my_function():
  # Finally do this 
  # Dothis
  # Then do this
  print ("Hello")
  print ("Bye")
  # Calling function 调用函数
my_function()

# Game 1
def turn_around():
    turn_left()
    turn_left()
def turn_right():
    turn_left()
    turn_left()
    turn_left()
    


for step in range(1,7):
    move()
    turn_left()
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()

# while loop
while something_is_ture:
    #Do this
    #Then do this

# Game Hurdle 1，用while loop
def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    move()
    turn_left()
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()

number_of_hurdles = 6
while number_of_hurdles > 0:
    jump()
    number_of_hurdles -= 1
    print(number_of_hurdles)

# Hurdle 2
def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    move()
    turn_left()
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()

# while not相反条件
while not at_goal():
    jump()

# Hurdle 3&4
def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    turn_left()
    while not right_is_clear():
        move()
    turn_right()
    move()
    turn_right()
    while front_is_clear():
        move()
    turn_left()


while not at_goal():
    if front_is_clear():
        move()
    else:
        jump()

# Reeborg's World Maze
def turn_right():
    turn_left()
    turn_left()
    turn_left()

def wall():
    while not at_goal():
        if right_is_clear():
            turn_right()
            move()
        elif front_is_clear():
            move()
        else:
             turn_left()


while not at_goal():
    if front_is_clear():
        move()
    else:
        turn_left()
        wall()

```


## Day 7

```Python
# Hangman Game
#Step 1 

import random 

word_list = ["aardvark", "baboon", "camel"]

#TODO-1 - Randomly choose a word from the word_list and assign it to a variable called chosen_word.
chosen_word = random.choice(word_list)
print(chosen_word)
number_chosen_word = int(len(chosen_word))
print(number_chosen_word)

#TODO-2 - Ask the user to guess a letter and assign their answer to a variable called guess. Make guess lowercase.
guess = input("Guess a letter: ").lower()
print(guess)

#TODO-3 - Check if the letter the user guessed (guess) is one of the letters in the chosen_word.
chosen_word_list = []

for x in range(0, number_chosen_word):
  chosen_word_list.append(chosen_word[x])

print(chosen_word_list)

for y in chosen_word_list:
  if y == guess:
    print("Right")
  else:
    print("Wrong")


# Alternative method
# for loop如果是in list，就是检查list中所有值，如果是in string，就是检查string的每一位
for letter in chosen_word:
  if letter == guess:
    print("Right")
  else:
    print("Wrong")
    
#Step 2

import random

word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#TODO-1: - Create an empty List called display.
#For each letter in the chosen_word, add a "_" to 'display'.
#So if the chosen_word was "apple", display should be ["_", "_", "_", "_", "_"] with 5 "_" representing each letter to guess.

# 让所有猜的字母都转化成小写去和单词中的字母对比
guess = input("Guess a letter: ").lower()

# 创建空的下划线list
underscore = []
# 用for loop将下划线加入，数量是随机单词字母数量n，所以range是(1, n+1)
for number in range(1, int(len(chosen_word)) + 1):
    underscore.append("_")
print(underscore)
# list有n个元素，位置有第0位到第n-1位
# print(len(underscore))

#TODO-2: - Loop through each position in the chosen_word;
#If the letter at that position matches 'guess' then reveal that letter in the display at that position.
#e.g. If the user guessed "p" and the chosen word was "apple", then display should be ["_", "p", "p", "_", "_"].
# for letter in chosen_word:
#     if letter == guess:
#         print("Right")
#     else:
#         print("Wrong")

# 空List，把所选单词的字母都转化成list中的值
chosen_word_list = []

# 将所选单词的字母用for loop逐一加入list，从第0位到第n-1位
for x in range(0, len(chosen_word)):
    chosen_word_list.append(chosen_word[x])
print(chosen_word_list)

# 将所选单词字母组成的list的值，逐一与猜测字母对比，如果在第n位上相同，就把单词上这一位的字母换到下划线list之中。
for n in range(0, len(chosen_word)):
    if chosen_word[n] == guess:
        underscore[n] = chosen_word[n]

#TODO-3: - Print 'display' and you should see the guessed letter in the correct position and every other letter replace with "_".
#Hint - Don't worry about getting the user to guess the next letter. We'll tackle that in step 3.

print(underscore)

#Step 3

import random
word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)
word_length = len(chosen_word)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
for _ in range(word_length):
    display += "_"

#TODO-1: - Use a while loop to let the user guess again. The loop should only stop once the user has guessed all the letters in the chosen_word and 'display' has no more blanks ("_"). Then you can tell the user they've won.

# My Method
while  '_' in display:
  guess = input("Guess a letter: ").lower()
  
  #Check guessed letter
  for position in range(word_length):
      letter = chosen_word[position]
      # print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
      if letter == guess:
          display[position] = letter
  
  print(display)
  
if not '_' in display:
  print("You won!")
  
# Method 2
end_of_game = False

while not end_of_game: # 或者用while end_of_game == False
    guess = input("Guess a letter: ").lower()

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        #print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
        if letter == guess:
            display[position] = letter

    print(display)

    #Check if there are no more "_" left in 'display'. Then all letters have been guessed.
    if "_" not in display:
        end_of_game = True
        print("You win.")

#Step 4

import random

stages = [
    '''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========''', '''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
      |
      |
      |
=========
''', '''
  +---+
  |   |
      |
      |
      |
      |
=========
'''
]

end_of_game = False
word_list = ["ardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)
word_length = len(chosen_word)

#TODO-1: - Create a variable called 'lives' to keep track of the number of lives left.
#Set 'lives' to equal 6.

lives = 6

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
for _ in range(word_length):
    display += "_"
print(display)

while not end_of_game:
    guess = input("Guess a letter: ").lower()

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        # print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
        if letter == guess:
            display[position] = letter
            # print(f"Your live is {lives}")

    #TODO-2: - If guess is not a letter in the chosen_word,
    #Then reduce 'lives' by 1.
    #If lives goes down to 0 then the game should stop and it should print "You lose."
    if guess not in display:
        lives -= 1
        # print(f"Your live is {lives}")

        if lives == 0:
            end_of_game = True
            print("You lose.")
    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print("You win.")

    #TODO-3: - print the ASCII art from 'stages' that corresponds to the current number of 'lives' the user has remaining.
    print(stages[lives])

#Step 5 My Method

import random
import hangman_art
import hangman_words
#TODO-1: - Update the word list to use the 'word_list' from hangman_words.py
#Delete this line: word_list = ["ardvark", "baboon", "camel"]
chosen_word = random.choice(hangman_words.word_list)
word_length = len(chosen_word)

end_of_game = False
lives = 6

#TODO-3: - Import the logo from hangman_art.py and print it at the start of the game.
print(hangman_art.logo)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
entered = []
for _ in range(word_length):
    display += "_"

while not end_of_game:
    guess = input("Guess a letter: ").lower()
    
    # print(entered)
    #TODO-4: - If the user has entered a letter they've already guessed, print the letter and let them know.

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        # print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
        if letter in entered:
            print(f"Letter {guess} has been entered.")
        elif letter == guess:
            display[position] = letter
            entered.append(guess)

    #Check if user is wrong.
    if guess not in chosen_word:
        #TODO-5: - If the letter is not in the chosen_word, print out the letter and let them know it's not in the word.
        lives -= 1
        print(f"You guessed {guess}, that's not in the word. You lose a lift.")
        if lives == 0:
            end_of_game = True
            print(f"You lose.\nThe word is {chosen_word}.")

    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print("You win.")

    #TODO-2: - Import the stages from hangman_art.py and make this error go away.
    print(hangman_art.stages[lives])

#Step 5 Angela's Method

import random
from replit import clear

#TODO-1: - Update the word list to use the 'word_list' from hangman_words.py
#Delete this line: word_list = ["ardvark", "baboon", "camel"]
from hangman_words import word_list

chosen_word = random.choice(word_list)
word_length = len(chosen_word)

end_of_game = False
lives = 6

#TODO-3: - Import the logo from hangman_art.py and print it at the start of the game.
from hangman_art import logo
print(logo)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
for _ in range(word_length):
    display += "_"

while not end_of_game:
    guess = input("Guess a letter: ").lower()
    clear()

    #TODO-4: - If the user has entered a letter they've already guessed, print the letter and let them know.
    if guess in display:
        print(f"You've already guessed {guess}")

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        #print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
        if letter == guess:
            display[position] = letter

    #Check if user is wrong.
    if guess not in chosen_word:
        #TODO-5: - If the letter is not in the chosen_word, print out the letter and let them know it's not in the word.
        print(f"You guessed {guess}, that's not in the word. You lose a life.")
        
        lives -= 1
        if lives == 0:
            end_of_game = True
            print("You lose.")

    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print("You win.")

    #TODO-2: - Import the stages from hangman_art.py and make this error go away.
    from hangman_art import stages
    print(stages[lives])

# hangman_art
stages = ['''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========''', '''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
      |
      |
      |
=========
''', '''
  +---+
  |   |
      |
      |
      |
      |
=========
''']

logo = ''' 
 _                                             
| |                                            
| |__   __ _ _ __   __ _ _ __ ___   __ _ _ __  
| '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \ 
| | | | (_| | | | | (_| | | | | | | (_| | | | |
|_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_|
                    __/ |                      
                   |___/    '''
                                                                 
                                                                    
								    
								    

```
## Day 8

```Python
# start
# Review: 
# Create a function called greet(). 
# Write 3 print statements inside the function.
# Call the greet() function and run your code.

def great():
  print("A")
  print("B")
  print("C")

great()

def greet_with_name(name):
  print(f"Hello {name}.")
  print(f"How are you, {name}?")

greet_with_name("Xian")
# def my_function(something)
# something = 123
# something是parameter(the name of the data that's being passed in)，函数定义中的参数
# 123是argument(actual value of the data)，函数调用时的实际参数

# function with more than 1 input
def greet_with(name, location): 
    print(f"Hello {name}.")
    print(f"What is it like in {location}?")

greet_with("Xian", "Nowhere")# positional argument
greet_with(location = "Nowhere", name = "Xian" ) # Keyword Argument
# greet_with(input("What's your name?"), "Nowhere")


# paint
#Write your code below this line 👇

def paint_calc(height, width, cover):
  cans = round((int(height) * int(width) / cover)+0.5)
  print(cans)


#Write your code above this line 👆
# Define a function called paint_calc() so that the code below works.   

# 🚨 Don't change the code below 👇
test_h = int(input("Height of wall: "))
test_w = int(input("Width of wall: "))
coverage = 5
paint_calc(height=test_h, width=test_w, cover=coverage)

# prime number
#Write your code below this line 👇
def prime_checker(number):
    is_prime = True

    for x in range(2, number):
        if number % x == 0:
            is_prime = False
    if is_prime:
        print("It's a prime number.")
    else:
        print("It's not a prime number.")



#Write your code above this line 👆
    
#Do NOT change any of the code below👇
n = int(input("Check this number: "))
prime_checker(number=n)

# Caesar Cipher Part 1

alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
# print(alphabet.index("z")) 查找某个值在List中的index

direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
text = input("Type your message:\n").lower()
shift = int(input("Type the shift number:\n"))

#TODO-1: Create a function called 'encrypt' that takes the 'text' and 'shift' as inputs.

    #TODO-2: Inside the 'encrypt' function, shift each letter of the 'text' forwards in the alphabet by the shift amount and print the encrypted text.  
    #e.g. 
    #plain_text = "hello"
    #shift = 5
    #cipher_text = "mjqqt"
    #print output: "The encoded text is mjqqt"

    ##HINT: How do you get the index of an item in a list:
    #https://stackoverflow.com/questions/176918/finding-the-index-of-an-item-in-a-list

    ##🐛Bug alert: What happens if you try to encode the word 'civilization'?🐛

#TODO-3: Call the encrypt function and pass in the user inputs. You should be able to test the code and encrypt a message. 

# My method
def encrypt(text, shift):
  cipher_text = ""
  for letter in text:
    letter_index = alphabet.index(letter)
    real_shift = shift % 26    
    alt_number = letter_index+real_shift
    if alt_number > 25:
      alt_number -= 26
    alt_letter = alphabet[alt_number]
    cipher_text += alt_letter
  print(f"The encoded text is {cipher_text}")
  #Join all the elements in the list and turn it into a String.
  # print(f"{''.join(cipher_text)}")
    
encrypt(text, shift)  

# Caesar cipher step 2
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
text = input("Type your message:\n").lower()
shift = int(input("Type the shift number:\n"))

def encrypt(plain_text, shift_amount):
  cipher_text = ""
  for letter in plain_text:
    position = alphabet.index(letter)
    new_position = position + shift_amount
    cipher_text += alphabet[new_position]
  print(f"The encoded text is {cipher_text}")

#TODO-1: Create a different function called 'decrypt' that takes the 'text' and 'shift' as inputs.
def decrypt(cipher_text, shift_amount):
  #TODO-2: Inside the 'decrypt' function, shift each letter of the 'text' *backwards* in the alphabet by the shift amount and print the decrypted text.  
  #e.g. 
  #cipher_text = "mjqqt"
  #shift = 5
  #plain_text = "hello"
  #print output: "The decoded text is hello"
  plain_text = ""
  for letter in cipher_text:
    position = alphabet.index(letter)
    new_position = position - shift_amount
    plain_text += alphabet[new_position]
  print(f"The decoded text is {plain_text}")


#TODO-3: Check if the user wanted to encrypt or decrypt the message by checking the 'direction' variable. Then call the correct function based on that 'drection' variable. You should be able to test the code to encrypt *AND* decrypt a message.
if direction == "encode":
  encrypt(plain_text=text, shift_amount=shift)
elif direction == "decode":
  decrypt(cipher_text=text, shift_amount=shift)


# Caeser cipher Step 3
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
text = input("Type your message:\n").lower()
shift = int(input("Type the shift number:\n"))

#TODO-1: Combine the encrypt() and decrypt() functions into a single function called caesar(). 
def caesar(plain_text, shift_amount, direction_choice):
  # if direction == "decode":
  #   shift_amount *= -1
  #   print(shift_amount)
  alt_text=""
  for letter in plain_text:
    position = alphabet.index(letter) # 查找输入文本中字母的位置
    real_shift = shift_amount % 26    # 变化输入的转换值，除以26得出余数
    if direction_choice == "encode": #如果是encode，加上真正的转换值
      new_position = position+real_shift 
      if new_position > 25: # 检查是否大于25，大于则减去26
        new_position -= 26   
       
    if direction_choice == "decode":
      new_position = position-real_shift
      if new_position < 0:
        new_position += 26
    alt_text += alphabet[new_position]
  print(f"The {direction_choice}d text is {alt_text}.")    


    #TODO-2: Call the caesar() function, passing over the 'text', 'shift' and 'direction' values.

caesar(plain_text=text, shift_amount=shift, direction_choice=direction)

# Caesar Cipher Final
alphabet = [
    'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o',
    'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'
]

from art import logo
# from replit import clear

def caesar(start_text, shift_amount, cipher_direction):
    end_text = ""
    if cipher_direction == "decode":
        shift_amount *= -1
    for char in start_text:
        if char not in alphabet:
            end_char = char
            #TODO-3: What happens if the user enters a number/symbol/space?
            #Can you fix the code to keep the number/symbol/space when the text is encoded/decoded?
            #e.g. start_text = "meet me at 3"
            #end_text = "•••• •• •• 3"
        if char in alphabet:
            position = alphabet.index(char)
            new_position = position + shift_amount
            if new_position > 25:
                new_position -= 26
            elif new_position < 0:
                new_position += 26
            end_char = alphabet[new_position]
        end_text += end_char

    print(f"Here's the {cipher_direction}d result: {end_text}.")

print(logo) 
game = True

while game:
#TODO-1: Import and print the logo from art.py when the program starts.
 

#TODO-4: Can you figure out a way to ask the user if they want to restart the cipher program?
#e.g. Type 'yes' if you want to go again. Otherwise type 'no'.
#If they type 'yes' then ask them for the direction/text/shift again and call the caesar() function again?
#Hint: Try creating a while loop that continues to execute the program if the user types 'yes'.



    direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
    text = input("Type your message:\n").lower()
    shift = int(input("Type the shift number:\n"))
    real_shift = shift % 26  # 变化输入的转换值，除以26的余数为真正的转换值

#TODO-2: What if the user enters a shift that is greater than the number of letters in the alphabet?
#Try running the program and entering a shift number of 45.
#Add some code so that the program continues to work even if the user enters a shift number greater than 26.
#Hint: Think about how you can use the modulus (%).


    caesar(start_text=text, shift_amount=real_shift, cipher_direction=direction)
    restart = input("Type 'yes' if you want to go again. Otherwise type 'no'.\n").lower()
    if restart == "no":
        game = False

    # clear()
    
print("Goodbye")

```


