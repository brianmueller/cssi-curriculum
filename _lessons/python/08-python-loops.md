---
  layout: post
  title: Python Lists and Loops
  language: python
---
# What You Need to Know:
+ Command-line Basics
+ Python Lists

# What You Will Learn:
+ How to create a loop in Python syntax.
+ How and when to use for loops, while and while/else loops.

# Why This is Important:
As a programmer, whenever you find yourself repeating an action in your code, you can probably write some code to do that repetitive task for you and save lots of time, this is where writing loops becomes very valuable. Loops allow you to automate iteration through a list or task.

# Loops
Loops let us repeat a section of code over and over, even if we only type it out once.

### For Loops
The most basic reason to use looping  is when you need to do something _for_ a certain number of times. To do this, Python uses a ***for loop***.

#####  Example 1: Looping Through a List

This code will repeat for every element in the list.

```python
for name in ["Finn", "Jake", "Marceline"]:
  print name
```
Note that the variable `name` is what we are calling each element within the list. We could call that variable anything: `character`, `person`, `actor`. It doesn't matter, as long as we continue to use that variable later within the _for_ block.

Alternatively, we can declare a variable `names` which contains a list of our lovely characters, and then use the same syntax.
```python
# same result, slightly different syntax

names = ["Finn", "Jake", "Marceline"]:
for name in names:
  print name
```
#####  Example 2: Looping through Integers

The _for_ loop syntax is similar for integers.
* Notice that in this example we also used string interpolation.
* This code will repeat for every integer in the range.

```python
for i in range(1, 4):
  print "I am looping and am currently on %d." % i

# again, you can also declare your variable before the loop
my_range = range(1,4)
for i in my_range:
  print "I am looping and am currently on %d." % i
```
### While Loops
While loops continue to repeat _while_ - or as long as - a certain condition is met. A while loop has a block of code and a condition.

#####  Example 1: A Simple While Loop
This code will repeat while the condition `n<5` is met. It will stop when n is equal to 5.

```python
n = 0
while n < 5:
  print n
  n = n + 1
```
#####  Example 2: A While/Else Loop
This code is similar to the first _while_ loop example, except that there is an `else` statement. Once the condition `n<5` is not met, the instructions in the `else` block are executed. Then, the entire _while_ loop is exited, and the next instruction (to print `"You counted to 5"`) is executed.
```python
n = 0
while n < 5:
  print n, " is  less than 5"
  n = n + 1
else:
  print n, " is not less than 5"

print "You counted to 5"
```
# Loops Exercises:

###  Add Ten and Divide By Two
```
some_numbers =[2, 52, 19, 46, 1000]
```
Use a loop to add ten to each number in the list and then divide it by two and print this new number to the screen.

###  Reverse Presidents
 ```
 presidents = ["George Washington", "John Adams", "Thomas Jefferson", "James Madison", "James Monroe", "John Quincy Adams"]
 ```
Use a loop to print out a string with the name reversed for each of the presidents in the `presidents` list.

###  10 Bottles of Milk on the Wall
Create an list with all the numbers from 10 down to 0. Using a loop, for every number print the string "___ bottles of milk on the wall", filling in the blank with the number in your list.

# Conclusion
Creating, modifying and accessing lists are important for every programmer, as is being able to use _for_ loops and _while_ loops. Practicing these small examples are a great way to build your foundation as a strong developer.
