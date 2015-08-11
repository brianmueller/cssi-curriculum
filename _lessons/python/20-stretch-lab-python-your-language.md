---
  layout: post
  title: Lab: Python Interpretation Challenge - Build Your Own Language
  language: python
---

When you type python my_program.py at the terminal, you're running a Python interpreter, that is, a program that understands Python and knows how to execute the code you wrote. Every programming language needs another program to translate it into something the computer's CPU can deal with.

For this challenge, you are going to write an interpreter for your own programming language, called "Pythonic" (from CSSI).

Read the [Norvig article](http://norvig.com/lispy.html) linked above. Read it again. This is the model we'll be following in this challenge. Read it a third time.
We'll start Cussy off with some simple math operations:

```python
4 + 5
8 * 2 + 1
1 - 1 - 1 - 1 - 1
8 / 0
```
For now, executing a math expression like one of those above should print out the result to the user. Math in Cussy should obey the standard order of operations. Once you get the basic ones, add more; Python's list is here. Add support for parenthesized math operations, so that 7 - 5 - 4 is different than 7 - (5 - 4). 3. Add logical operators like <, >, <=, >=, ==, and != to Cussy. These should yield values of True or False, like Python. 4. Add the ability to store the result of expressions to named variables and retrieve the value later. Code like this should now work:

```python
a = 4 + 5
a * a * a - 7
```
However, this should be an error, since the frobnicate variable isn't defined yet:

```python
4 + 8 * frobnicate
```
+ Add support for calling functions in Cussy. Start off by defining a built-in print function (this will be your only function so far):

```python
a = 4 + 5
print(a)
```
+ Next up: if statements. These should look like this. Don't worry about else for now.

```python
if (a < 5) {
    print(a)
}
```
Just like in Python, I should be able to do something like this:
```python

b = a < 5 if (b) { print(a) }
```
7. Now add the ability to define your own functions to Cussy. Start off easy and work your way up to more complex forms:

```python
function my_function() {
    return 55
}
```
and then
```python
function my_function(a) {
    return 55 + a
}
```
+ Your major goal here is to be able to write and run this Cussy code:

```python
function factorial(val) {
    if (val <= 1) {
        return 1
    }
    return val * factorial(val - 1)
}
result = factorial(10)
print(result)
```
