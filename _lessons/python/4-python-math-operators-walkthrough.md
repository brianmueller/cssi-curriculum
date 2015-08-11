---
  layout: post
  title: Python Math Operations Walkthrough
  language: python
---

# Objectives:

+ Understand how math operators are used in python
+ Understand the order of operations in python

# Motivation
Like we saw when we were exploring the interpreter, Python supports the basic math operators you would expect ``(+, -, *, /)``  Anytime we see an equation in code, python will try to evaluate the expression.


#  Decimals or Floats
There are some caveats about fractions and decimals numbers. Sometimes you'd expect one thing, but python gives you another.
```
>>> 5/2
2
```
What? Why is that happening? Shouldn't it be 2.5? Python treats some numbers as if fractions didn't exist. It doesn't even round! Why is this? I thought computers were supposed to be good at math!?!
```
>>> 5.0/2.0
2.5
```
It turns out that python is trying to be your friend - when you give it integers, it wants to give you integers right back. When it gets a **decimal or float** it returns a decimal/float.

However, if we were cutting slices of a cake, that would be a whole different story. We shouldn't let any piece of cake go to waste, and most people are fine with fractional slices of cake. What can we do to make sure that when we divide our cake among all the students, we get some and not 0?

This doesn't work:
```
>>> cake = 1
>>> students = 35
>>> slice_size = cake / students
>>> slice_size
0
```
NOOOOO! We have to do something!

# Student Practice: Decimals and Floats
If we only have one cake, what would you place in the cake variable so that python returns a decimal or float?
```
>>> cake = ??
>>> students = 35
>>> slice_size = cake / students
```
Now, we are putting a float in and getting a float out.  It's a floating point number - it works like the Real numbers you use in your algebra and calculus classes.

# Modulo %
% is the remainder operator. When you divide a number, how many are left over?
```
>>> 1 % 3
1
>>> 2 % 3
2
>>> 3 % 3
0
```
# Student Practice:

Try these operations in your python interpreter:
```
>>> 4 % 3

>>> 10 % 3

>>> 19 % 16
```
Write a math operation that include integers and floats and output the following answers:
```
>>> Your code using an integer goes here
2
>>> Your code using a float goes here
2.5
>>> Your code using a % goes here
3

```
