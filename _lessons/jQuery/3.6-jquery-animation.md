---
  layout: post
  title: Animation with jQuery and CSS
  language: jquery
---
One of the cooler features of jQuery is animation. The concept is pretty simple:

- You have an element with its current style
- You set a target style
- jquery gradually changes the style from one to the other

It turns out there is some somewhat complicated math for the values of the properties as they are changing, but you don’t have to worry about that at all. Instead, you describe to jQuery exactly how you want the animation to happen - how long it should take, and what rate the change should happen - and it figures all that out for you.


###  Animation using the animate() Method
The full syntax for the animate() method is below:

`$(selector).animate({params},speed,callback);`

* *params*  defines the CSS properties to be animated.

* *speed* is optional and  specifies the duration of the effect "slow", "fast", or milliseconds.

* *callback* is an optional function to be executed after the animation completes.

Here's an example:
```
$('p').animate(
    {fontSize: 24},
    1500
)
```
Over 1500 ms, the font-size in the paragraphs will change from whatever it was to 24.

####  Animation Shortcuts
There are also some convenient shortcut methods for common animations developers use all the time:
- .slideUp() - slide an element up a distance
- .slideDown()
- .fadeIn() - Show an element with a slow fade
- .fadeOut() - Fade out the element

Animation powers all kinds of nice-feeling web experiences - when a page has satisfying button clicks, when elements fade or slide (or both!) nicely onto and off the page - all excellent animation. Animation can be bad too - when the sliding is too slow, or the fades and slides in and out look cartoonish and silly.

As with color, font, position, whitespace, and design generally, there is far more depth to animation than we are going to cover. You can check out [this tutorial](http://www.sitepoint.com/guide-jquery-animate-method/) to learn more. As always, getting good takes practice.

Check the [documentation](https://api.jquery.com/category/effects/) for more examples and explanations.
