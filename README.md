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

## Day 9
### Starter of Dictionary
```Python
programming_dictionary = {
  "Bug": "An error in a program that prevents the program from running as expected.", 
  "Function": "A piece of code that you can easily call over and over again.",

}

# Retrieving items from dictionary.
print(programming_dictionary["Bug"])

# adding new items to dictionary
programming_dictionary["Loop"] = "The action of doing something over and over again."
print(programming_dictionary)

# create an empty dictionary
empty_list = []
empty_dictionary = {}

# wipe an existing dictionary
programming_dictionary_A = {}

# edit an item in adictionnary
programming_dictionary["Bug"] = "A moth in your computer"
print(programming_dictionary)

# loop through a dictionary
for thing in programming_dictionary:
  print(thing) # only print key
for thing in programming_dictionary:  
  print(programming_dictionary[thing])
  
```
### Step 1
```Python
student_scores = {
    "Harry": 81,
    "Ron": 78,
    "Hermione": 99,
    "Draco": 74,
    "Neville": 62,
}
# 🚨 Don't change the code above 👆

#TODO-1: Create an empty dictionary called student_grades.
student_grades = {}

#TODO-2: Write your code below to add the grades to student_grades.👇
for student in student_scores:
    if 90 < student_scores[student] <= 100:
        student_grades[student] = "Outstanding"
    elif 80 < student_scores[student] <= 90:
        student_grades[student] = "Exceeds Expectations"
    elif 70 < student_scores[student] <= 80:
        student_grades[student] = "Acceptable"
    elif student_scores[student] <= 70:
        student_grades[student] = "Fail"

# 🚨 Don't change the code below 👇
print(student_grades)

```

### Nesting in Dictionary
```Python
##Python Dictionaries

programming_dictionary = {
  "Bug": "An error in a program that prevents the program from running as expected.", 
  "Function": "A piece of code that you can easily call over and over again.",
}

#Retrieving items from dictionary.
# print(programming_dictionary["Function"])

#Adding new items to dictionary.
programming_dictionary["Loop"] = "The action of doing something over and over again."

#Create an empty dictionary.
empty_dictionary = {}

#Wipe an existing dictionary
# programming_dictionary = {}
# print(programming_dictionary)

#Edit an item in a dictionary
programming_dictionary["Bug"] = "A moth in your computer."
# print(programming_dictionary)

#Loop through a dictionary
# for key in programming_dictionary:
#   print(key)
#   print(programming_dictionary[key])

#######################################

#Nesting 
capitals = {
  "France": "Paris",
  "Germany": "Berlin",
}

#Nesting a List in a Dictionary

travel_log = {
  "France": ["Paris", "Lille", "Dijon"],
  "Germany": ["Berlin", "Hamburg", "Stuttgart"],
}

#Nesting Dictionary in a Dictionary

travel_log = {
  "France": {"cities_visited": ["Paris", "Lille", "Dijon"], "total_visits": 12},
  "Germany": {"cities_visited": ["Berlin", "Hamburg", "Stuttgart"], "total_visits": 5},
}

#Nesting Dictionaries in Lists

travel_log = [
{
  "country": "France", 
  "cities_visited": ["Paris", "Lille", "Dijon"], 
  "total_visits": 12,
},
{
  "country": "Germany",
  "cities_visited": ["Berlin", "Hamburg", "Stuttgart"],
  "total_visits": 5,
},
]

travel_log = [
{
  "country": "France",
  "visits": 12,
  "cities": ["Paris", "Lille", "Dijon"]
},
{
  "country": "Germany",
  "visits": 5,
  "cities": ["Berlin", "Hamburg", "Stuttgart"]
},
]

# exercise
#🚨 Do NOT change the code above

#TODO: Write the function that will allow new countries
#to be added to the travel_log. 👇

def add_new_country(country_visited, time_visited, cities_visited):
  new_country = {}
  new_country["country"] = country_visited
  new_country["visits"] = time_visited
  new_country["cities"] = cities_visited
  travel_log.append(new_country)



#🚨 Do not change the code below
add_new_country("Russia", 2, ["Moscow", "Saint Petersburg"])
print(travel_log)


```

### Blind Auction
```Python
from replit import clear
#HINT: You can call clear() to clear the output in the console.
from art import logo
print(logo)

game = True
auction={}

while game:
    name = input("What's your name? ")
    bid = int(input("What's your bid? $"))
    auction[name]=bid
    game_continue = input("Are there any other bidders? Type 'yes' or 'no'.").lower()
    if game_continue == "no":
        game = False
    else:
      clear()

highest = 0      
for key in auction:
    if auction[key] > highest:
        highest = auction[key]
        name_highest = key

print(f"The winner is {name_highest} with a bid of ${highest}.")
       
# print(auction)

# Angela's methond
from replit import clear
from art import logo
print(logo)

bids = {}
bidding_finished = False

def find_highest_bidder(bidding_record):
  highest_bid = 0
  winner = ""
  # bidding_record = {"Angela": 123, "James": 321}
  for bidder in bidding_record:
    bid_amount = bidding_record[bidder]
    if bid_amount > highest_bid: 
      highest_bid = bid_amount
      winner = bidder
  print(f"The winner is {winner} with a bid of ${highest_bid}")

while not bidding_finished:
  name = input("What is your name?: ")
  price = int(input("What is your bid?: $"))
  bids[name] = price
  should_continue = input("Are there any other bidders? Type 'yes or 'no'.\n")
  if should_continue == "no":
    bidding_finished = True
    find_highest_bidder(bids)
  elif should_continue == "yes":
    clear()
  

"""
FAQ: My console doesn't clear()

This will happen if you’re using an IDE other than replit. 
I’ll cover how to use PyCharm in Day 15. That said, you can write your own clear() function or configure your IDE like so: 

https://www.udemy.com/course/100-days-of-code/learn/lecture/19279420#questions/16084076

"""

```

## Day 10 Function with Outputs

### Start of function with outputs
```Python
# function with Outpus
def format_name(f_name, l_name):
  formated_f=f_name.title()
  formated_l=l_name.title()
  # print(f"{formated_f} {formated_l}")
  return f"{formated_f} {formated_l}"
# formated_string = format_name("xuan", "CHEN")
# print(formated_string)

print(format_name("xuan", "CHEN"))

output = len("Angela") # replace where function was called

# Multiple Return Values


#Functions with Outputs
def format_name(f_name, l_name):
  if f_name == "" or l_name == "":
    return "You didn't provide valid inputs."
  formated_f_name = f_name.title()
  formated_l_name = l_name.title()
  f"Result: {formated_f_name} {formated_l_name}"

#Storing output in a variable
formatted_name = format_name(input("Your first name: "), input("Your last name: "))
print(formatted_name)
#or printing output directly
print(format_name(input("What is your first name? "), input("What is your last name? ")))

#Already used functions with outputs.
length = len(formatted_name)

#Return as an early exit
def format_name(f_name, l_name):
  """Take a first and last name and format it 
  to return the title case version of the name."""
  if f_name == "" or l_name == "":
    return "You didn't provide valid inputs."
  formated_f_name = f_name.title()
  formated_l_name = l_name.title()
  return f"Result: {formated_f_name} {formated_l_name}" # The return tells this is the end of function


```

### Exercise: Days in month
```Python
def is_leap(year):
    #docstring
    """to figure out if the year input is a leap year"""
    if year % 4 == 0:
        if year % 100 == 0:
            if year % 400 == 0:
                return True
            else:
                return False
        else:
            return True
    else:
        return False


def days_in_month(year, month):
  if month >12 or month <1:
      return "Invalid month"
  month_days = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]  
  if is_leap(year) and month == 2:
      return 29
  return month_days[month - 1]


#🚨 Do NOT change any of the code below
year = int(input("Enter a year: "))
month = int(input("Enter a month: "))
days = days_in_month(year, month)
print(days)

```
### Calculator
```Python
# Step 1
# My method
from art import logo
from replit import clear
# Calculator

#add
def add(n1, n2):
  return n1 + n2

#substrate
def sub(n1, n2):
  return n1 - n2

#multiply
def mul(n1, n2):
  return n1 * n2

#devide
def dev(n1, n2):
  return n1 / n2

operations = {
  "+": add,
  "-": sub,
  "*": mul,
  "/": dev,
}

calculate = True
answer = ""

while calculate:
    if answer == "":
        num1 = float(input("What's the 1st number?: "))
    else:
        num1 = answer
    for symbol in operations:
      print(symbol)
    operation_symbol = input("Pick an operation from the line above: ")
    
    num2 = float(input("What's the next number?: "))
      
    calculation_function = operations[operation_symbol] 
    # 让一个新的function等于选定的运算function，然后再在括号里放入需要计算的数值
    answer = calculation_function(num1, num2)
    print(f"{num1} {operation_symbol} {num2} = {answer}")  
    if_continue = input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ")
    if if_continue == "n":
      clear()  
      answer = ""
        
# Angela's method
from replit import clear
from art import logo

def add(n1, n2):
  return n1 + n2

def subtract(n1, n2):
  return n1 - n2

def multiply(n1, n2):
  return n1 * n2

def divide(n1, n2):
  return n1 / n2

operations = {
  "+": add,
  "-": subtract,
  "*": multiply,
  "/": divide
}

def calculator():
  print(logo)

  num1 = float(input("What's the first number?: "))
  for symbol in operations:
    print(symbol)
  should_continue = True
 
  while should_continue:
    operation_symbol = input("Pick an operation: ")
    num2 = float(input("What's the next number?: "))
    calculation_function = operations[operation_symbol]
    answer = calculation_function(num1, num2)
    print(f"{num1} {operation_symbol} {num2} = {answer}")

    if input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ") == 'y':
      num1 = answer
    else:
      should_continue = False
      clear()
      calculator()

calculator()


```

## Day 11

### Black Jack My Method
``` Python
############### Blackjack Project #####################

#Difficulty Normal 😎: Use all Hints below to complete the project.
#Difficulty Hard 🤔: Use only Hints 1, 2, 3 to complete the project.
#Difficulty Extra Hard 😭: Only use Hints 1 & 2 to complete the project.
#Difficulty Expert 🤯: Only use Hint 1 to complete the project.

############### Our Blackjack House Rules #####################

## The deck is unlimited in size.
## There are no jokers.
## The Jack/Queen/King all count as 10.
## The the Ace can count as 11 or 1.
## Use the following list as the deck of cards:
## cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
## The cards in the list have equal probability of being drawn.
## Cards are not removed from the deck as they are drawn.
## The computer is the dealer.

##################### Hints #####################

#Hint 1: Go to this website and try out the Blackjack game:
#   https://games.washingtonpost.com/games/blackjack/
#Then try out the completed Blackjack project here:
#   http://blackjack-final.appbrewery.repl.run

#Hint 2: Read this breakdown of program requirements:
#   http://listmoz.com/view/6h34DJpvJBFVRlZfJvxF
#Then try to create your own flowchart for the program.

#Hint 3: Download and read this flow chart I've created:
#   https://drive.google.com/uc?export=download&id=1rDkiHCrhaf9eX7u7yjM1qwSuyEk-rPnt

#Hint 4: Create a deal_card() function that uses the List below to *return* a random card.
#11 is the Ace.
#cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]

#Hint 5: Deal the user and computer 2 cards each using deal_card() and append().
#user_cards = []
#computer_cards = []

#Hint 6: Create a function called calculate_score() that takes a List of cards as input
#and returns the score.
#Look up the sum() function to help you do this.

#Hint 7: Inside calculate_score() check for a blackjack (a hand with only 2 cards: ace + 10) and return 0 instead of the actual score. 0 will represent a blackjack in our game.

#Hint 8: Inside calculate_score() check for an 11 (ace). If the score is already over 21, remove the 11 and replace it with a 1. You might need to look up append() and remove().

#Hint 9: Call calculate_score(). If the computer or the user has a blackjack (0) or if the user's score is over 21, then the game ends.

#Hint 10: If the game has not ended, ask the user if they want to draw another card. If yes, then use the deal_card() function to add another card to the user_cards List. If no, then the game has ended.

#Hint 11: The score will need to be rechecked with every new card drawn and the checks in Hint 9 need to be repeated until the game ends.

#Hint 12: Once the user is done, it's time to let the computer play. The computer should keep drawing cards as long as it has a score less than 17.

#Hint 13: Create a function called compare() and pass in the user_score and computer_score. If the computer and user both have the same score, then it's a draw. If the computer has a blackjack (0), then the user loses. If the user has a blackjack (0), then the user wins. If the user_score is over 21, then the user loses. If the computer_score is over 21, then the computer loses. If none of the above, then the player with the highest score wins.

#Hint 14: Ask the user if they want to restart the game. If they answer yes, clear the console and start a new game of blackjack and show the logo from art.py.

import random
from art import logo
from replit import clear

card = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
card_score = {}

# Do you want to play a game of Blackjack? Type 'y' or 'n':
# Your cards: [ ], current score:
# Computer's first card:
# Type 'y' to get another card, type 'n' to pass:
# Your final hand: [], final socre:
# Computer's final hand: [], final score:
# Opponent went over. You win.
# You went over. You lose.
# You win
# You lose
# The draw
# Lose, opponent has Blackjack.
# You win! You have Blackjack.

player_card = []
dealer_card = []
player_score = 0
dealer_score = 0


def player_draw():
    global player_score
    player_draw_random = card[random.randint(0, 12)]
    player_card.append(player_draw_random)
    player_score += player_draw_random


def dealer_draw():
    global dealer_score
    dealer_draw_random = card[random.randint(0, 12)]
    dealer_card.append(dealer_draw_random)
    dealer_score += dealer_draw_random
    


def compare():
    print(f"Your final hand: {player_card}, final score: {player_score}.")
    print(
        f"Computer's final hand: {dealer_card}, final score: {dealer_score}.")
    if player_score > 21:
        print("You went over. You lose.")
    elif dealer_score > 21:
        print("Opponent went over. You win.")
    elif player_score > dealer_score:
        print("You win.")
    # elif player_score == 21 and dealer_score == 21:
    #     print("You lose.")
    elif player_score == dealer_score:
        print("The draw.")
    elif player_score < dealer_score:
        print("You lose.")


# player_score = sum(player_card)
# print(player_score)
# dealer_score = sum(dealer_card)
# print(dealer_score)

start = True
one_draw = True

player_start = input(
    "Do you want to play a game of Blackjack? Type 'y' or 'n': ")
if player_start == "n":
    start = False
clear()
while start:
    print(logo)
    player_draw()
    player_draw()
    dealer_draw()
    dealer_draw()
    print(f"Your card: {player_card}, current score: {player_score}.")
    print(f"Computer's first card: {dealer_card[0]}.")
    if player_score == 21:
        print("You win! You have Blackjack.")
    elif dealer_score == 21:
        print("Lose, opponent has Blackjack.")
    else:
        if_one_draw = input("Type 'y' to get another card, type 'n' to pass: ")
        if if_one_draw == "n":
            one_draw = False
            compare()
        else:
          while one_draw:
            player_draw()
            if player_score >= 21 and 11 not in player_card:
                one_draw = False
                # while dealer_score < 17:
                #     dealer_draw()
                compare()
            elif player_score == 21:
                one_draw = False
                compare()
            elif player_score >21 and 11 in player_card:
                player_card.remove(11)
                player_card.append(1)
                player_score -= 10
                print(f"Your card: {player_card}, current score: {player_score}.")
                print(f"Computer's first card: {dealer_card[0]}.")
                if_one_draw = input("Type 'y' to get another card, type 'n' to pass: ")
                if if_one_draw == "n":
                    one_draw = False
                    while dealer_score < 17:
                        dealer_draw()
                    compare()
                else:
                    one_draw = True                
            else:
                print(f"Your card: {player_card}, current score: {player_score}.")
                print(f"Computer's first card: {dealer_card[0]}.")
                if_one_draw = input("Type 'y' to get another card, type 'n' to pass: ")
                if if_one_draw == "n":
                    one_draw = False
                    while dealer_score < 17:
                        dealer_draw()
                    compare()
                else:
                    one_draw = True

    restart = input(
        "Do you want to play a game of Blackjack? Type 'y' or 'n': ")
    if restart == "n":
        start = False
    clear()
    if restart == "y":
        player_card = []
        dealer_card = []
        player_score = 0
        dealer_score = 0        


```

### Black Jack Angela

```Python
############### Blackjack Project #####################

#Difficulty Normal 😎: Use all Hints below to complete the project.
#Difficulty Hard 🤔: Use only Hints 1, 2, 3 to complete the project.
#Difficulty Extra Hard 😭: Only use Hints 1 & 2 to complete the project.
#Difficulty Expert 🤯: Only use Hint 1 to complete the project.

############### Our Blackjack House Rules #####################

## The deck is unlimited in size. 
## There are no jokers. 
## The Jack/Queen/King all count as 10.
## The the Ace can count as 11 or 1.
## Use the following list as the deck of cards:
## cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
## The cards in the list have equal probability of being drawn.
## Cards are not removed from the deck as they are drawn.

##################### Hints #####################

#Hint 1: Go to this website and try out the Blackjack game: 
#   https://games.washingtonpost.com/games/blackjack/
#Then try out the completed Blackjack project here: 
#   http://blackjack-final.appbrewery.repl.run

#Hint 2: Read this breakdown of program requirements: 
#   http://listmoz.com/view/6h34DJpvJBFVRlZfJvxF
#Then try to create your own flowchart for the program.

#Hint 3: Download and read this flow chart I've created: 
#   https://drive.google.com/uc?export=download&id=1rDkiHCrhaf9eX7u7yjM1qwSuyEk-rPnt

#Hint 4: Create a deal_card() function that uses the List below to *return* a random card.
#11 is the Ace.
import random
from replit import clear
from art import logo

def deal_card():
  """Returns a random card from the deck."""
  cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
  card = random.choice(cards)
  return card

#Hint 6: Create a function called calculate_score() that takes a List of cards as input 
#and returns the score. 
#Look up the sum() function to help you do this.
def calculate_score(cards):
  """Take a list of cards and return the score calculated from the cards"""

  #Hint 7: Inside calculate_score() check for a blackjack (a hand with only 2 cards: ace + 10) and return 0 instead of the actual score. 0 will represent a blackjack in our game.
  if sum(cards) == 21 and len(cards) == 2:
    return 0
  #Hint 8: Inside calculate_score() check for an 11 (ace). If the score is already over 21, remove the 11 and replace it with a 1. You might need to look up append() and remove().
  if 11 in cards and sum(cards) > 21:
    cards.remove(11)
    cards.append(1)
  return sum(cards)

#Hint 13: Create a function called compare() and pass in the user_score and computer_score. If the computer and user both have the same score, then it's a draw. If the computer has a blackjack (0), then the user loses. If the user has a blackjack (0), then the user wins. If the user_score is over 21, then the user loses. If the computer_score is over 21, then the computer loses. If none of the above, then the player with the highest score wins.
def compare(user_score, computer_score):
  #Bug fix. If you and the computer are both over, you lose.
  if user_score > 21 and computer_score > 21:
    return "You went over. You lose 😤"


  if user_score == computer_score:
    return "Draw 🙃"
  elif computer_score == 0:
    return "Lose, opponent has Blackjack 😱"
  elif user_score == 0:
    return "Win with a Blackjack 😎"
  elif user_score > 21:
    return "You went over. You lose 😭"
  elif computer_score > 21:
    return "Opponent went over. You win 😁"
  elif user_score > computer_score:
    return "You win 😃"
  else:
    return "You lose 😤"

def play_game():

  print(logo)

  #Hint 5: Deal the user and computer 2 cards each using deal_card()
  user_cards = []
  computer_cards = []
  is_game_over = False

  for _ in range(2):
    user_cards.append(deal_card())
    computer_cards.append(deal_card())

  #Hint 11: The score will need to be rechecked with every new card drawn and the checks in Hint 9 need to be repeated until the game ends.

  while not is_game_over:
    #Hint 9: Call calculate_score(). If the computer or the user has a blackjack (0) or if the user's score is over 21, then the game ends.
    user_score = calculate_score(user_cards)
    computer_score = calculate_score(computer_cards)
    print(f"   Your cards: {user_cards}, current score: {user_score}")
    print(f"   Computer's first card: {computer_cards[0]}")

    if user_score == 0 or computer_score == 0 or user_score > 21:
      is_game_over = True
    else:
      #Hint 10: If the game has not ended, ask the user if they want to draw another card. If yes, then use the deal_card() function to add another card to the user_cards List. If no, then the game has ended.
      user_should_deal = input("Type 'y' to get another card, type 'n' to pass: ")
      if user_should_deal == "y":
        user_cards.append(deal_card())
      else:
        is_game_over = True

  #Hint 12: Once the user is done, it's time to let the computer play. The computer should keep drawing cards as long as it has a score less than 17.
  while computer_score != 0 and computer_score < 17:
    computer_cards.append(deal_card())
    computer_score = calculate_score(computer_cards)

  print(f"   Your final hand: {user_cards}, final score: {user_score}")
  print(f"   Computer's final hand: {computer_cards}, final score: {computer_score}")
  print(compare(user_score, computer_score))

#Hint 14: Ask the user if they want to restart the game. If they answer yes, clear the console and start a new game of blackjack and show the logo from art.py.
while input("Do you want to play a game of Blackjack? Type 'y' or 'n': ") == "y":
  clear()
  play_game()


```

## Day 12 Scope
### Start code
```Python
################### Scope ####################

enemies = 1

def increase_enemies():
    enemies = 2
    print(f"enemies inside function: {enemies}")

increase_enemies()
print(f"enemies outside function: {enemies}")

# Local Scope

def drink_potion():
    potion_strength = 2
    print(potion_strength)

drink_potion()
print(potion_strength)

# Global Scope
player_health = 10

def game():
    def drink_potion():
        potion_strength = 2
        print(player_health)

    drink_potion()

print(player_health)

# There is no Block Scope

game_level = 3

def create_enemy():
    enemies = ["Skeleton", "Zombie", "Alien"]
    if game_level < 5:
        new_enemy = enemies[0]

    print(new_enemy)


# Modifying Global Scope

enemies = 1

def increase_enemies():
    print(f"enemies inside function: {enemies}")
    return enemies + 1

enemies = increase_enemies()
print(f"enemies outside function: {enemies}")

#Global Constants

PI = 3.14159
URL = "https://www.google.com"
TWITTER_HANDLE = "@yu_angela"


```


### Guess the number

```Python

from art import logo
from replit import clear
import random

# Welcom to the Number Guessing Game!
# I'm thinking of a number between 1 and 100.
# Choose a difficulty. Type 'easy' and 'hard':
# You have X attempts remaining to guess the number.
# Make a guess: XX
# Too high.
# Too low.
# Guess again
# You've run out of guess, you lose.
# This repl has exited, run again?
# You got it! The answer was XX.

guess_time = 0
game = True
chosen_number = random.randint(1,100)
print(logo)

level = input("Choose a difficulty. Type 'easy' and 'hard': ")
if level == "easy":
  guess_time = 10
elif level == "hard":
  guess_time =5

def compare(chosen_number, guess):
  global guess_time
  global game
  if guess == chosen_number:
    game = False
    return f"You got it! The answer was {chosen_number}"
  elif guess > chosen_number:
    guess_time -= 1
    return "Too high."
  elif guess < chosen_number:
    guess_time -= 1
    return "Too low."


while guess_time > 0 and game:
  print(f"You have {guess_time} attempts remaining to guess the number.")
  guess = int(input("Make a guess: "))
  print(compare(chosen_number, guess))
if guess_time == 0:
  print("You've run out of guess, you lose.")


```

### Angela's code
```Python
from random import randint
from art import logo

EASY_LEVEL_TURNS = 10
HARD_LEVEL_TURNS = 5

#Function to check user's guess against actual answer.
def check_answer(guess, answer, turns):
  """checks answer against guess. Returns the number of turns remaining."""
  if guess > answer:
    print("Too high.")
    return turns - 1
  elif guess < answer:
    print("Too low.")
    return turns - 1
  else:
    print(f"You got it! The answer was {answer}.")

#Make function to set difficulty.
def set_difficulty():
  level = input("Choose a difficulty. Type 'easy' or 'hard': ")
  if level == "easy":
    return EASY_LEVEL_TURNS
  else:
    return HARD_LEVEL_TURNS

def game():
  print(logo)
  #Choosing a random number between 1 and 100.
  print("Welcome to the Number Guessing Game!")
  print("I'm thinking of a number between 1 and 100.")
  answer = randint(1, 100)
  print(f"Pssst, the correct answer is {answer}") 

  turns = set_difficulty()
  #Repeat the guessing functionality if they get it wrong.
  guess = 0
  while guess != answer:
    print(f"You have {turns} attempts remaining to guess the number.")

    #Let the user guess a number.
    guess = int(input("Make a guess: "))

    #Track the number of turns and reduce by 1 if they get it wrong.
    turns = check_answer(guess, answer, turns)
    if turns == 0:
      print("You've run out of guesses, you lose.")
      return
    elif guess != answer:
      print("Guess again.")


game()

```

## Day 13 Higher Lower
### My Code

```Python
import random
from replit import clear
from art import logo
from art import vs
from game_data import data

#Step 1：进入游戏
#Step 2：随机从dictionary里选两个人
#Step 3：选一个人
#Step 4：如果被选的少，不加分，结束游戏。
#Step 5：如果被选的多，加1分
#Step 6：抽选新的人，与上一轮第二个比较
#Step 7：重复第四步

# for thing in data:
# 	print(thing)

score = 0
game_continue = True


def compare(number_a, number_b):
    """compare follower's number of A and B"""
    choice = input("Who has more followers? Type 'A' or 'B': ").lower()
    if choice == 'a' and number_a > number_b:
        return True
    elif choice == 'b' and number_a < number_b:
        return True
    else:
        return False


option_a = random.choice(data)
option_b = random.choice(data)

print(logo)
print(
    f"Compare A: {option_a['name']}, a {option_a['description']}, from {option_a['country']}."
)
print(vs)
print(
    f"Against B: {option_b['name']}, a {option_b['description']}, from {option_b['country']}."
)

while game_continue:
	if compare(option_a['follower_count'], option_b['follower_count']):
		clear()
		print(logo)	
		score += 1
		print(f"You're right. Current score: {score}")
		option_a = option_b
		option_b = random.choice(data)
		print(f"Compare A: {option_a['name']}, a {option_a['description']}, from {option_a['country']}.")
		print(vs)
		print(f"Against B: {option_b['name']}, a {option_b['description']}, from {option_b['country']}.")
	
	else:
		clear()
		print(logo)
		print(f"Sorry, that's wrong. Final score: {score}")
		game_continue = False


```
### Angela's method
```Python
# Generate a random account from the game data.

# Format account data into printable format.

# Ask user for a guess.

# Check if user is correct.
## Get follower count.
## If Statement

# Feedback.

# Score Keeping.

# Make game repeatable.

# Make B become the next A.

# Add art.

# Clear screen between rounds.

from art import logo, vs
from game_data import data
import random
from replit import clear


def get_random_account():
	'''Get data from random account'''
	return random.choice(data)


def format_data(account):
	'''Format account in to printable format: name description and country '''
	name = account["name"]
	description = account["description"]
	country = account["country"]
	return f"{name}, a {description}, from {country}"


def check_answer(guess, a_followers, b_followers):
	'''compare followers and return True of False'''
	if a_followers > b_followers:
		return guess == 'a'
	elif b_followers > a_followers:
		return guess == 'b'

def game():
	print(logo)
	score = 0
	game_continue = True
	account_a = get_random_account()
	account_b = get_random_account()

	while game_continue:
		account_a = account_b
		account_b = get_random_account()

		while account_a == account_b:
			account_b = get_random_account()

		print(f"Compare A: {format_data(account_a)}.")
		print(vs)
		print(f"Against B: {format_data(account_b)}.")

		a_or_b = input("Whos has more followers? Tyep 'A' or 'B': ").lower()
		a_follower = account_a["follower_count"]
		b_follower = account_b["follower_count"]
		is_correct = check_answer(a_or_b, a_follower, b_follower)

		clear()
		print(logo)
		if is_correct:
			score += 1
			print(f"You're right! Current score: {score}.")
		else:
			game_continue = False
			print(f"Sorry, that's wrong. Final score: {score}.")


game()


```
