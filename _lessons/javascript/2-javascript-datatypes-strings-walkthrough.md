---
  layout: post
  title: Datatypes and String Methods
  language: javascript
---

## After the lesson, you'll be able to understand:
+ JS data types
+ Strings and string methods
  + length
  + upper and lower case
  + concatenation
  + charAt
+ String indexing

##  Data Types
In order to be useful to us, computers need to represent data that is meaningful to people. Underneath, though, all they can do is flip bits back and forth - all the data in a computer is just 1s and 0s, underneath. However, if you arrange 1s and 0s into certain patterns, you can interpret them as decimal numbers (the numbers we're familiar with), or letters and words, or sounds and pictures. Every machine you interact with is doing that type of interpretation all the time.

What does that mean for us programmers? When we want to do something meaningful with a computer, we have to tell the computer how we want it to treat our data - is that set of 1s and 0s supposed to be words? Or numbers? Or something else? Depending on the type of data we tell the computer to treat it as, we can instruct the computer to do different things with it.

JavaScript has a just a few different data types. We’ve played with two of them already - numbers and strings. Javascript recognizes numbers and strings when we write them - numbers it interprets as decimal numbers, and anything between double(" ") or single(' ') quotes is treated like a string. The rest will become more useful to us later on as we continue to code.

1. **Number**: 1, 3.14, 0.13, -100, …  
2. **String** (as in, a string of characters). examples include: "a", 'World Wide Web'
3. **Boolean**: Represents true or false
4. **Undefined**: has not been assigned a value, so the value is unknown
5. **Null**: This is a special keyword that means one of two things: no value or empty. The difference from undefined is that when a variable is null, it is still defined

##  String Methods and Properties
We've already seen what numbers can do - math operations, like addition, subtraction, and multiplication. Let’s play with our string data type. Let’s take one of our college variables that has a string for a value:
```
>var collegeText = "Intro to CS"
```
What if we want to learn more about the string in our variable? What if we want to control or change it with our code? We can call a method on our variable to do that. A method is a function attached to a piece of data. Often, it is a set of actions that can be performed on the data. When a method is called on a string, it modifies that string based on that set of actions. JavaScript has a number of built in methods that we can call on strings. The syntax for calling methods is dot notation, which looks like this:
```
variable.method()
```
Try calling these methods on your college variables:
```
>collegeText.toUpperCase()
>collegeText.toLowerCase()
```
The names of the methods tell you what actions they will perform.

Sometimes, there are multiple syntaxes that do the same thing.
```
> "one ".concat("two")
"one two"
>"one " + "two"
"one two"
```
When we add strings to each other, we stick one right on the end of the other. This is called concatenation, and we can do it with the .concat() method, or with the '+'.

ASK: Why do you think there would be different ways to do the same thing?

Now let’s try this:
```
>collegeText.charAt(1)
```
What did that method do? What do you notice?

You may notice that using the charAt(1) method returns the character in the string found at index 1. Are you surprised to find it returns the second character in your string? What if we wanted the method to return the first character?
```
>collegeText.charAt(0)
```
This returns the first character. In many programming languages, we start counting indexes from 0, so the first character in the string has an index value of 0.

You can make a new variable from the result of a function call.
```
> var bigColor = "pink".toUpperCase()
```
You can chain functions - call a function on the result of another function:
```
>"yellow".substring(0,4).toUpperCase()
```
You can combine these tricks. You can even store the resultant value in the same variable you started with!
```
> var lemonColor = "yellow"
> lemonColor
> lemonColor = lemonColor.toUpperCase()
> lemonColor
```
The key to understanding this mind trip is that the interpreter handles everything on the right side of the "=" before dealing with the left side.

We can also call a property on string to find out some valuable information about it, using the length property.
```
var lemonColor = "yellow"
> lemonColor.length
```
You can see since length is a property rather than a method, its notation does not include parenthesis () at the end.

**Challenge:**
Given the string  var text = "ELEPHANTBEARMOUSECOW" , make the 'MOUSE' portion into a lowercase 'mouse'.  Store the value back into 'text'.

Not sure how? Remember you can also search the web for documentation on js
string methods, talk to a classmate, or consult your ducky droid!
