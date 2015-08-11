---
  layout: post
  title: Python Objects and Classes
  language: python
---

## Creating A Class
A class has this basic structure:
```python
class ClassName:
  'Optional documentation'
  class_suite
```
+ A class includes a **class statement** defining the name of the class, followed by the stuff that defines the attributes and actions of the members of that class - **methods** and **arguments**.
+ Class names should always be capitalized.


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

**Arguments** we choose to add to our class, like name and genre, are descriptors that allow us to add more data to our objects, the methods we add to the class provide actions for our objects to execute.

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
            print "Hoping to get in the studio soon, I know you are jonesing for new material!"

kanye = Musician('Kanye', 'Rap', 'Yeezus', False)

```

+ We can call our new method on our instance:

```python
kanye.is_in_studio()
```
