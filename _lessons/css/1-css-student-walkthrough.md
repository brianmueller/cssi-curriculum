---
  layout: post
  title: CSS Student Walkthrough
  language: css
---
 
#### A Page with No Style

* Open up any page. Let's say `www.google.com`
* Right click on it and select "Inspect Element". You should see a whole bunch of HTML
* In the html `<head>` tag, you should see either a `<style>` tag or something like `link rel="stylesheet" type="text/css" href="mystyle.css">`. Delete that and watch what happens.

CSS is the "styling" for HTML pages. Think of HTML being like your body, and CSS being the clothes. Your clothes (CSS) make your body (HTML) look good. And without your clothes (CSS) your body (HTML) would look pretty naked.


#### Code-Along-Setup

Let's get set up to add CSS styling to your HTML page from the previous walkthrough

On your desktop create a new folder by going to the top right of your computer and clicking "File New Folder"
Rename the folder `my_profile_project`
Drag your `my_profile.html` file from the desktop into your `my_profile_project` folder
Click into your `my_profile_project` and your finder window should pop up
Create a new file called `style.css`

#### Selectors and Linking our Stylesheet
We write our CSS in a separate file  to seperate our style from our structure. Writing your CSS in a different file is called an external style sheet.

You can change the styling on entire website in one css file! Each html page must include a reference to that external style sheet though.

Copy and paste the `<link>` tag below into your my_profile.html page. It should be between the `<head>,</head>` tags

```
<head>
...other stuff...
     <link rel="stylesheet" type="text/css" href="style.css">
</head>
```

#### Selectors
Open your my_profile_project in Atom and click to edit your style.css file In style.css, let's make our `<h1>` tags a different color. To make `<h1>` the color red we use a type selector. First we write 'h1' because we want to select all `<h1>`s. The selectors go outside the curly braces. Then we want to change the color property to the value, red.  Property and value go between the curly braces. Colons and semicolons are important - they end our statements.
```
h1 {
 color: red;
}
```


The property-value pairs in between the curly braces {} are the styles (`color: blue` sets the text color to blue), and the selector defines (or “selects”) which elements these styles apply to.

#### Types of Selectors
There are three ways to select an element:
* Type selector: selects all of the elements by html tag
* Class selector: makes a class or a category that is associated with as many html elements
* ID selector: can only be used one time to grab a single element.

The first of these is a basic selector or type selector, and it’s composed of the name of the tag for which these styles apply. Using a basic selector the style rule applies to all elements of this type on the page.

A class selector selects all elements that have the class attribute defined to a given value. For example, .navigation selects all HTML elements that have an attribute class=navigation. Classes are not unique and there can be many elements with the same class name.

An id selector selects a particular element that has the id attribute defined to a given value. For example, # main selects the HTML element that has an attribute id=main. Each id should be unique in an HTML page; no two HTML elements should have the same id.



We’ll go the different types of selectors in more detail in an exercise.

####  Favorite Songs Example

##### Boiler Plate Code: Favorite Songs

Adding an HTML file In your my_profile_project folder create a new file called "favorite_songs.html" Open "favorite_songs.html" in Atom. Imagine you’re building a page with all your favorite playlists. Copy this boilerplate code:
```
<!DOCTYPE html>
<html>
  <head>
   <link rel="stylesheet" href="my_profile_project/favorite_songs_style.css">
    <title>My Playlists</title>
  </head>
  <body>
   <h1>Victoria's Playlists</h1>
   <h2>Workout Playlist</h2>
   <ul>
     <li>Break Free by Ariana Grande</li>
     <li>Do It Again by Robyn</li>
     <li>Shake It Off by Taylor Swift</li>
     <li>B.O.B. by OutKast</li>
   </ul>
   <h2>Bedtime Playlist</h2>
   <ul>
     <li>Such Great Heights by Iron &amp; Wine</li>
     <li>Passenger Seat by Death Cab for Cutie</li>
     <li>Wedding Song by Yeah Yeah Yeahs</li>
   </ul>
  </body>
</html>
```
This is what your html page should look like
Adding a CSS file We’ll define the CSS styles in a separate file. In your my_profile_project folder create a new file called favorite_songs_style.css Open favorite_songs_style.css in Atom Copy this boilerplate code
```
h2 {
 color: green;
}
```


Notice how both `<h2>` elements have a font color of green. That’s because the h2 selector selects all h2 elements on the page.

##### Change the Font: Let’s starting trying to make this page prettier. First of all, let’s change the font to something prettier, like Arial. This is specified by the font-family property.
We really want to change the font for all the text on the web page. How can we do that?
We could add rules for every element:
```
h1 {
 font-family: Arial;
}

h2 {
 color: green;
 font-family: Arial;
}

li {
 font-family: Arial;
}

```
This works, but it’s kind of annoying to have the write the same rule all the time. Plus, what if we wanted to change the font again? We’d have to update it in every place.
We have a couple of options on how to define the style more concisely. Combining selectors with comma You can combine selectors using a comma:
```
h1, h2, li {
 font-family: Arial;
}

h2 {
 color: green;
}
```

Notice the selector “h1, h2, li”: the comma is like an “and.” This rule says, apply “font-family: Arial;” to all h1s and all h2s and all lis. Note that you can still create other rules that reference the same element, and we see color: green is defined for h2.

It’s often very helpful to combine CSS selectors using comma, but actually in this scenario, it’s still a little annoying - what if we add a `<p>`element to the HTML:
```
<h1>Victoria's Playlists</h1>
 <p>Check out my playlists!</p>
```

We’d have to remember to add “p” to the list of selectors:
```
h1, h2, li, p {
 font-family: Arial;
}
```

This gets pretty annoying to remember to do as a page grows more complex with more elements. Inheriting styles Really we want to say, “All elements on this web page should have font-family: Arial.”
If we apply a style to the parent element, all of its descendants will inherit that style, if that style is inheritable. In general, text-related styles are inheritable, and layout-related styles are not.
We can then use this to our advantage to apply a style to parent element that contains all the elements we’d like to style in a certain way. In this case, the parent element containing every element on the page is the body element.
Change your CSS file to look like the following:
```
body {
 font-family: Arial;
}

h2 {
 color: green;
}
```

And you see that you get the desired result:
#### Colors
RGB vs Hexadecimal color There are a few ways to get more specific with color value other than just writing "red". There are many tones of red RGB- stands for Red, Green, Blue. RGB color model is the ways of getting different colors through adding different amounts of Red, Green, and Blue. Count up from 0 amounts of each to 255 of each rgb(0,0,0) gives you black rgb(255,255,255) gives you white Hexademical is a different notation for the amount of Red, Green, and Blue that gets added to your color. count: 0, 1, 2, 3, 4, 5, 6, 7, ,8, 9, a, b, c, d, e, f 6 values: two red, two green, two blue # 000000is black # ffffff is white # 0000FF is blue (zero amounts of red and green) Color Picker is a great resource to find other color tones

#### Fonts
Google fonts
Browsers can only display whatever fonts are downloaded on that computer. If a web application is using some random font that my computer doesn't have, I won't be able to see it. Google fonts is a great resource to get around this.  Click the quick view button
Scroll down the page till you see this and make sure import is selected: Copy that the @import url and paste it at the top of your CSS file Step 4 shows you how to use the font: They chose to style the font-weight property as well, you can ignore that
```
h1 {
   font-family: 'Metrophobic', Arial, serif;
 }
 ```
### Conclusion
Now you know how to add styling to your HTML pages. Use different types of selectors to change elements within your HTML page.

### Labs
Add CSS styling to your my_profile.html pages. Don't forget to reference your css stylesheet in the head of your HTML page using " reference to the external style sheet file. Copy and paste this into your my_profile.html page. It should be between the `<head>,</head>` tags
`<link rel="stylesheet" type="text/css" href="style.css">`


If you are finished try a stretch that is about the CSS box model: http://guyroutledge.github.io/box-model/


### Stretch Lab  
Use <div> tags and play around with [box model](http://guyroutledge.github.io/box-model)



##  Resources

* [W3 Schools- CSS ](http://www.w3schools.com/css)
