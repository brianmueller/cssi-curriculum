---
  layout: post
  title: 4-intro-to-python-walkthrough
  language: python
---
---
tags: cssi, basic python
level: 1
languages: python
---
# Intro to Python

# What You Will Learns:
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

# Python Interpreter
Open your terminal and type...
```
$ python
```
You'll see something like...
```
Python 2.5.1 (r251:54863, Jun 17 2009, 20:37:34)
[GCC 4.0.1 (Apple Inc. build 5465)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
The interpreter allows you to run individual lines of Python code one at a time. For now, all you need to know is that if you invoke the command python, it will open up the interactive mode and allow you to try things out quickly.

Let's try some things out
```
>>> print 'hello world'
hello world
```
print is python's equivalent of console.log in javascript. It lets us print a string out. What happens if we just type the string?

```
>>> 'hello world'
'hello world'
>>>
```
The interpreter tries to be helpful and prints out the return value of every line that we enter. When we just enter a string, python tells us that the line would evaluate to a string. What will happen when we run that line in a script?  

Let's try some basic math. The basic math operations work the same as they do in javascript.
```
>>> 6 + 8
14
>>>
```
Python math can get pretty complicated, but arithmetic is pretty straightforward. What's the order of operations in python?
```
>>> 7 + 6 * 8
>>> 7 + (6 * 8)
>>> (7 + 6) * 8
```
Experiment with print, numbers, and strings. You get some errors, but don't panic! Errors are great - our computer didn't break, and they tell us what to do next time.

```
>>> 5==4
False
>>> 'five' == 'five'
True
```

Python has the == operator for checking equality. It returns a boolean value, which is either True or False, just like we had in javascript.

Close the prompt with
```
>>> quit()
```
A few thing to note:
+ When you close the prompt, the session is not saved anywhere
+ The three carrots >>> are the python prompt.  
+ The interactive mode should be used for testing out python code - if you want to be able to save your work, put it in a file!

# Code along: Creating and Running a Python Script
+ Open Terminal
+ cd dev
+ mk dir python_practice
+ cd python_practice
+ touch practice.py
+ open -a Atom practice.py

Let's write the most basic file we can, to test that we can run a script.
```
print 'hello, world'
```
Save. Back in the terminal, run the script with python and the name of your file, like this:

```
$ python practice.py
```

A few things to note here:
+ The .py ending tells us that it is a Python file
+ You need to be in the same directory as the python script
+ Python scripts are lines of code executed from top to bottom

# Conclusion
Think-Pair-Share
Take a moment on your own to **think** about situations where it would make sense to use a python script vs. the python interpreter.

**pair** with your partner and come up with reasons where you might want to use a python script, and reasons where you might want to use the python interpreter . Make sure you can **share** your reasons in each scenario.

# Resources
Here is some <a href="http://anandology.com/python-practice-book/getting-started.html">documentation</a> on the Python interpreter 
