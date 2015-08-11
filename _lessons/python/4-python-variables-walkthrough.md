---
  layout: post
  title: Python Variable Assignment Walkthrough
  language: python
---
# What You Will Learn

+ Understand common python syntax and datatypes
+ Understand how to assign variables
+ Learn python syntax for variable assignment

# Why This is Important
Python is a powerful programming language - it's a tool that you will be able to use to solve many different kinds of problems. Just like we can only solve problems with English once we have the basic rules down, we have to know the basics. We'll translate some of the programming concepts we learned in javascript into python, and practice with lots of exercises and labs.

If you get stuck, remember that you're not just learning to program - you're learning to learn. Try searching the official Python documentation and googling for answers. If you can't figure out how to phrase the search, or you searched and can't find results, try to work it out with those around you. If neither of you can figure it out, there are plenty of TAs and instructors - we'll probably find you before you even call us, but don't hesitate.

# Variable Assignment
Open up Terminal and launch the python interpreter to follow along as we learn the basics.

Variables are like buckets that store pieces of information. We name the variable and fill it with pieces of data that are relevant.

Variables in Python don’t need any special declaration to bring them into existence. In javascript, we needed the var keyword to tell the browser about our variable.
```
> var x = 15;
> x
15
```
In python we don't need var or a ;
```
>>> x = 15
>>> x
15
```
Just like javascript, you can use the variable by name - just type it where you would otherwise want the data it has inside. For instance, the following statements are equivalent:
```
>>> 30/5
6
and:
>>> students = 30
>>> instructors = 5
>>> students/instructors
6
```
#  Variable Re-assignment
Just like in javascript, we can change what's in the box at any time.
```
>>> minion = "Kevin"
>>> print minion
Kevin
```
What will happen when we run the following?
```
>>> name = "Kevin"
>>> name = "Carl"
>>> print name
```

On the first line, we assigned the variable name to store Kevin. On the next line, we reassigned the value of the variable name to store Carl. Each variable can only store one value, so we overwrote name, replacing what was inside with the new value. When we print name on the last line, we will see Carl - the last thing we assigned to name.

# Naming Conventions

Variables can store any type of data (strings, integers, floats, etc). When we name a variable, we use all lowercase letters.

What if we want to have more than one word in our variable? Like:
```
>>> despicable me = "Gru"
>>> print despicable me
```
Python gives us an error!
SyntaxError: invalid syntax.

Python doesn't know what despicable is because of the space between the words despicable and me. The space confuses the computer!

If we want a multi-word variable name, we can instead separate the words with underscores:
```
>>> despicable_me = "Gru"
>>> print despicable_me
Gru
```
And no error! this_style_is_called_snake_case. It's a little bit more readable than its alternative - CamelCase. Python prizes readability, so variables use snake case.

# Student Practice
Enter each of these into Python.  Some will work, some will give an error message.  Figure out why.
```
college = 'Illinois'
print college
```
```
'college' = 'Illinois'
print college
```
```
college = Illinois
print college
```
```
major = 'Computer Science'
print major
```
```
major = college
print major
print college
```
