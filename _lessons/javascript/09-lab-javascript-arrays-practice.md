---
  layout: post
  title: JavaScript Arrays Practice
  language: javascript
---
# Arrays Practice Instructions:

# 1. Arrays:

Arrays are lists of elements, similar to a bookshelf that has slots to store different books (the elements) in a single shelf. Books can be fetched by identifying their position in the shelf (index).

*  To declare an empty array, we can use the following construct:

```javascript
var myArr = [];
```

*  If we know already what elements we want to store in the array, we can put them inside the brackets:

```javascript
var myArr2 = [element, anotherElement];
```

Elements can be strings, numbers, boolean, or even *undefined*. If you leave a blank spot in an array it creates a blank shelf space (undefined) placeholder. Keeping these characteristics in mind, make a new array, `myArr`, with four elements that will behave in the following ways:

```javascript
myArr[0]
  --> 'Hello'
myArr[1]
  --> undefined
myArr[2]
  --> 54.3
myArr[3]
  --> true
```

*  We can insert new values into any space in the array using the positions index. Change the undefined item in `myArr` to equal the string "Stuff" instead.

# 2. Overwriting:
We can overwrite all the elements of an array by assigning a new value to each of them. Or if we have two arrays, we can replace all elements of the first with those of the second in one statement, by assigning one array to the other.
*  Make an array called `fruits` where the four elements are these strings: Apples, Oranges, Pears, and Bananas.
*  Overwrite `myArr` so that its elements are the same as in `fruits`.

# 3. Retrieving the Total Number of Elements and Last Index:
*  Using the property `length` of myArr. Is the result the number you were expecting? Why? (Note how `length` is a property, not a method like those that we have seen for strings. Can you spot the difference?)
*  Keeping in mind the fact that indexes start with zero instead of one, get the last element's index position in `myArr`.
*  Make a variable "pos" and set it equal to the number you found in the step just above.
*  What should `myArr[pos]` return? Does it?

# 4. Array Insertion and Deletion:
We can insert on to the end of an Array simply by using the `push()` method.
*  Insert the string "Strawberries" into "myArr".
*  You can pull the last element off the end using the `pop()` method.
*  Call `pop` on "myArr". What will `myArr[myArr.length - 1]` return? Does it?
*  We can use [splice](http://www.w3schools.com/jsref/jsref_splice.asp) method to insert content at a given position or to remove content from a given position. Here is the syntax:
```javascript
arrayToModify.splice(index, how many elements to remove, optional content to add);
```
*  Add the string "Tiger" at index 2 without removing any elements. What do you think `myArr.length`; will return?
*  Let's say we needed to remove the second to last item, but we do not know how long the array is...We can use negative numbers to go to end of array and index from end to beginning.
*  Replace "Pears" with "Lion" using the negative index number, using the info above.
*  Now remove Lion from the 3rd index position using `splice`.
