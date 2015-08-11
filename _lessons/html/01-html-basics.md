---
layout: post
title:  Intro to HTML
date:   2015-08-04 11:56:31
categories: day-1 html frontend
language: html
---
## What you need to know:
+ How to make a Github repo
+ Commandline basics

## What you will Learn:
  + How the web works
  + Structure an html page
  + How to use HTML tags and attributes
  + Using tags to add text, images, and links
  + Understand relative and absolute paths
  + How to use paragraph tags and bold and italicize font
  + Understand tag nesting
  + Make comments
  + Understand how the browser reads whitespace in HTML

## Why this is important:
How many times a day do you use the internet? How many times do you load a different web page? I bet you can't even begin to guess how many times in a year! In order to be a developer, and especially a web developer, it's incredibly important to understand how the web works.

HTML is the foundational technology for the Internet, every one of your favorite websites is HTML at its core. Today you are going to learn how to create an HTML site from scratch. And create your own styles for your personal web page.


## Intro to the Web
A web page is a text file written in a language that your browser (a program like Chrome or Firefox) knows how to read and turn into the page you see.  Often, it tells your browser to find other files, like pictures, that belong on the page. Sometimes it also tells the browser to find files with more code, which the browser uses to change the page. Before we talk about how we can write files that the browser can read, lets talk about where the browser gets web pages from, and how.

In talking about the internet, we use a metaphor of clients and servers - it helps us form a mental image of what is happening. Your browser is called the client, and the client makes requests of the server, to which the server responds. A server is just another computer, which your computer communicates with. Most of the requests that your browser makes are "GET" requests - your browser wants to get a page. A GET request is a request to load information. Once the server receives our request, they send back a response, which has the files needed for the page.

As you can tell, we are talking about how this happens in abstract, high-level terms. You can spend years studying the fine detail of how the internet works. After making sure we have everything set up right, we'll get started with some core internet technologies - HTML and CSS.


## Set Up Directions

In Terminal:

1. `cd ~/cssi`: Go to your `~/cssi folder`
  + If that folder doesn't exist create it with `mkdir ~/cssi` then go there using `cd ~/cssi`
2. `mkdir html`: Make a folder called `html`
3. `cd html`: Navigate into the `html` folder
4. `touch practice.html`: Create a `practice.html` file in your `html` folder
5. `atom practice.html`: Open `practice.html` with the Atom text editor
6. Copy the boiler plate code below into `practice.html` and save the file
7. `open practice.html`: Open the file with the default program (Chrome)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Web Page</title>
  </head>
  <body>
    Hello, world!
  </body>
</html>
```

## Tag syntax
HTML is made up of building blocks called "elements".
```
<tag> .... CONTENT GOES HERE .... </tag>
```
## Attributes
Attribute: Different elements can have different attributes. All elements can have class and id attributes to help differentiate them from other elements.

```
<h1 id="song-title">"Halo"</h1>
<p class="beyonce-lyrics">Remember those walls I built? Well, baby they're tumbling down And they didn't even put up a fight They didn't even make a sound I found a way to let you in But, I never really had a doubt Standing in the light of your halo I got my angel now</p>
```
+ ID - identifies a unique element on the page and there can only be one element that has that id.
+ Class- Identifies and group elements that may occur more than once.

##Types of Tags:
+ Headers  
Headers tell your visitors what your site is about. Usually, the main title of pages uses the `<h1>` tag.

Netflix might use headers like this:
```
<!DOCTYPE html>
 <body>
   <h1>Netflix</h1>
   <h2>Top Picks For You</h2>
   <!-- your top picks would be here! --> 
  <h3>TV Shows</h3>
   <!-- TV Shows would be here! -->
   <h3>Comedies</h3> 
  <!-- Comedies here! -->
   <h3>Horror</h3>
   <!-- Horror Movies here! --> 
</body>
```

+ Paragraphs and Emphasis
	1.	`<p>` tags, delineate paragraph text
	2.	`<strong>` will make any text contained within bold
	3.	`<em>` will italicize text or add emphasis

+ Lists
	1.	Bullet point lists start with `<ul>` for unordered list
	2.	Numbered lists start with `<ol>` for ordered list
	3.	The actual list items go between `<li>` tags for, you guessed it, list items

```
<ul>
   <li>item with bullet point</li>
   <li>2nd item with bullet point</li>
   <li>another list item</li> 
</ul>

  <ol>
   <li>Numbered item</li> 
  <li>List item #2</li> 
  <li>Third list item</li>
 </ol>
```
+ Links  
Links use an `<a>` tag, which stands for anchor. If you wanted a link to Google it would look like this:
`<a href="http://www.google.com">Super secret link</a>`

+ Images  
Images use an `<img>` tag to embed an image in a webpage.
`<img src="your_image_location">`

## Absolute or Relative paths


## Indentation
HTML is not the easiest to read. It's designed to be clear for the browser to understand, but not always for humans. Indentation help make your code easier to understand and debug.

No indentation:
```
<html><head><title>The end of the world as we know it</title>
</head><body><p>
Some text about things</p></body>
```
This is confusing to read, and makes it harder to find errors. Can you spot the missing tag?

Indentation:
```
<html>
  <head>
    <title>
      The end of the world as we know it
    </title>
  </head>
  <body>
    <p>
      Some text about things
    </p>
  </body>
```
With better indentation, the missing tag is easy to spot!

## Comments

HTML also has a way to write things that won't show up in the browser at all. That doesn't sound very useful at first, but developers use this invisible text to leave helpful comments in the code.

HTML comments look like this:
```
<!-- Here's a comment that won't get seen -->
<!--
Here's a comment that spans multiple lines!
See!
-->
```

Especially if you are doing something complicated, it's helpful to leave notes for yourself in your code. That way, if you came back a year later, or if someone else was reading your code and trying to understand it, they would have help!

## Whitespace
The browser mostly ignores the whitespace in your HTML page.

`<br>` is the line break tag - it's like pressing enter on the keyboard.
```
<p> I could use a <br> break</p>
```
`&nbsp;` is the html entity name for a no-break space. If you want to put extra spaces in between words, you can use it like this:
```
<p> I need a little &nbsp; &nbsp; &nbsp; space </p>
```

## Conclusion
HTML allows us to define and label the content of our page. All modern browsers have implemented the same specification for how to display content written with html syntax. Now, you have control over how content is displayed, by naming the parts in the structure of your document.
