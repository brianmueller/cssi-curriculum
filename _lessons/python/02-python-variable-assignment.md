---
  layout: post
  title: Python Variable Assignment
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
Variables are like buckets that store pieces of information. We name the variable and fill it with pieces of data that are relevant. Variables can store any type of data (strings, integers, floats, etc).

```python
>>> x = 15;
>>> x
15
```

You can use the variable by name - just type it where you would otherwise want the data it has inside. For instance, the following statements are equivalent:

```python
>>> 30/5
6
```
and:

```python
>>> students = 30
>>> instructors = 5
>>> students/instructors
6
```

#  Variable Re-assignment
We can change what's in the box at any time.

```python
>>> minion = 'Kevin'
>>> minion
'Kevin'
>>> print minion
Kevin
```
What will happen when we run the following?

```python
>>> name = "Kevin"
>>> name = "Carl"
>>> print name
```

On the first line, we assigned the value `"Kevin"` to the variable `name`. On the next line, we reassigned the value of the variable `name` to `"Carl"`. Each variable can only store one value - `"Kevin"` was replaced by the new value. When we print name on the last line, we will see `"Carl"` - the last thing we assigned to name.

# Naming Conventions

What if we want to have more than one word in our variable name? Like:

```python
>>> despicable me = "Gru"
>>> print despicable me
```
Python gives us an error!
`SyntaxError: invalid syntax.`

Python doesn't know what despicable is because of the space between the words despicable and me. The space confuses the computer!

If we want a multi-word variable name, we can instead separate the words with underscores:

```python
>>> despicable_me = "Gru"
>>> print despicable_me
Gru
```
And no error! this_style_is_called_snake_case. It's a little bit more readable than its alternative - CamelCase. Python prizes readability, so variables use snake case.

# Practice
Enter each of these into Python.  Some will work, some will give an error message.  Figure out why.

```python
college = 'Stanford'
print college
```

```python
'college' = 'Stanford'
print college
```

```python
college = Stanford
print college
```

```python
major = 'Computer Science'
print major
```

```python
major = college
print major
print college
```
