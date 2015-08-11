---
  layout: post
  title: Python Lists
  language: python
---
# What You Need to Know:
+ Command-line Basics
+ Basic Python syntax and datatypes

# What You Will Learn
+ How to create a list in Python syntax

# Why This is Important:
In this lesson you will learn how to create a Python list.

# Lists
A list is the most basic Python data structure. It is a list of objects or values. The syntax for a list is a set of objects enclosed in brackets. To create an empty list, set a variable equal to empty brackets:
```
>>> empty_list = []
```
To create a list with some objects in it, just add the elements separated by commas:
```
>>> groceries = ['Eggs', 'Milk','Butter']
```
### Accessing items in a list
List items have an index and are accessed by calling their index number. Numbering in the list starts at 0.
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
The easiest way to modify a list’s content is to just access the list object by its index (numerical place in the list) and use the assignment operator.
```
>>> groceries
['Eggs', 'Milk','Butter']
>>> groceries[0] = 'Bread'
>>> groceries
['Bread', 'Milk', 'Butter']
```
Another convenient way to modify a list is the append() method. The append method allows you to add an element at the end of a list.
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

#List Countries Exercise
<img src="https://s3.amazonaws.com/after-school-assets/globe.jpeg" align="right" width="300px" hspace="10">
+ Create a new Python file called countries.py. Create a list called `four_letter_countries` with the following countries (in this order):
	- Chad
	- Cuba
	- Greenland
	- Iraq
	- Mali
	- Oman
	- India

+ Add **Fiji** to the end of the list

+ Delete **India**

+ **Reverse** the order of the list

+ Replace Greenland with **Togo**

+ Add **Laos** to the end of the list

+ **Reverse** the order of the list again

+ Add **Peru** to the start of the list

#  What does your final list look like?


# Conclusion
Creating, modifying and accessing lists are important for every programmer, as is being able to use _for_ loops and _while_ loops. Practicing these small examples are a great way to build your foundation as a strong developer.
