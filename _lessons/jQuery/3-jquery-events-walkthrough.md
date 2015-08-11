---
  layout: post
  title: 3-jquery-events-walkthrough
  language: jquery
---

#  Events, Listeners, and Handlers in JQuery
### What You Will Learns
+ Understand what constitutes an event
+ Attach jQuery event handlers (like 'click') to HTML elements
+ Add callback functions to event handlers
+ Use the $(this) selector in event handlers
+ Understand how to chain jQuery methods
+ Use the jQuery documentation as a resource

### Why This is Important / Why Should You Care?
What happens when you click a button on site? Can we make code that responds to user actions? What if we want something to turn blue when your mouse moves over it?

jQuery has event handlers that respond to user actions. This allows us to make all sorts of amazing behaviors and websites that respond naturally to user actions.

We've talked about dynamic web pages, where the user can interact with the page, but so far, all of the changes happen when the code is executed, not when a user does something. So, how do we tie the changes we want to make to some user action?

## JavaScript Events
In JavaScript, events are user actions such as mouse clicks, key presses, or window resizing. We can define code that will be run when those events happen.

JavaScript allows us to bind - or connect - functions to particular events. We create a function, and then tell the browser to run that function whenever that event happens. 

```
<body>
	<h1>Javascript Events</h1>
	<p>An event is an action a user does</p>
	<p>Use jQuery to "listen" to the event and respond to it</p>
	<p>Click on the header to see what happens</p>
</body>
```

jQuery lets us bind events with a concise, readable syntax. In the example below, lets pretend we wanted to do something everytime the user clicked on a header.

```js
$("h1").click(action);
```

* `$("h1")` - the *listener* - uses the selector syntax `$()` to get all the `<h1>` elements
* `click` - the *event* we are responding to
* `action` - the *handler* - or what we want our response to be

Javascript gives us a few different ways to create the 'action', by using a named method or using a callback function.

####  Named Methods as Event Handlers

We can define a named method. Then we can pass that method as a parameter when we call the event:

```js
  function tellUsWeClicked () {
	alert("You clicked a header");
}
    $("h1").click(tellUsWeClicked);
```    


####  Callback Functions as Event Handlers

We can also use an anonymous function: `function(){}` as the parameter. It's anonymous because we create it without giving it a name. The code for the function will go inbetween the curly brackets. This is a common pattern, called a callback function.

```js
    $("h1").click(function(){
        alert("You clicked a header");
    });
```
Especially if that function is not going to be used anywhere else, this style of coding makes it easy to read off exactly what will happen when the click event is triggered.

Regardless of which way we choose to include the handler, we need to remember to include our external jQuery library. Your code should be linked from an extenal.js file, but for this case, it is inside the `<head>` tags.

Notice that we need to include `$(document).ready` so that the page is ready to listen to events.
```
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script>
$(document).ready(function(){

    function tellUsWeClicked () {
	alert("You clicked a header");
	}
    $("h1").click(tellUsWeClicked);
});
</script>
</head>
```


## jQuery Mouseover Handler
Another popular even is mouseover(). The code defined in this handler will be run anytime the HTML element that we are listening to is hovered over.
Suppose we have HTML that looks like this
```
<!DOCTYPE html>
<html>
<head>
</head>
<body>

<h1>Proofreader</h1>
 <h2> Can you find the typo? Hover over it when you see it.</h2>
    <p>My very important mother just <span class="mispelled">cent</span> me nine pizzas.
      One was pepperoni, one was only cheese and one was a supreme.
      They were delicious!</p>

</body>
</html>
```
We could attach a mouseover handler so that code is run anytime the user hovers over the mispelled word.
```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script>
$(document).ready(function(){

  $(".mispelled").mouseover(function()
    {
      alert("Champion! You found it!");
    });

});
</script>
```


Be Careful!! The (), {}, and ; can look confusing, but if you count where they open and close, you can see which matches with which.


## Other Event handlers
jQuery can respond to a wide variety of Events which you should read about in the documentation. Some popular ones are:
+ Mouse clicks
+ Page load finishing
+ Moving the mouse over an element (often used for menu highlights)
+ Submitting an HTML form
+ Pressing the keyboard buttons
+ And MORE!!

## Document Ready as an Event
We often only want to run our javascript when the page has finished loading. Just like we can bind functions to events triggered by the user, we can run certain functions when the document is ready.
```
$( document ).ready(function() {
  // Here are all the functions that
  // will be run when the document is ready.
});
```
## $(this) inside Event callbacks
 $(this) allows you to easily access the element that fired the event.
For Example:

```js
  $("h1").click(function(){
        alert("You clicked a header");
        $(this).fadeOut();
  });
```

Here, the $(this) refers to the header that was just clicked.  After the user click on the header, an alert will pop up and then that header will fade out.

## Chaining Methods
Up until this point we've been writing jQuery statements one at a time. However, there's a convenient way to do multiple things to an element without writing so much code - you can chain multiple commands together.

For example, if we wanted an element to turn blue, and then move up and down we could write it this way:

```js
$(this).css("color", "blue");
$(this).slideUp(2000);
$(this).slideDown(2000);
```

This works, but we're repeating the lookup for the HTML element with the ID of stuff multiple times. 

Instead we can do this:

```js
$(this).css("color", "blue").slideUp(2000).slideDown(2000);
```

Here, we've chained the methods by simply adding the next one to the end of the chain.

## Conclusion / So What?
jQuery and other libraries allow you to do amazingly complex stuff with a simple function call. Any developer worth their salt will want to make a website that responds to the user. jQuery events let you do that.

Now it's time to explore events and event handlers! Try some of the jquery you've been learning to change elements and style when certain actions happen. [Here's a list](http://help.dottoro.com/larrqqck.php) of a ton of browser events that your code can listen for.

Some of the most common are 'click', 'scroll', 'mouseenter' and 'mouseleave', 'focus', 'blur',  and 'keyup'. There are lots and lots of events - what events do popular websites listen for and handle?
