---
  layout: post
  title: Python Lists and Loops
  language: python
---

# What You Will Learn
+ Create a list in python syntax
+ Create a loop in python syntax

# Why This is Important:
In this lesson you will learn how to create python's version of an array, a list. You will also learn how to use loops in your python code.

# Lists
A list is the most basic python data structure. It is a list of objects or values. The syntax for a list is a set of objects enclosed in brackets. To create an empty list, set a variable equal to empty brackets:
```
>>> empty_list = []
```
To create a list with some elements in it, just add the elements separated by commas:
```
>>> groceries = ['Eggs', 'Milk','Butter']
```
### Accessing items in a list
List items have an index and are accessed like they were in javascript:

```
>>> groceries[0]
'Eggs'
>>> groceries[1]
'Milk'
>>> groceries[0:2]
['Eggs', 'Milk']
>>> groceries[1:]
['Milk', 'Butter']
```

### Modifying a List
The easiest way to modify a list’s content is to just access the list element by its index (numerical place in the list) and use the assignment operator.
```
>>> groceries
['Eggs', 'Milk','Butter']
>>> groceries[0] = 'Bread'
>>> groceries
['Bread', 'Milk', 'Butter']
```
Another convenient way to modify a list is the append() method. The append method allows you to stick an element at the end of a list.
```
>>> groceries.append('Asparagus')
>>> groceries
['Bread', 'Milk', 'Butter', 'Asparagus']
```

### List Methods
Using the len function, you can return the number of items in a list:
```
>>> print len(groceries)
3
```
Here are some other list methods that will come in handy:
```
groceries.extend(['Rutabaga', 'Ice Cream'])
['Bread', 'Milk', 'Butter', 'Asparagus','Rutabaga', 'Ice Cream']

del groceries[3] # removes 'Asparagus' from the list
['Bread', 'Milk', 'Butter','Rutabaga', 'Ice Cream']

groceries.remove('Rutabaga')
['Bread','Milk','Butter','Ice Cream']

groceries.sort()
['Bread', 'Butter', 'Ice Cream', 'Milk']
```

###  'In' and 'Not' Operator
What if you have a list of groceries and you want to check if ‘apples’ is in that list? Or a list of names and you want to check to see if someone is present? Use the 'in' operator.
```python
if 'albert' in students:
  print 'good, albert is here'
else:
  print 'gosh, where is albert?!'
```
To check if an element is absent from a list, use the 'not' in operator:
```python
if 'albert' not in students:
  print 'where is albert?!'
```

### range(): building lists of numbers easily
It is frequently useful to be able to generate a list of numbers. Rather than have you type out all the numbers you want, Python makes this easy:
```
>>> print range(0,10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>> print range(0,100,10)
[0, 10, 20, 30, 40, 50, 60, 70, 80, 90]
```
Generally, ranges have the form:
`range(<start_int>, <end_int>, <interval>)`

# Loops
Loops let us repeat a section of code over and over, even if we only type it out once.

### For Loops
The simplest looping situation is where you need to do something _for_ a certain number of times. To do this, Python uses a for loop.

#####  Example 1: Looping Through a List


This code will repeat for every element in the list.

```python
for name in ["Lucy", "Riccardo", "Ricky Jr."]:
  print name
```
Note that the variable `name` is what we are calling each element within the list. We could call that variable anything: `character`, `person`, `actor`. It doesn't matter, as long as we continue to use that variable later within the _for_ block.

Alternatively, we can declare a variable `names` which contains a list of our lovely characters, and then use the same syntax.
```python
# same result, slightly different syntax

names = ["Lucy", "Riccardo", "Ricky Jr."]:
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

# Conclusion
Creating, modifying and accessing lists are important for every programmer, as is being able to use _for_ loops and _while_ loops. Practicing these small examples are a great way to build your foundation as a strong developer.
