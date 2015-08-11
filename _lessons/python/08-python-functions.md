---
  layout: post
  title: Python Functions
  language: python
---

# What You Will Learn
+ What functions are, and how we use them in python
+ N.I.C.O (Name, Input, Code, Output)
+ How to declare functions with and without parameters
+ Call functions with and without passing arguments
+ Output vs. Return Values
+ Local and global variable scope

# Why This is Important:
Functions let us package code into blocks that we can reuse. We've been using a handful functions already and this lesson will explain how and why we've been doing that.

In programming, a function holds a set of actions that will run when we call that function. This helps us control the flow of our program and allows us to easily repeat a set of actions multiple times.

# Function Declaration
A python function is essentially a set of instructions that we write out and can reuse over and over again.

The syntax for writing python functions is very specific. Let’s write a function in python to go get dinner. To define a function in python, you use the `def` keyword, followed by the name of the function, parentheses, and a colon. Like this:

```python
def GoGetDinner():
```

Then, you write the block of code defining what the function does. Remember to indent your block of code - that's what tells python which statements are part of your function, and when your function declaration is over.

```python
def GoGetDinner():
  print "Stop what you're doing. "
  print "Wash your hands. "
  print "Get a plate of food."
  print "EAT!"
```
Copy this code in a file dinner.py, and run it from the command line.

Nothing happened. Why is that? We declared our function, but didn't call it. Declaring the function is like writing down a set of instructions - we never told python to execute the function.

# Calling a Function

Whenever we want a function to run, we need to write the name of the function and include parenthesis. The parentheis should contain your arguments if needed. This is called 'calling' the function. Python will run the function when you include `GoGetDinner()` in the code.

This is the equivalent of telling the computer - do those steps in the `GoGetDinner` function. Test it out.
What’s up with those parentheses? Those are like a placeholder for something called an argument.
Our instructions are pretty generic right now. What if we wanted to direct them towards a specific student? Like adding a step that says “hey, Joe”.

# Using Parameters (Inputs)

```python
def GoGetDinner(student):
	print 'hey, ' + student
	print 'close your computer'
	print 'stand up'
	print 'walk out the door'
```

 We can reuse this function and just change the name of the student we address by adding a student parameter.

 Then we can call the function by writing the name of the function and a name as the argument.


```python
GoGetDinner("Joe");
GoGetDinner("Jill");
GoGetDinner("Josie");
```
#  Arguments vs Parameters
* A parameter is a variable in the function definition: "student".
* An argument is the data you pass into the function's parameters when you call it: "Joe", "Jill", "Josie"

#  Return Values

There is one more VERY IMPORTANT thing about functions - return values.
A function is kind of like placing a mouse in a box. That mouse will only perform the actions he was trained to do and will only do those actions when he is told to.

Here is Cheddar in his box. We’ve trained him to `DoMath` (addition really) with two parameters, x and y.

```python
def DoMath(x,y):
	return x + y
```
Notice there is a `return` statement at then end of the function. We need to include `return` in order to get something back from the function. In essence if we left off the return statement Cheddar might perform the math in his head but not give us the answer. By saying return we’re telling the function give us back the answer.

#  N.I.C.O

We can break down the creation of functions into four things that every function has:

 * **Name** - Decide an appropriate name for the function
 * **Inputs** - Figure out what inputs, if any, are needed to accomplish what the name describes
 * **Code** - Put the code inside the function to be run when it is called
 * **Outputs** - A value that the function can return though it can be `undefined`

#  Variable Scope

Another thing that is important to understand about python functions is variable scope.

When you declare a variable outside of a function it will also be available inside of the function. This is called a global variable. For example:

 ```
 milkType = "skim milk" # global variable
 def IsWholeMilk():
 	if (milkType == "whole milk”):
 		return true
 	else:
 		return false
```

If I run `IsWholeMilk();` we’ll get back false. The function `IsWholeMilk` has access to the variable milkType that was declared outside of the function.

If you declare a variable inside of a function it will only be available inside of the function. This is called a local variable.

Here is an example:

 ```
 def milkTheCow():
   bessyCow = 'milked'  #  local var
   return bessyCow;

 print bessyCow  #  Throws an error, since the variable is local to the function 'milkTheCow'

 print milkTheCow()  #  Prints correctly since we are printing the returned value, bessyCow now
 ```

If we type `bessyCow` we’ll get an error. We are trying to access `bessyCow` from outside of the function and she only exists inside of the function.
The only way you can get access to `bessyCow` is if you call the function.

*Variable scope*  seems complicated but it's really important and helpful to seperate function variable and global variables.

# Lists as Parameters

 Functions can accept lists as inputs:

 ```
def GetMaximumLength(list_of_strings):
     lengths = []
     for item in list_of_strings:
         lengths.append(len(item))
     return max(lengths)

print GetMaximumLength(['hello', 'from', 'cssi', 'at', 'google'])
 ```

Functions can return lists:

 ```
 def GetDigits(my_string):
     digits = []
     for letter in my_string:
         if letter.isdigit():
             digits.append(letter)
     return digits

 print GetDigits('It is 71 degrees today')
 ```

 Functions can modify their arguments:

 ```
 def SwapEnds(some_list):
     some_list[0] = some_list[-1]


 def MessWithList(my_list):
     SwapEnds(my_list)
     my_list.append(5)


 a_list = [1, 2, 3, 4]
 print a_list
 MessWithList(a_list)
 print a_list
 ```

# Conclusion / So What?

 Functions are the building block of any developer. They let you create little machines (mice) that you can use and re-use from other parts of your code. This can make life a lot easier and save a ton of typing!
