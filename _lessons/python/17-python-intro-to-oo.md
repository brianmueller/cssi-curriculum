---
  layout: post
  title: Python Objects and Classes
  language: python
---
# What You Need to Know:
+ Command-line Basics
+ Python Basics and Syntax

# What You Will Learn:
+ Python Syntax for Classes
+ Using instance variables and class methods

# Why This is Important:
As a programmer you have different design choices you can make for structuring your code. Object Orientation is a way to organize, manipulate and store your data. It’s a design pattern that provides a way of building new objects - say all the alien enemies in a video game, Sim people in The Sims, cars in Grand Theft Auto, users of Facebook - by making programs that are "factories" that standardize how the objects are made.

To generate new instances(versions) of an object we create something called a Class. The Class allows us to create a template for the objects we want to make. The template can then be tailored without having to recreate all of the code for each new instance of the object. Class syntax will give us a new way to organize and write our programs.

## Creating A Class
A class has this basic structure:
```python
class ClassName:
  'Optional documentation'
  class_suite
```
+ A class includes a **class statement** defining the name of the class, followed by the stuff that defines the attributes and actions of the members of that class - **methods** and **arguments**.
+ Class names should always be capitalized. When the name includes two words, the second word should also be capitalized.

Here is a class that will allow us to create Musician objects.

```python
class Musician(object):

    """A class that creates awesome musicians!"""

    def __init__ (self, name, genre):
        self.name = name
        self.genre = genre
```

+ class statement establishing a new class called Musician
+ members of the class Musician are defined with the __init__() method, whose first argument is self, followed by whatever additional arguments you choose.
+ within the __init__() we have our instance variables assigning our arguments.

Now we have our blueprint for our Musician.

You can make many instances of Musician.
For example:

```python
beyonce = Musician('Beyonce' , 'R&B')
```

We can make as many instances of Musician as we want. They’ll all be added to our class of Musicians.

**Arguments** that we add to our class, like name and genre, are descriptors that allow us to add more data to the objects. We can create any sort of argument we want.

**Methods** we add to the class provide actions for our objects to execute.

## Adding Methods:
+ Here we add a new argument and a method that will describe an instance of musician for us.

```python
class Musician(object):

    def __init__(self, name, genre, fav_album):
        self.name = name
        self.genre = genre
        self.fav_album = fav_album

    def description(self):
        print "Hey, my name is {0}, I make {1} music. Check out my album {2}." .format(self.name, self.genre, self.fav_album)

kanye = Musician('Kanye', 'Rap', 'Yeezus')
```

+ We can call that method to get that description.

```python
kanye.description()
```

+ We can add another that tells us if the musician is currently recording. We’ll need a new method and a new argument for our object that has a boolean value:

```python
class Musician(object):

    def __init__(self, name, genre, fav_album, recording):
        self.name = name
        self.genre = genre
        self.fav_album = fav_album
        self.recording = recording

    def description(self):
        print "Hey, my name is {0}, I make {1} music. Check out my album {2}." .format(self.name, self.genre, self.fav_album)

    def is_in_studio(self):
        if self.recording:
            print "Yo, I'm in the studio recording some fresh tracks! Holla at me later!"
        else:
            print "Hoping to get in the studio soon, I know you've been wanting new material!"

kanye = Musician('Kanye', 'Rap', 'Yeezus', False)

```

+ We can call our new method on our instance:

```python
kanye.is_in_studio()
```

# Exercise: SpaceShip Class
1. Write your own class that will create space ships. What arguments will you use to describe each one of your space ships? Add at least 3 to your class, then use the class to create 2 different instances of your space ship.

2. What can your space ship do? Add a method to your space ship class that defines an action for the space ship to execute. Create a new instance of your space ship. Print the method for your new instance.

# Conclusions
As you can see, there is more than one way of designing your code. There is a lot more that can be learned about Classes and the advantages that working within this structure can provide, if you are interested you can continue learning about Object Orientation on your [own](https://docs.python.org/2/tutorial/classes.html). For now, familiarity with class structure for Python will be useful to us next week when we get into learning AppEngine. We’ll work with Python classes again there.
