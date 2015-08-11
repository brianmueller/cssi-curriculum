---
  layout: post
  title: Python Libraries and Modules
  language: python
---

## Importing a Class
+ A class saved in its own .py file, in its own module, can be imported into another .py file at the top of the script:

```python
import musician
from musician import *
```
The first line imports the musician.py file itself. The second line imports all the classes and functions contained in that musician.py file.



## Importing a Library/Module
 Remember when we linked to the JQuery library for Javascript? There are tons of python libraries out there that we can import into our scripts.

 <a href="http://pythontips.com/2013/07/30/20-python-libraries-you-cant-live-without/">Here’s a great list of possibilities! </a>


Here is an example of a basic python library - **random.py**. You can find documentation on this library <a href="https://docs.python.org/2/library/random.html">here</a> to learn about all the different functions you can call from it.

Here is some simple code that uses the random library:

```python
import random

print random.randint(1,3)

```

## PARTNER PROGRAMMING:

<a href="https://github.com/learn-co-curriculum/cssi-5.2-monopoly-dice-mini-app">Basic Random Lab: Monopoly Auto Dice Roll Mini App</a>

Let's use the random library to create an automatic dice roller for a game of Monopoly!
In Monopoly, at the beginning of each turn a player rolls two six sided dice. The numbers rolled on each die are added together to tell the player how many spaces to move. If the player rolls doubles, if they roll the same value on each die, then they get to roll again. If they don’t roll doubles, its the next player’s turn.
 Every time we run our dice roller app, it will tell us how many spaces we should move, and if we have rolled doubles and get to go again, or it it is the next player’s turn.

# Conclusion:
There are many libraries out there we can import to add to our python coding power. Just take a look at the documentation to find out what cool functionality one will add to your script! We will be using import a lot when we talk about Google App Engine next week.
