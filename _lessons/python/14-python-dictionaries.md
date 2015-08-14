---
  layout: post
  title: Python Dictionaries
  language: python
---
# What You Need to Know:
+ Basic Python syntax

# What You Will Learn:
+ Understand the syntax of dictionaries in Python
+ Compare the differences of dictionaries and lists

# Why This is Important:
Lists let us group data in order. Dictionaries hold a set of paired keys and values - another way to keep data. Programmers use dictionaries all the time, because lots of problems are easier to solve when pieces of data are associated with each other.

# Dictionaries
When you open up a real-world dictionary, what do you see? Words and their definitions. Python dictionaries are like that too - they contain pairs of keys (words) and values (definitions). They make it easy to look up a value (definition) by its key (word).

Dictionaries are like lists - they store data - but instead of having numbers as indexes, the indexes are the keys you define - usually strings. Check it out:

<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-4.10-python-dictionaries/master/images/dictionary.png">

In this example, we associate each of the items on our grocery list with its price. We don't really care about the order of the grocery list - it is way more helpful to know how much each item will cost!

Think of keys like the words in a dictionary and the values as the definitions. A dictionary holds pairs of keys and values. A key in a dictionary must be unique and associated with a value.

How do we use them? The python syntax for declaring a dictionary is with {curly brackets}. To create an empty dictionary, just set a variable equal to curly braces:

```python
empty_dict = {}
```

To create a dictionary with values in it, set key-value pairs separated by colons and commas:

```python
my_cart = {'Eggs': 2.59,
'Milk': 3.19,
'Cheese': 4.80,
'Yogurt': 1.35,
'Butter': 2.59,
'More Cheese':6.19 }
```

# Accessing values in dictionary
We get the values out of the dictionary much like we got values out of lists. In order to access the values of a dictionary, you want to pass the key to the dictionary and it will return the value.

```python
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}

print cartoon_species['elmer']
```

# Updating a dictionary
To modify the values inside a dictionary, the same thing applies - you want to use the assignment operator and send it the key value.

```python
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}

cartoon_species['bugs'] = 'bunny' # reassigns rabbit to bunny
```

You can also use this technique to add key-value pairs to a dictionary that don’t already exist. For instance, with my_dict, I could do the following:

```python
cartoon_species['tweety'] = ‘bird’
print cartoon_species

{'tom': 'cat', 'wiley e': 'coyote', 'elmer': 'human', 'bugs': 'bunny', 'jerry': 'mouse', 'tweety': 'bird'}
```
The {"tweety": "bird"} key value pair has now been added to my_dict.

# Common Dictionary Operations

```python
len(my_dict)
5

my_dict.clear()
{}

del my_dict['bugs']
{‘elmer’: ‘human’,
‘wiley e’: ‘coyote’,
‘tom’: ‘cat’,
‘jerry’: ‘mouse’}
```

## Key-Value Pairs
Key-value pairs are separated by commas

```python
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}
```

***Keys*** are on the left of the colons (‘bugs’, ‘elmer’, ‘wiley’, ‘tomas’, ‘jerry’)
***Values*** are on the right of the colons (‘rabbit’,‘human’,‘coyote’,‘cat’, ‘mouse’)

Keys must be unique, otherwise the program will throw an error. The same word doesn't appear in a dictionary more than once!

```python
my_dict = {'bugs': 'rabbit',
      	'bugs': 'non-rabbit' # Doesn't make sense
      }
```

It doesn't make sense to have two different values for the same key - one will get overwritten.

Keys are usually strings, because they are easier to read, but they can be other data types too.  Values can be any data type - strings, numbers, lists, or even other dictionaries!

With strings as values:

```python
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}
```

A dictionary with list values:

```python
cartoon_friends = {'bugs': ['daffy','porky', 'foghorn leghorn'],
                   'mickey': ['minnie', 'goofy', 'donald'],
                   'woody': ['buzz', 'rex', 'slinky'],}
```

dictionary with other dictionaries as values:

```python
cartoon_relationships = {'friends' : cartoon_friends,
                         'species' : cartoon_species }
```

# Searching for a Key in a Dictionary
What if you wanted to check if the key 'jerry' was in my_dict?  Use the in operator.

```python
if 'jerry' in cartoon_species:
 print 'Hi Jerry!'
```
This only works for keys in a dictionary, not the values.

# Looping through a dictionary
It is often useful to be able to loop over the contents of a dictionary. Using the for-in loop we would write:

```python
for cartoon in cartoon_species:
 print cartoon
```

What do you notice? What is it printing? It’s printing the keys!

```python
bugs
elmer
wiley e
tom
jerry
```

How would you print the values? Combine the technique of accessing the dictionary through the key:

```python
for cartoon in cartoon_species:
 print cartoon_species[cartoon]
```

This prints:

```python
rabbit
human
coyote
cat
mouse
```

# Conclusion:
Dictionaries are phenomenally useful tools for representing all kinds of data. They are similar to lists but rather than having and index (0,1,2,3) you have keys for each value!
