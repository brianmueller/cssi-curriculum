---
  layout: post
  title: Intro to JavaScript and the Developer Console
  language: javascript
---
# What You Will Learn:
+ Understand and define key programming concepts
+ Use the JavaScript console
+ Understand the console is for testing, does not permanently store code
+ Use Arithmetic Operators in console
+ Use and concatenate strings in console

# Why This is Important:
JavaScript is what gives the web its "magic".  The most useful and interesting applications on the internet today are mostly all powered by JavaScript.


# Using the Console

We can play-around with JavaScript in the JavaScript Console. This is like a playground to experiment with JavaScript.

To get to the console, open chrome, and navigate to any webpage.  Press <kbd>command</kbd> + <kbd>option</kbd> + <kbd>J</kbd>

This gives you an area down at the bottom of the screen, called the console. The ">" symbol is called the prompt, where you can type JavaScript code.


# Simple interpretation
Try typing these lines, pressing enter after each one:

```
>4
>2+3
>2*3
```

Note that your friend the interpreter mostly just repeats what you say, but evaluates mathematical expressions. JavaScript performs basic math as you would expect, with the operators ` +, -, /, * .`  A less familiar operator is %, or modulo. See if you figure out what modulo does.

```
> 10 % 5
```

```
> 11 % 5
```

```
> 13 % 5
```

```
> 16 % 5
```

```
> 23 % 16
```

Here are some other mathematical operators:

| operator 	| name      	| description    	| usage         	|
|----------	|-----------	|----------------	|---------------	|
| -        	| negation  	| subtracts      	| 3 - 2 = 1     	|
| +        	| plus      	| adds           	| 3 + 2 = 5     	|
| *        	| multiply  	| multiplies     	| 3 * 2 = 6     	|
| /        	| divide    	| divides        	| 12 / 3 = 4    	|
| %        	| modulus   	| remainder      	| 12 % 5 = 2    	|
| ++       	| increment 	| increases by 1 	| x=1; x++; x=2 	|
| --       	| decrement 	| decreases by 1 	| x=1; x--; x=0   |


# Strings
So now we know we can do math in the  console. The interpreter will do things to pieces of text, too. In programming we call bits of text "strings".  

```
>"my string"
```

Note that you have to put text inside quotes before the interpreter can understand them. Anything between quotes is called a string.

Now try adding two strings together:

```
>"first name" + " last name"
```

Combining strings with the + operator is called concatenation.

JavaScript uses + symbol for math when it is operating on numbers, but when it sees strings, it will concatenate (link together) the text.

Let’s test this. Try entering these three different expressions:

```
>1 + 1
>”1” + “1”
>”1” + 1
```

1 + 1 is a mathematical expression adding two numbers, while “1” + “1” is an expression concatenating two strings of the character 1. If you try to add a string and a number, both pieces are treated as strings and concatenated into a bigger string.

Our code and the results as we use the JS Console are only there until we hit refresh. Think of the console as a place to test ideas quickly, not a place to build something that will endure for the ages.
