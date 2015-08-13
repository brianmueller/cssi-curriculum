---
layout: post
title: Intro to Python
language: python
---
# What You Will Learn
+	Interact with python (interpreter, text editor + run from command line)
+ Understand Basic concepts in python
+ Print a string
+ Add and multiply numbers
+ Understanding and error

# Why Should You Care?
Python is a scripting language - it is used to perform tasks. Those tasks might be scientific calculations and data analysis, binding together the pieces of a game engine, or, as we'll be using it next week, running a web app. When we run python, we don't run it through the browser, we run it directly on our machines.

# Python Interpreter or Python Script

**Python interpreter**-We start it from the command line and it is most useful when we want to test things out or quickly do a calculation. Just like the javascript console, it evaluates statements and prints the return value back to us immediately.

**Python scripts**- are text files saved with a .py extension, and run from the command line. Scripts are full programs - we can save them, change them, share them, and reuse them. We'll use them to write much more complex code than we could in the interpreter.

#Python Interpreter

# Python Interpreter
Open your terminal and type...

```python
$ python
```
You'll see something like...

```python
Python 2.5.1 (r251:54863, Jun 17 2009, 20:37:34)
[GCC 4.0.1 (Apple Inc. build 5465)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
The interpreter allows you to run individual lines of Python code one at a time. This allows you to try things quickly.

## Integers
Let's try some basic math. The basic math operations work the same as they do in javascript. We do math with integers, which is the first datatype we can experiment with.

```python
>>> 6 + 8
14
>>>
```

## Floats

```python
>>> 10/3
3
>>>
```
If we divide an integer by another integer, python will only return an integer. In python, any number with a decimal is a new datatype, a float.

To return a float, your math operations need to include a float.

```python
>>> 10/3.0
3.3333333333333335
>>>
```

## Python Strings
We can also use other characters, aside from numbers, like letters and punctuation. These datatypes are called strings. Put characters between a set of quotes so that the interpreter knows we're inputting a new datatype.

```python
>>> 'Hello'
'Hello'
>>>'Hello' + ' Nicki!'
'Hello Nicki!'
```

##Python Booleans

```python
>>> 5==4
False
>>> 'five' == 'five'
True
```

Python has the == operator for checking equality. It returns a boolean value, which is either True or False.

## Exiting the Interpreter
Close the prompt with

```python
>>> quit()
```
A few thing to note:

+ When you close the prompt, the session is not saved anywhere
+ The three carrots >>> are the python prompt.  
+ The interactive mode should be used for testing out python code - if you want to be able to save your work, put it in a file!

# Creating and Running a Python Script

When developers want to save their work or run multiple lines of code, they must write a script.

+ Open Terminal
+ cd ~/cssi
+ mk dir python_practice
+ cd python_practice
+ touch practice.py
+ open -a Atom practice.py

Let's write the most basic file we can, to test that we can run a script.

```python
print 'hello, world'
print 5 * 4
```
Save. Back in the terminal, run the script with python and the name of your file, like this:

```python
$ python practice.py
```

A few things to note here:

+ The .py ending tells us that it is a Python file
+ You need to be in the same directory as the python script
+ Python scripts are lines of code executed from top to bottom

# Comments
When writing scripts, it is important to add comments, notes that help clarify your code. In Python, you can make a one-lined comment by using the `#` character. In order to make multi-line comments, you start and end your comment with three quotation marks `"""`


# Conclusion
Here are some python resources <a href="http://anandology.com/python-practice-book/getting-started.html">documentation</a> on the Python interpreter
