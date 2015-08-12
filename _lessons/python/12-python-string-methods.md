---
  layout: post
  title: Python String Methods
  language: python
---
# What You Need to Know
+ Python datatypes
+ Python basics
+ Index positions

# What You Will Learn
+ Understand the syntax of strings in Python
+ How to get data from the user
+ How to concatenate strings
+ How to interpolate with str.format() and %s

# Why This is Important
Python has lots of prebuilt string methods that help us use and modify strings.

# Strings
Let's explore how to use some string methods, and then jump into some challenges. Remember, you can always look back at these pages as a reference, or search for the method that you need. It's good to practice using these methods, but it's always okay to look up the function name and the syntax.

# Printing Strings
```
print 'hello, world!'
```
displays
```
hello, world!
```

# User Input
Remember in Python, if you want to get text from a user, you can use the raw_input() function. 

```
>>> name = raw_input('Enter your name: ')
Enter your name: Joseph
>>> name
'Joseph'
```

The raw_input() function allows the user to input any answer. The input() function will only allow the user to input a string.  

# String Concatenation
The process of joining two strings is called ***concatenation*** in programming. This is one of those things that might seem intuitive to a human but needs to be spelled out explicitly for the computer. For instance, when I run this, what will display?
```
celebrity_couple = 'Kim' + 'ye'
print celebrity_couple
```
Python doesn't add anything extra - if you want a space between your words, you need to put it there!

When you try to concatenate a string with a datatype other than another string you will get an error.
```
tv_show= 30 + "rock"
print tv_show
TypeError: cannot concatenate 'str' and 'int' objects
```

# Substrings
A substring is a part of a string.  To get a substring from a string, use square brackets and specify the range of characters that you want from the string. Just like in javascript arrays and python lists, string characters are indexed starting at 0.

Grabbing a specific character:
```
>>> google = 'android'
>>> print google[0]
a
```

Grabbing a substring of a range of characters:
```
>>> google = 'android'
>>> print google[0:4]
andr
```
As you might be able to guess, the selection works like this:
```
<string>[<first character position>: <last character position +1>]
```
Here are a couple handy shortcuts for selecting particular parts of strings:
```
>>> print google[3:] #  character position 3 to the end
roid
>>> print google[:5] #  From the beginning to character position 4
andro
```
# String Length

Python gives us the len() function to determine a string's length.
```
>>> short = "o"
>>> long_string = "(pumba) When I was a young warthog… (timon) When he was a young waaarthoooooooooooooog!"
>>> len(short_string)
1
>>> len(long_string)
89
```

# Replace Function
Replace() replaces a substring of a string with another substring.
```
>>> google = 'android'
>>> googley = google.replace('android', 'ANDROID')
>>> print googley
ANDROID
```
#  Lower and Upper Function

lower() and upper() make strings lowercase and uppercase respectively.
```
>>> celebrity = 'Beyonce'
>>> print celebrity.lower()
beyonce
>>> print celebrity.upper() + '!!!'
BEYONCE!!!
```

# Strip Function
The strip() function removes leading and trailing white space.
```
>>>print '     spaces everywhere     '.strip()
spaces everywhere
```

# String Formatting and Interpolation
String interpolation lets us pass different data into a string, which is faster and more convenient than keeping track of different pieces of string and concatenating them ourselves. There are two ways to do string interpolation. With the .format method and with the %s. Let's take a look at the difference:


***.format***
This is the newer version of using variables within string in Python.

The string is in quotes. The placeholder for the variable is surrounded by curly brackets.  The entire string is followed by .format(). Inside the parenthesis, declare what the substituted variable will be.

The Spongebob example uses a keyword argument, 'character', which is assigned to a global variable, 'name'.
```
name = "Spongebob Squarepants"
print "Who lives in a Pineapple under the sea? {character}".format(character=name)
>> Who lives in a Pineapple under the sea? Spongebob Squarepants.
```
The hobby example uses two keyword arguments: 'name' and 'hobby', which are assigned to strings within .format()

```
print "{name} is the best at {hobby}".format(name='Charlie', hobby='playing piano')
>>Charlie is the best at playing piano
```

This final example uses positional arguments:
```
print "There are {0} students at CSSI in {1}!".format(30, "Chicago")
>>There are 30 students at CSSI in Chicago!
```
***%s***
The older way to use variables in strings and uses the % operator.

Again the whole string is in quotes. The placeholder for the variable is a percent sign and the first letter of the datatype. (%d int, %s string, %f/%g float). The entire string is followed by a percent sign and the name of the variable

```
print "The %s have %d %s championships in %d years" %("Chicago",3, "NHL", 3)
>>The Chicago have 3 NHL championships in 3 years
```

## Exercise: User Input App
Let's build a simple input/output app. The main objective is to create an application that _takes in user input, does something with that input, and then prints out an output_.

###  Get User Input
The first thing we need to do is take in user input with the `raw_input()` method. When an executed Python program hits the method `raw_input()`, the program pauses and waits for the user to enter text into the terminal.

The way `raw_input()` takes in data from the user is important to remember. It does not interpret the data entered, it merely returns exactly what the user enters, the raw data. The second thing to remember is that `raw_input()`  takes exactly one line of input. Once the user presses enter, what is on that line is what raw_input() returns.

###  The Challenge: A Visit to My Favorite City
Let's build an application to plan tourists' visits to your favorite city. Create a new file with `touch trip.py` in terminal. Open `trip.py` with Atom to start writing your program.

Ask the user where they would like to stay, what sites they want to visit, what food they want to eat, and how many nights they want to stay. For each question, take input from the user and store it in a variable. <img src="https://s3.amazonaws.com/after-school-assets/greetings.jpg" align="right" width="300" hspace="20">

Once you have that input stored, use string methods (upper(), lower(), capitalize(), etc) to put the input in the proper format. You can always take a look at the Python documentation [here](https://docs.python.org/2/library/stdtypes.html) to learn more about string methods you can use.

Your final output should use *string interpolation* to output the data in a full summary of their trip itinerary. The output should look like this:

Destination: Washington DC
Sites:
 - Visiting the Washington Monument
 - Visiting the Air And Space Museum
 - Visiting the White House
Food: Burgers and Fries
Nights: 3

Remember, you can execute your code by typing `python trip.py` in terminal from inside the directory of this lab. Good luck!

#  Conclusion
There are a lot of string methods that we can access in python. Whenever you don't remember if one exists, or the syntax, you can always look up the documentation.

#  References
[Python String Interpolation Guide] (https://mkaz.com/2012/10/10/python-string-format/)
