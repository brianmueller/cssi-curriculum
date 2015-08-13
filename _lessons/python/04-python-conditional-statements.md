---
  layout: post
  title: Python Conditional Statements
  language: python
---
# What You Will Learn
+ How to get input from a user
+ Understand the syntax of conditional statements
+ Use conditional statements
+ Understand what a boolean is

# Why This is Important
Sometimes we only want our code to run if certain conditions are in place. If a condition is met, then python should run the code otherwise something else should happen.

## User Input
In python, if you want to get text from a user, you can use the raw_input() function. Let's try it out!

```python
>>> name = raw_input('Enter your name: ')
Enter your name: Georgia
>>> name
'Georgia'
```

The raw_input() method allows the user to input any answer. The input() function will only allow the user to input a string.

# Conditionals
Conditional statements are a type of control flow: They can control which parts of code get executed, and which do not. The basic conditional statement is the if statement:

```python
if condition_1:
    run this block of code
```
Here is an example with two variables:

```python
yourAnimal = raw_input('What is your favorite animal? ')
myAnimal = "dog"

if yourAnimal == myAnimal:
  print "That's my favorite animal, too!"
```

# Comparison Operator
  + "==" means "are these two things equal?".
  + "=", means assignment - you're setting a variable equal to a value.

# Boolean Values
False and True are special values called **booleans**. Booleans can be assigned to variables.
For example:

```python
x = (3 == 5)
print x
```
First, we calculate (3 == 5). This is a question: "Is 3 equal to 5?". The answer to that question is False: 3 is not equal to 5.

So, when we say x = (3==5), this is equivalent to x = False. We're setting X to the boolean value False. Now, when we print x, we just print out False.

Here are some important boolean operators:
<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-2.5-conditional-statements/master/js-boolean-operator-table.png">

# Else and Elif conditional statements
There are a few other conditional statements that work together with if. For example, you often want to do something if the condition failed:

```python
yourAnimal = raw_input('What is your favorite animal? ')
myAnimal = "dog"
if yourAnimal == myAnimal:
  print "That's my favorite animal, too!"
else:
  print "I don't think you understand how cool dogs are."
```


There's also "elif".  This is the "catch-all" branch, if a condition is not met in the prior branches, then the code in the elif branch will be executed.

```python
if x > 500:
  print "x is really big"
elif x > 50:
  print "x is sort of big"
elif x < 0:
  print "x is negative!"
else:
  print "x is not very interesting"
```
# Student Practice
In your practice.py try writing a conditional statement with an if condition, elif condition and else condition

 * **Pick a Number:** Write a program that makes the user guess a number 1-10. If their guess is correct, tell them they've won. If their guess is too high or too low, give the user a hint. you will need to use python's `input()` method.
  * `userGuess = input('Guess a number between 1-10')`

 * **Stretch: Phone Number Validator:** Write a program that checks if a string is formatted correctly as a phone number (312)867-5309.
  * Check if there are 10 integers
  * Check if the first three integers are between two parenthesis
  * Check to make sure that a dash separates the 6th and 7th integer.
