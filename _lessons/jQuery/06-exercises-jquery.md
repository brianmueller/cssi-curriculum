---
  layout: post
  title: jQuery Review Drills
  language: jquery
---

##  Instructions:
Fork and clone this lab, then complete the drills below.

###  1. Selector Drills

Given the following HTML page:
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-git.js"></script>
    <title>Fruits</title>
  </head>
  <body>
    <h1>Fruits</h1>
    <h2 class="div">Orange</h2>
    <div>
      <p>Cherry</p>
      <p id="h2">Banana</p>
    </div>
  </body>
</html>
```
What would be the output of the following jQuery commands?

```javascript
$('h1').text();
```

```javascript
$('h2').text();
```

```javascript
$('# h2').text();
```

```javascript
$('.div').text();
```

```javascript
$('# div').text();
```

```javascript
$(div).text();
```

Make your guesses before running the code. You can check your answers by opening http://jsbin.com, copying the HTML into the HTML tab, and copying the jQuery commands into the Console tab.

###  2. Manipulating the DOM

Given the following HTML page:
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-git.js"></script>
    <script src="animals-script.js"></script>
    <title>SPIRIT ANIMAL</title>
  </head>
  <body>
    <h1>My spirit animal is a:</h1>
    <div id="favorite">bunny</div>
  </body>
</html>
```

Write JavaScript to do the following:

1. Log the contents of the ```div``` to the console.
2. Change the text content of the ```div``` to be "bear" instead of "bunny"
3. Change the content of the ```div``` to show this picture of a bear instead of text: http://i.imgur.com/SHxgKJv.png

The HTML file and JavaScript stub file are available in this git repository in the directory ```animals```. Put your JavaScript in ```animals-script.js``` and load ```animals.html``` to test your answers.

###  3. Event Handlers
Open the contents of ```cookies/cookies.html``` in Chrome. You should see something like:
![cookie monster lab](http://i.imgur.com/NMHh8mCl.jpg "Cookie Monster Lab")

Modify ```cookies-script.js``` and ```cookies.html``` to accomplish the following:

1. Log a message "Baking a cookie" to the console when the "BAKE a cookie" button is clicked.
2. Implement "BAKE a cookie": Insert an image with source cookie.png into the div with id="plate" when the "BAKE a cookie" button is clicked. You should be able to add multiple cookies into the div.
3. Implement "EAT ALL the cookies": Remove all the cookies from the pink plate when "EAT ALL the cookies" button is clicked.
4. Implement "EAT a cookie": Remove a single cookie from the pink plate when the  "EAT a cookie" button is clicked.

###  4. Code reading: Forms and Event handlers
Remember the form in the Deli Counter lab? Now you've learned enough to understand the contents of the ```index.html``` and ```lib/app.js``` file!

Take some time to look through those files again and describe in English how it works to your neighbor:
https://github.com/learn-co-students/js-deli-counter-google-cssi-test-2015

###  5. Coding: Forms and Event Handlers
Open the contents of ```todo/todo.html``` in Chrome. You should see something like:
![todo lab](http://i.imgur.com/5yCxP8ul.png "To-Do List Lab")

Modify ```todo-script.js``` and ```todo.html``` to accomplish the following:

1. Log the contents of the text input when the "Add" button is clicked.
2. Implement "Add": Insert the contents of the text input at the end of the ol list when the "Add" button is clicked. Clear the contents of the text input when this happens.
3. Implement "Submit on enter": Pressing enter while focused on the text  box should trigger the same behavior as clicking the "Add" button.
4. **EXTRA CREDIT** *Warning: These are both quite tricky due to some jQuery quirks. Only proceed if you're VERY comfortable with everything we've done so far - and comfortable using Google for help!*
  *  Implement "Cross off": Clicking each list item should cross the item off the list by making it appear with a ~~strike~~ through it.
  *  Implement "Delete": Add a "Delete" button next to every item of the list. Clicking this button should remove the item from the list.

###  6. An Annoying JS Bug

Given the following ```wontwork.html``` page:
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-git.js"></script>
    <script src="wontwork-script.js"></script>
    <title>Weather Report</title>
  </head>
  <body>
    <h1 id="weather">Rainy :(</h1>
  </body>
</html>
```

And the following ```wontwork-script.js``` file:
```javascript
function magicWand() {
  $('# weather').text('Sunny!');
}
magicWand();
```

Answer the following questions:

1. When you load ```wontwork.html```, what appears in the ```h1```: "Sunny!" or "Rainy :("? Why?
2. Modifying only ```wontwork-script.js```, how do you fix this bug?

The HTML file and JavaScript stub file are available in this git repository in the directory ```wontwork```.
