---
  layout: post
  title: Javascript Objects Walkthrough
  language: javascript
---

## After the Lesson you'll be able to understand:
+ What is an object
+ object notation
+ key:value pairs
+ differences between arrays and objects

Remember when we talked about strings earlier today? Well it turns out that Strings are Objects. In fact, arrays are objects as well. Nearly everything in javascript is an object. Even a function is object in JS, though this is not true in many other languages.

Javascript is an object oriented programming language. Objects are the foundation of Object Oriented Programming. Consider all the hardware changes in the past 50 years: Memory once measured in kilobytes, expanded to megabytes, gigabytes and now terabytes.  The speed of computers and capabilities of graphics chips, based on smaller, more dense circuits, have marked the advances in hardware.  Yet in programming languages, there has been one major revolution: Objects.  C spawned C++, and now many widely used programming languages like Java, Objective-C, C# , Ruby, Python, and JavaScript all use Objects.

Everything can be described by Objects, which bundles properties, with methods or actions, and events that impact that Object.

Let’s learn about another data structure we can use besides our array, which is referred to as an Object and behaves like an associative array. That is, it creates a list of associated data pairs. Objects arrays do not have numbered indexes. Instead they contain key names and associated values. Where a numbered grocery list is a good metaphor for an array, a birthday list including a person’s name (key) and their birthday date(value) would be a better metaphor for an object.

It's like a list of pairs of things; or a list of stickers, each of which is stuck to something else. The syntax is different, too.

```
> var fruitColors = { "apple" : "red", "tangerine": "orange", "banana": "yellow"}
```

Each sticker/object pair, also called a key/value pair in computer science, is separated from the next by a comma.
And instead of looking up individual values with an index, we now can use the keys, or stickers.
```
> fruitColors["apple"]
You will get an error if you ask for something that doesn't exist.
> fruitColors["pear"]
```
Javascript also allows you to access the values by using a dot, similar to how you call a method. Try this:
```
> fruitColors.apple
```
Exercise: Now create an object with at least 4 associated pairs and assign it to a variable. What did you make?
