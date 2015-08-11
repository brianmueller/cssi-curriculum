---
  layout: post
  title: Python Libraries and Modules
  language: python
---

## Importing a Class
+ A class saved in its own .py file can be said to be in its own module. The module can be imported into another .py file with a couple lines of code at the top of the script:

```python
import musician
from musician import *
```
The first line imports the musician.py file itself. The second line imports all the classes and functions contained in that musician.py file.


## Importing a Library/Module
A Python Library is a module containing python scripts written and collected by someone else. There are tons of useful Python libraries out there that we can import into our scripts.

 <a href="http://pythontips.com/2013/07/30/20-python-libraries-you-cant-live-without/">Here’s a great list of possibilities! </a>

Here is an example of a basic Python library - **random.py**. You can find documentation on this library <a href="https://docs.python.org/2/library/random.html">here</a> to learn about all the different functions you can call from it.

Here is some simple code that uses the random library:

```python
import random

print random.randint(1,3)
```
## Exercise: Monopoly Auto Roller Mini App
In Monopoly, at the beginning of each turn, a player rolls two six sided dice. The numbers rolled on each die are added together to tell the player how many spaces to move. If the player rolls doubles, if they roll the same value on each die, then the player gets to move the total number of space, AND gets to roll again. Every time we run our monopoly dice app, it will tell us how many spaces we should move, and whether we have rolled doubles and get to go again, or whether it is the next player's turn.

The program should print a string that looks something like this if you roll doubles:
```python
Doubles! Move 6 spaces and roll again.
```
And if you don't roll doubles:
```python
Move 8 spaces. Next player's turn!
```
Remember to import your random library at the start of your script!

# Conclusion:
There are many libraries out there we can import to add to our Python coding power. Just take a look at the documentation to find out what cool functionality one will add to your script! We will be using import a lot when we talk about Google App Engine next week.
