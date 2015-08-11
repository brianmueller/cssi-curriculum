---
  layout: post
  title: 4-cartoon-collections
  language: 
---


##  Objectives

You're going to get familiar with iterating through lists.

##  Instructions

There are three functions to complete in this lab:

1. Dwarf Roll Call
2. Summon Captain Planet
3. Long Planeteer Calls

####  Function 1 - Dwarf Roll Call

![dwarves](https://s3-us-west-2.amazonaws.com/web-dev-readme-photos/cartoon-collections/dwarves.jpg)

This function should accept a list of dwarf names, for instance:

```python
["Doc", "Dopey", "Bashful", "Grumpy"]
```

It should then print out each name using `print`. The print-out should look like this:

> 1. Doc
> 2. Dopey
> 3. Bashful
> 4. Grumpy

Look into [for loops](https://wiki.python.org/moin/ForLoop) and [enumerate()](https://docs.python.org/3/library/functions.html# enumerate)


####  Function 2 - Summon Captain Planet

![captain-planet](https://s3-us-west-2.amazonaws.com/web-dev-readme-photos/cartoon-collections/captain-planet.jpeg)

This function should accept a list of planeteer calls, like this:

```python
planeteer_calls = ["earth", "wind", "fire", "water", "heart"]
```

It should then capitalize each element and add an exclamation point at the end. The return value of this function should be a list. Example:

```python
summon_captain_planet(planeteer_calls)
# => ["Earth!", "Wind!", "Fire!", "Water!", "Heart!"]
```

The `map` function or list comprehensions might be appropriate for this task, take a look at them [here](http://www.dotnetperls.com/map) and [here](http://www.dotnetperls.com/list-python).


####  Function 3 - Long Planeteer Calls

The `long_planeteer_calls` function should accept a list of calls. The function should tell us if any of the calls are longer than four characters. For example:

```python
short_words = ["puff", "go", "two"]
long_planeteer_calls(short_words)
# => False

assorted_words = ["two", "go", "industrious", "bop"]
long_planeteer_calls(assorted_words)
# => True
```

Notice the return value of this function is either `False` or `True`, depending on the list it was given as an argument.

Checkout the [Python docs on lists](https://docs.python.org/3/tutorial/datastructures.html) for a hint.
