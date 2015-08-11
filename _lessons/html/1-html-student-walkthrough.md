---
  layout: post
  title: HTML Student Walkthough
  language: html
---

HTML is the foundational technology for the Internet, every one of your favorite websites is HTML at its core. This walkthrough explains how to create an HTML site from scratch, and start creating a personal web page.

####  What is a Webpage?
A basic web page is just a file that can be loaded from your browser, like Chrome, Safari or Internet Explorer.
Most webpages are stored on servers all over the world. To get to those files from our browser we have to use a URL - Uniform Reference Locator. This is an address that tells our browser where to find each file.

However, you can also create a webpage _locally_ (on your own computer) and open it in your browser. This is what we'll start with today.

####  File Extensions
All programs start out as text files. In order to let other programs (and humans) know what language a file is written in, we add a different file extension. So, the html files are saved as file**.html**, javascript files are saved as file**.js**, CSS files are named file**.css**, and python files are file**.py.**

When we start writing in HTML, what extension will we use? .html of course!

###  Writing your First Webpage, Hello World (for Macs)

####  Getting Setup

1. Cmd+space: opens your spotlight search.
2. Type "Atom" and press enter
3. Go to "file" and click "new file" to open a new tab
4. Cmd+space Save as "hello_world.html"
5. Save the file on your desktop

#### HTML Page Structure (Hello, World!)
In hello_world.html type the following:
```html
<!DOCTYPE html>
<title>My First Web Page</title>
Hello, world!
```
Save your file. Then open it in your browser. You're a web developer!

####  Breaking Down Hello World
Congratulations, you made a site! Obviously, there's a lot to do in order to make the site better. Let's get started by breaking down the different parts of what we wrote:

`<!DOCTYPE html>`

This is -- reasonably enough -- called the DOCTYPE. It lets someone - or a program like your browser - know that the document it's looking at is an HTML document, and in particular, an HTML5 document. Browsers use this statement to determine whether your page should be displayed in "standards mode" (good) or "quirks mode" (old and inconsistent). It will make your life much easier if you remember to include this.

`<title>My First Web Page</title>`

Note that this text doesn't appear on the body of the page, but in the title (which is usually in your browser's tab). It's important to make the title clear and succinct and contextually independent. This will also be the default bookmark name, and title of the search result for the page.

`Hello, world!`

This is body text. It appears in the body of the page, and we haven't done anything extra to it other than make it appear in the browser window.

### Elements and Tags

HTML is made up of building blocks called "elements". You've already seen one, the `<title>` element. Elements are typically made up of an "opening tag", a "closing tag", and some content in between. Here's another example:

`<h1>All About Honey Badgers</h1>`

This is an h1 (or "heading-1") element. Note that the opening tag `<h1>` differs from the closing tag `</h1>` by a slash.

Generally, elements are written like
`<tag>    .... CONTENT GOES HERE ....</tag>`

They have an opening tag, then some content, and then a closing tag, which is a / and the tag name.

There are a lot of different elements you can use in HTML. Check them out [here](http://www.w3schools.com/tags/)

Elements can also have "attributes", which go inside the opening tag and give extra information about an element. For instance, on an image element, you might see this:

`<img src="documents/pictures/car.gif"  height="50" width="100">`

There is a height attribute with a value of 50 and a width attribute with a value of 100. There is also the src attribute which stands for source - this tells the page where to find the image of the car. Notice that attributes take the form name="value", where the value is in quotes!

Different elements can have different attributes. For instance the img has height and width attriubtes, but it doesn't make sense for a `<p>` paragraph to have height and width attributes.

All elements, however, can have class and id attributes to help differentiate them from other elements. You will learn more about why class and ids are important in the next walkthough. For now take a quick look below.

```
<h1 id="main_title">The Gettysburg Address</h1>
  <p class="about">November 19, 1863.</p>

  <p>Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.</p>

  <p class="about">Delivered by Abraham Lincoln </p>
```

An `id` identifies a *unique* element on the page - there can only be one element that has that id. There is only one "main_title" of the speech.

The `class` lets us say that an element is a particular kind or group, used to identify and group elements that may occur more than once. There are a few places where we have paragraphs that are "about" the speech, so we can use the class attribute.

Some elements do not have closing tags; these are typically elements that have no textual content.

For example, the `<img>` element points to an image, but doesn't have any text inside.

`<img src="kittens.jpg" width="80" height="100" alt="Photo of kittens playing">`

This tag has attributes (src, width, height, alt), but no closing tag.

#### Tag Nesting

As you've seen, HTML elements just love to nest inside each other. This nesting is really useful for organizing the content of a page. On almost every page, there are pieces that belong to each other in a hierarchy.


```
<html>
  <head>
    <title>Just an Example</title>
    <meta author="Helpful meta-info">
  </head>
  <body>
    <nav>
      <ol>
        <li>home</li>
        <li>another page</li>
        <li></li>
      </ol>
    </nav>
    <article>
      <h1>Article Title</h1>
      <section>
        <p>Here's some text!</p>
        <p>It's inside a paragraph inside a section</p>
        <p>inside an article inside the body inside the document</p>
      </section>
    </article>
  </body>
</html>
```
In the code above, a hierarchy of elements could be:
Text belongs to paragraphs, paragraphs belong to sections, sections belong to an article. Items in a list belong to a list, and the list can be a list of links in a nav bar. Both the article and the nav bar belong to the body of the page. The body of the page, the title, and some meta-info all belong to the whole html document.

It's helpful to think about what parts of the page belong to each other, or are inside of one another. Then the html looks less like meaningless characters, and more like a useful way of structuring our documents!

#### Whitespace
The browser mostly ignores the whitespace in your HTML page. If you have text on different lines or with lots of spaces in between, it will all get replaced by a single space. This is really helpful for making our HTML file readable - we can hit Enter as many times as we need to, and the browser will ignore it!

This:
```
<p>For years, I wondered why Garfield was so popular. I still can't believe that anyone finds that cat funny in the slightest. It's mean to the man and dog. Ha.</p>
```
Will show up the same as this:

```
<p>For years,

I wondered why Garfield was so popular.


I still can't                       believe that anyone finds that cat funny in the slightest. It's mean to the man and dog.


Ha.</p>
```

Why anyone would use the second one is beyond me, but there are lots of times when this trick can be useful!

It also forces us to use other ways to put whitespace into our pages, if we want it. We'll go in depth about styling and positioning when we cover CSS, but for now, there are two whitespace tricks to know.

br is the line break tag - it's like pressing enter on the keyboard.

`<p> I could use a <br> break</p>`

&nbsp; is the html entity name for a no-break space. If you want to put extra spaces in between words, you can use it like this:

`<p> I need a little &nbsp; &nbsp; &nbsp; space </p>`

### Types of Tags

#### Headers
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
#### Paragraphs and emphasis
`<p> `tags, delineate paragraph text
`<strong> `will make any text contained within bold
`<em>` will italicize text or add emphasis

#### Lists
Bullet point lists start with `<ul>` for unordered list
Numbered lists start with `<ol>` for ordered list
The actual list items go between `<li>` tags. li stands for list items
```
<ul>
  <li>item with bullet point</li>
  <li>2nd item with bullet point</li>
  <li>another list item</li>
</ul>

<ol>
  <li>Numbered item</li>
  <li>List item # 2</li>
  <li>Third list item</li>
</ol>
```

#### Links
Links use an `<a>` tag, which stands for anchor. If you wanted a link to Google it would look like this:

```<a href="http://www.google.com">An absolute link to someone else’s site</a>```

And if you wanted to link to a file right next to your practice.html file on your computer, it would look like this:

```<a href="my_folder/stuff.html">A relative path to my site</a>```

#### Images
Images use an <img> tag to embed an image in a webpage.
`<img src="your_image_location">`

This can be either an absolute path (good for "hot-linking" to images you find on the web) or a relative paths.

#### Indentation
HTML is not the easiest to read. It's designed to be clear for the browser to understand, but not always for humans. However, there are some ways to make it easier for you and others to read your code. Following the guidelines will help make your code easier to understand and debug.

Bad indentation:
```
<html><head><title>The end of the world as we know it</title>
</head><body><p>
Some text about things</p></body>
```
This is confusing to read, and makes it harder to find errors. Can you spot the missing tag?

Good indentation:
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
#### Comments
HTML also has a way to write things that won't show up in the browser at all. That doesn't sound very useful at first, but developers use this invisible text to leave helpful comments in the code.

HTML comments look like this:
```
<!-- Here's a comment that won't get seen -->
<p>This line will show up</p>
<!-- <p>This line will not show up</p> -->
<p>This line will show up</p>
<!--
Here's a comment that spans multiple lines!
See!
-->
```
Especially if you are doing something complicated, it's helpful to leave notes for yourself in your code. That way, if you came back a year later, or if someone else was reading your code and trying to understand it, they would have help!

### Conclusion
* HTML allows us to define and label the content of our page. All modern browsers have implemented the same specification for how to display content written with html syntax. Now, you have control over how content is displayed, by naming the parts in the structure of your document.


#### Hints and Hurdles
* You do not need to know every tag - you need to know tag syntax: how to open and close tags and  how to use an attribute
* Don't worry too much about class and id attributes quite yet, you'll see them in CSS

####  Personal Profile Page
Part 1: [HTML Personal Page Lab](https://github.com/learn-co-curriculum/cssi-1.4-html--personal-webpage-lab)

####  Resources

* [W3 Schools HTML](http://www.w3schools.com/html/default.asp)
