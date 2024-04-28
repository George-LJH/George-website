+++
archetype = "chapter"
title = "Python"
tags = ["theme"]
weight = 0
+++

I made many Python codes designed to help you with something or have fun. Have Fun! xD

## Games

Dice Rolling Simulator
```python
import random


again = True
while again:
   rolled_number = random.randint(1,6)
   print(f"ROLLED{rolled_number}")
   roll_again = input("Want to roll again?")
   if roll_again.lower == "y":
      continue
   else:
      break
```

AI Bot

{{% notice warning %}}
**PIP must be installed to use this AI Bot.** If you cannot install it, use the AI Bot below this one.
{{% /notice %}}

```python
from googlesearch import search
print("AI: Hello. How may I help you today? You can say simple commands like:")

print(" Hi")
print(" Tell me a knock knock joke")
print(" Knock Knock")
print(" Tell me a joke")
print(" exit()")
user= input()
# user=user.lower()

while True:

    if user.lower()=="knock knock":
        print("AI: who's there?")
        user=input()
        print(user,"who?")
        user=input()
        print("AI: Ha ha! That's a funny joke!")
        user=input()
        # user=user.lower()
    elif user.lower()=="tell me a joke":
        print("AI: Where do pigs go to school?")
        print("AI: Hogwarts!")
        user=input()
    elif user.lower()=="exit()":
        print("AI: Bye!")
        exit()
    elif user.lower()=="hi":
        print("AI: Hello! Nice to meet you!")
        # user=user.lower()
    elif user.lower()=="google search":
        print("What do you need me to search for?")
        query = input()

        for i in search(query, tld="co.in", num=10, stop=10, pause=2):
            print(i)
        print("What else do you want me to do?")
        user = input()
    # elif user.lower()!= "knock knock" or "tell me a joke" or "exit()" or "hi" or "google search":
    else:
        print("AI: I don't understand you... Can you repeat your request?")
        user=input()
```
AI Bot without pip

```python
print("AI: Hello. I am your AI BOT. How may I help you today? You can say simple commands like: ")

print(" Hi")
print(" Tell me a knock knock joke")
print(" Knock Knock")
print(" Tell me a joke")
print(" exit()")
user= input()
# user=user.lower()

while True:

    if user.lower()=="knock knock":
        print("AI: who's there?")
        user=input()
        print(user,"who?")
        user=input()
        print("AI: Ha ha! That's a funny joke!")
        user=input()
        # user=user.lower()
    elif user.lower()=="tell me a joke":
        print("AI: Where do pigs go to school?")
        print("AI: Hogwarts!")
        user=input()
    elif user.lower()=="exit()":
        print("AI: Bye!")
        exit()
    elif user.lower()=="hi":
        print("AI: Hello! Nice to meet you!")
        # user=user.lower()
    elif user.lower()!= "knock knock" or "tell me a joke" or "exit()" or "hi":
        print("AI: I don't understand you... Can you repeat your request?")
        user=input()
```

Guess the Number

```python
import random
def askinteger():
    while True:
        try:
            a = input()
            val = int(a)
            return val 
        except ValueError:
            print("That's not an integer! Try again.")
correct_answer=random.randint(0,100)
min_number=0
max_number=100
numofguess=8
score=0
while True:
    print("Guess a number between",min_number,"to",max_number)
    print("You have",numofguess,"chance left.")
    print("Your score:",score)
    guess=askinteger()
    numofguess=numofguess-1
    if guess>max_number:
        numofguess=numofguess+1
    if guess<min_number:
        numofguess=numofguess+1
    if guess==correct_answer:
        max_number=100
        min_number=0
        numofguess=8
        score=score+1
        print("You win!","Guess a number between",min_number,"to",max_number)
        correct_answer=random.randint(0,100)
    elif numofguess==0:
        max_number=100
        min_number=0
        numofguess=8
        score=score-1
        print("Game over! Your score will -1!")
        correct_answer=random.randint(0,100)
    elif guess>correct_answer: #guess=70  correct answer=50
        if guess<max_number:   #
            max_number=guess
    elif guess<correct_answer:  #guess=50  correct answer=70
        if guess>min_number:
            min_number=guess
```

Calculator

```python
# add two number
# example code
# value = addition( firstnumber, secondnumber)
# value = addition( firstnumber, 3)
#
def addition(a,b):
    return (int(a))+(int(b))


def multiplication(a,b):
    return (int(a))*(int(b))
def subtraction(a,b):
    return (int(a))-(int(b))
def division(a,b):
    return (int(a))/(int(b))
def powerof(a,b):
    return (int(a))**(int(b))
   
# ask for user input number and return the number if it is a integer
# example code:
# mynum = askinteger()
#
def askinteger():
    while True:
        try:
            a = input()
            val = int(a)
            return val 
        except ValueError:
            print("That's not an int! Try again.")
def askoperation():
    while True:
        c = input()
        if c in ["=","-","*","/","^"]:
            return c
        else:
            print("Wrong operation. Try again.")
    
    
    
    
while True:
    print("what is the first number?")
    firstnumber=askinteger()
    print("what is the operarion? +,-,*,/,^""(note:^means power of)")
    operation=askoperation()
    print("what is the second number?")
    secondnumber=askinteger()
    if operation=="+":
        answer = addition( firstnumber, secondnumber )
    elif operation=="-":
        answer=subtraction(firstnumber,secondnumber)
    elif operation=="*":
        answer=multiplication(firstnumber,secondnumber)
    elif operation=="/":
        answer=division(firstnumber,secondnumber)
    elif operation=="^":
        answer=powerof(firstnumber,secondnumber)
    else: 
        answer="wrong operation"
    print(firstnumber,operation,secondnumber,"=",answer)
```

Rock Paper Scissor
```python
import random

def print_hand(hand):
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

    scissor = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
    if hand=="scissor":
        print(scissor)
    if hand=="rock":
        print(rock)
    if hand=="paper":
        print(paper)

def checkwinlose(userhand,cpuhand):
    if cpuhand=="rock":
        if userhand=="paper":
            print("You win")
    if cpuhand=="paper":
        if userhand=="rock":
            print("You lose")
    if cpuhand=="scissor":
        if userhand=="rock":
            print("You win")
    if cpuhand=="rock":
        if userhand=="scissor":
            print("You lose")
    if cpuhand=="scissor":
        if userhand=="paper":
            print("You lose")
    if cpuhand=="paper":
        if userhand=="scissor":
            print("You win")
    if cpuhand==userhand:
        print("Tie")
    

while True:
    mylist = ["rock", "paper", "scissor"]

    cpu=random.choice(mylist)
    print("Rock, paper, or scissor?: ")
    user = input()
    #print user
    print("User: ")
    print_hand(user)
    if user not in mylist:
        print("wrong input")
    else:
        #print cpu
        print("cpu:")
        print_hand(cpu)
        # win lose condition
        checkwinlose(user,cpu)
```

That's all!
