---
  layout: post
  title: Variables and Assignment 
  language: javascript
---
The interpreter has been great for doing little calculations like `2*3`, but it doesn't remember values from line to line.

To help it remember, we will need to make a variable.We can think of a variable like a bucket. Inside of the bucket we can store data. Variables will store data that we can access at any time.

To use a variable, you need to make a new name, and assign a value to it by using an '=' sign.

You need to declare variables explicitly in JavaScript with the var keyword like this:
```
>var students = 30
```
* `var` lets JavaScript know that you've just made a variable!
* The name of the variable is "students"
* The value assigned to students is 30.

Anytime we want to see what's inside the bucket, the value of a variable, we just need to call the variabe's name.
```
>students
30
```
If we reassign the variable, the value changes. We can change what’s in the bucket by putting something new in. Variables store data, and that data can be reassigned with the = sign.
```
>var instructors = 4
>instructors
4
>var instructors = 6
>instructors
6
```
Don't worry about the "undefined" you get from the "var" lines; the interpreter is just telling you that variable assignment itself doesn't evaluate to anything. It doesn't need to: the point is that the value is remembered for later.

We can put strings into variables:

```
> var cssi = "Google Computer Science Summer Institute"
> var description = "A program for awesome rising college freshmen"
> cssi
"Google Computer Science Summer Institute"
> description
"A program for awesome rising college freshmen"
```
And we can use the variables in expressions - they act as if the value stored inside them is in the expression instead:
```
> students + instructors
36
> cssi + " - " + description
"Google Computer Science Summer Institute - A program for awesome rising college freshmen"
```
We can assign variables to the results of expressions too:
```
>var humansInRoom= students + instructors
>var info = cssi + " - " + description
>humansInRoom
36
>info
"Google Computer Science Summer Institute - A program for awesome rising college freshmen"
```

Note that variable names are case-sensitive, which means capital letters matter.
```
>info
"Google Computer Science Summer Institute - A program for awesome rising college freshmen"
>Info
ERROR!!
```
javascript thinks that 'info' and 'Info' are different things - the capitalized one is not defined!

Our variable names should be specific and relevant to so that it is easy for other developers to understand what goes inside.
```
var x = 30; // pretty unintelligible
var number = 30; // what does the number mean?
var studentCount = 30; // this one is pretty clear!
```
For variable names consisting of multiple words, we can use camelCase or snake_case. Usually, javascript developers use camelCase (called camelCase  becauseTheLettersMakeHumpsInTheName). In python, developers like snake_case (which sorta looks like a snake, if you squint.) snake_case is slightly easier to read, but it's most important to follow the established conventions, and especially to be consistent within a project. That way, other programmers can look at a word and tell in an instant whether it is a variable, or something else!
