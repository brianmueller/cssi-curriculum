---
  layout: post
  title: Arrays Walkthrough
  language: javascript
---

## Objectives:
+ What an array is
+ js array syntax
+ assigning an array to a variable
+ array indexing
+ how to locate and identify data in an array
+ how to change an array entry
+ calling methods on an array - finding the length of an array

We’ve learned how to store a piece of data in a variable.

```
>var student = "Tamara"
```

If we want to store a whole list of data, we need to make an array. Arrays are a type of data structure that creates an ordered list of individual elements.

One example of a real world array is a grocery list. Each item on the list has an index (number) and a element (food item). Another example would be a parking lot: each space is numbered (index) and contains a car (element).

You can visualize an array as a two-column table where the left column is the index (or the order) and the right column is the thing you’re listing:

| Index | Value     |
|-------|-----------|
| 0     | "Georgia" |
| 1     | "Norah"   |
| 2     | "Joseph"  |
| 3     | "Nicki"   |
| 4     | "Rob"     |

Notice that the index starts at 0. The first item in an array has index 0, the second has index 1, and so forth. The seventh person in a list would be index 6, the fiftieth would be index 49.

One way to think about this is that the computer counts indexes the way we count ages. We start at age '0' and only after our first full year do we turn '1'. In the same way, the first element gets index 0, and the second element gets index 1.

![example of array indexing](https://newcircle.com/static/bookshelf/ruby_tutorial/array_indexing.png)

We saw this same index numbering when we used methods to identify characters in a string earlier. In fact, you can think of a string like an array of characters.

###  Creating Arrays
An array can contain any combination of data types, strings, integers, floats, even other arrays.

You can create arrays using two different types of syntax.
* **The Good Way:** an array literal, uses square brackets `[]` : `var my_array = []`
```
var array1 = [1,3,5,7,9]      // an array with 5 elements
var array2 = [false,'CSSI',[2]]  // each element can be any datatype!
```

* **The Bad Way:** the Array constructor, uses `new Array` with parentheses `()`: `var my_array = newArray()

```
var array3 = new Array(2,'pickle',true,8,900)  // an array with 5 elements
var array4 = new Array(17)        // an empty array of length 17
var array6 = new Array()           // an empty array of length 0
```

Generally,  you should ALWAYS use the array literal with brackets when creating arrays.

###  Students Array
Let’s initialize an array of students:
```
>var students= ['Tamara','Georgia','Norah','Joseph','Nicki','Rob']
>students
["Tamara", "Georgia", "Norah", "Joseph", "Nicki", "Rob"]
```

You'll notice that we don't write the index of the elements anywhere. The computer automatically makes an index starting at 0 and incrementing by 1 for each element.

##  Accessing and Modifying Elements
To access an element, you need to call the name of the array and the index of that element.
```
>students[3]
< "Joseph"
```
Why did it return ‘Joseph’ ? Well Joseph is 4th name, but remember, indexing starts with 0.

```
students[0] is the first element
students[1] is the second element
students[2] is the third element
```

We talked about how to reassign variables earlier. What if we wanted to reassign an element in an array? What if Joseph dropped the class, and instead we had Barry?
```
>students[3] = 'Barry'
>students[3]
< "Barry"
```
The array element at index three has been changed!

Just like we got the length for our strings with a string method, we can also get the length of an array. Every array has a property that is it's length, which we can access with the '.'
```
>console.log(students.length);
```
This prints out '6' since our students array contains 6 elements. (Notice though that the last element of our array only has an index of '5', this will become important when discussing loops.)

## Add and Remove items from an array
We can also add and remove items from an array. Arrays actually have methods built in to them. Remember that methods are just a set of instructions.
```
names.push("Alfred")
```
`push` will add an item to the end of the array. In this case, the argument is "Alfred" and the array is names.

```
var lastName = names.pop()
```
`pop` will remove the last item in an array and return it. Since we just added "Alfred" to the end, that is what names.pop() returns.

Here are some other cool methods to experiment with: .sort(), .splice(), .split()
