---
  layout: post
  title: 4-python-lists-loops-walkthrough
  language: python
---
---
tags: cssi, lists, loops
level: 2
languages: python
---
# Python Lists and Loops

# What You Will Learns:
+ Create a list in python syntax
+ Create a loop in python syntax

# Why This is Important:
When we learned Javascript, we raced through lots of techniques programmers use to represent and manipulate data. We learned arrays, conditionals, looping, functions, and objects really quickly, and we used them to do interesting things to webpages.

Most of the techniques, though, don't only apply to javascript. Just like we can use the python interpreter like the javascript console, and just like we can do basic arithmetic and string operations in both languages, we can use python logic to solve problems. We'll look at the most frequently used data structures and techniques, and use them to tackle some interesting challenges.

# Lists
A list is the most basic python data structure. It is a list of objects or values. The syntax for a list is a set of objects enclosed in brackets. To create an empty list, set a variable equal to empty brackets:
```
>>> empty_list = []
```
To create a list with some elements in it, just add the elements separated by commas:
```
>>> groceries = ['Eggs', 'Milk','Butter']
```
Accessing items in a list
List items have an index and are accessed like they were in javascript. Remember, that the 1st element has an index of 0

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
# Student Practice: Lists
What would this print? Why?
```
>>> groceries[0][3]
```
`groceries[0]` would first access the first element of the groceries list, 'Eggs'. Adding the second index, `groceries [0][3]` would then grab the 4th character in 'Eggs', the 's'.


# Modifying a List
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

# List Methods
Using the len function, you can return the number of items in a list:
```
>>> print len(groceries)
3
```
Here are some other list methods that will come in handy:
```
## extend() adds multiple elements to a list
groceries.extend(['Rutabaga', 'Ice Cream'])
['Bread', 'Milk', 'Butter', 'Asparagus','Rutabaga', 'Ice Cream']

##  del() removes the element at that index
del groceries[3]
['Bread', 'Milk', 'Butter','Rutabaga', 'Ice Cream']

##  remove() removes the element that matches the string
groceries.remove('Rutabaga')
['Bread','Milk','Butter','Ice Cream']

##  .sort sorts alphabetically
groceries.sort()
['Bread', 'Butter', 'Ice Cream', 'Milk']
```

#  'In' and 'Not' Operator
What if you have a list of groceries and you want to check if ‘apples’ is in that list? Or a list of names and you want to check to see if someone is present? Use the 'in' operator.
```
if 'albert' in students:
 print 'good, albert is here'
else:
 print 'gosh, where is albert?!'
```
To check if an element is absent from a list, use the 'not' in operator:
```
if 'albert' not in students:
 print 'where is albert?!'
```

# range(): building lists of numbers easily
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
Computers, as we've been learning, aren't that clever. However, they can do simple things really really fast. It makes sense that some of the most powerful things we do with computers, we do in a loop. Loops let us repeat a section of code over and over, even if we only type it out once. In javascript, we saw how to use loops to iterate through an array. We can do the same thing in python, stepping through each element in a list and doing something with it.



# For Loops
The simplest looping situation is where you need to do something _for_ a certain number of times. To do this, Python uses a for loop.

##  Example 1: Looping Through a List


This code will repeat for every element in the list.

```python
for name in ["Lucy", "Riccardo", "Ricky Jr."]:
	    print name
```
Note that the variable `name` is what we are calling each element within the list. We could call that variable anything: `character`, `person`, `actor`. It doesn't matter, as long as we continue to use that variable later within the _for_ block.

Alternatively, we can declare a variable `names` which contains a list of our lovely characters, and then use the same syntax.
```
# same result, slightly different syntax

	names = ["Lucy", "Riccardo", "Ricky Jr."]:
	for name in names:
	    print name
```
##  Example 2: Looping through Integers

The _for_ loop syntax is similar for integers. 
* Notice that in this example we also used string interpolation. 
* This code will repeat for every integer in the range.
```
for i in range(1, 4):
    print "I am looping and am currently on %d." % i

# again, you can also declare your variable before the loop
my_range = range(1,4)    
for i in my_range:
    print "I am looping and am currently on %d." % i    
```
# While Loops
While loops continue to repeat _while_ - or as long as - a certain condition is met. A while loop has a block of code and a condition.
###  Example 1: A Simple While Loop
This code will repeat while the condition `n<5` is met. It will stop when n is equal to 5.

```
n = 0		
while n < 5:	
   print n
   n = n + 1	
```
###  Example 2: A While/Else Loop
This code is similar to the first _while_ loop example, except that there is an `else` statement. Once the condition `n<5` is not met, the instructions in the `else` block are executed. Then, the entire _while_ loop is exited, and the next instruction (to print `"You counted to 5"`) is executed.
```
n = 0
while n < 5:
   print n, " is  less than 5"
   n = n + 1
else:
   print n, " is not less than 5"
   
print "You counted to 5"
```   

##  Extended Loop Examples

###  For Loops
The simplest looping situation is where you need to do something once for every item in a list. To do this, Python uses a for loop:

```
my_string = raw_input('Type something: ')

for word in my_string.split(): # returns individual words in a string
   print word.upper()

for letter in my_string:
   print letter.upper()
```
####  Nested For Loops
You can even put one loop inside another:

```
my_string = 'hello world'

for word in my_string.split():  #  Loop 1
   for letter in word:         #  Loop 2
       print letter.upper()
```

Everything indented inside Loop 1 is run every time through the loop -- including Loop 2!

####  Conditionals and For Loops
Now let's make it more complex.

Let's say you hand me a sack of apples, and you bet me $5 that I can't eat every apple in the sack. It doesn't really matter how many apples are in the sack: I have to eat them all, so I'm just going to concentrate on eating them one at a time.

If I were a soulless robot, my thought process would look something like this:

```
sack_of_apples = GetApples()

ate_all_the_apples = True

for apple in sack_of_apples:
    EatApple(apple)  #  Crunch, crunch!
    if TooSickToEatMore():
   	 #  Ugh, maybe that wasn't a good idea.
   	 ate_all_the_apples = False
   	 break

if ate_all_the_apples:
    print 'Gimme my five bucks!'
else:
    print 'Please cart me to the hospital'
```
####  The range() function
You can use the range() function above to loop over the number of items in a list. Note that range() returns integers, so that song_num are integers. 
```
music_collection = GetSongs()

for song_num in range(len(music_collection)):
   print 'Song', song_num, 'is', music_collection[song_num]
```
 
###  While loops
Where for loops let you loop over a finite collection of things, while loops let you keep looping until a given condition evaluates to true.

Let's modify the wager we made earlier. Rather than betting me $5 that I can eat every apple in the sack, here's the deal: if I can eat more than five apples, I get $5; if I can eat 10 apples, I get $10; and for every apple over 10 that I eat, I get an extra $2.


```
apples_eaten = 0
while not TooSickToEatMoreApples():
    apple = TakeOneApple()
    EatApple(apple)
    apples_eaten += 1


#  Figure out how much I owe you.
if apples_eaten == 0:
    print 'Aww, you didn\'t even try.'

elif apples_eaten < 5:
    print 'Nope, not enough apples. No money for you.'

elif 5 <= apples_eaten < 10:
    print 'Fine, here\'s your $5.'

elif apples_eaten >= 10:
    winnings = 10 + (apples_eaten - 10) * 2
    print 'Looks like I owe you', winnings, 'dollars.'
```

Since there's no limit on the number of apples I could eat, other than the size of my stomach, I use a while loop and keep eating until I don't feel well. As I go, I keep track of how many apples I ate so I can send you a bill (which likely won't cover the visit to the ER).



# Conclusion
Creating, modifying and accessing lists are imporatant for every programmer, as is being able to use _for_ loops and _while_ loops. Practicing these small examples are a great way to build your foundation as a strong developer.
