---
  layout: post
  title: HTML Lab Student Walkthrough
  language: html
---
##  Instructions


#### Setup
1. Press command+space to open spotlight
2. Type “Atom” and press enter to search for and open the Atom editor
3. Go to “file” and click “new file” (command+N)
4. Save the file with command+S
5. Save your file as “my_profile.html”
6. Select your Desktop for where the file should be saved
7. Copy the boilerplate code below!

```
<!DOCTYPE html>
<html>
  <head>
    <title>
      My personal webpage!
    </title>
  </head>
  <body>
    <h1>Heading</h1>
    <p>
      Some text about you!
    </p>
  </body>
</html>
```

#### Adding sections
For your new personal website all about you! Somethings you can include are: a short bio, your hobbies, fact about your future college etc. Try to make sure your webpage includes:
* a title
* a subheader (using h2-h6 tags)
* a p tag with a short descriptive paragraph
* an image (consider using your android Avatar if you can’t find a quick picture that you like)
* a link  to your g+ page, your github page  or another social media page

#### Stretch: Adding pages
* Add pages to your site by creating three separate html files: blog.html, pictures.html and home.html
* To link to pages in the same site, use an <a> tag.
* If your site has index.html and facts.html and they're in the same directory, having a link from index.html to facts.html looks like this: <a href="facts.html">click here for more facts</a>. This is a relative link.
* Put links in an unordered list using ul and li tags

#### Sample, Explained
If you need inspiration or want to know how to do more:
````
<!DOCTYPE html>
<title>Matthew Levine's Profile</title>

<h1>Matthew Levine</h1>

<img src="matthewlevine.jpg" width="80" height="80" alt="Photo of Matthew Levine">

<h2>Summary</h2>
<p>I live in San Francisco and work at Google. I like teaching, hanging out in coffee shops, and swing dancing.</p>

<h2>Hometown</h2>
Tustin, California

<h2>University</h2>
Dartmouth College

<h2>Other Profiles</h2>
<ul>
  <li><a href="http://plus.google.com/115182601594934760469">Google+</a></li>
  <li><a href="http://www.facebook.com/matthew.s.levine">Facebook</a></li>
  <li><a href="http://twitter.com/matthewlevine">Twitter</a></li>
</ul>

<h2>My Favorite Movies</h2>
<ol>
  <li>Sneakers</li>
  <li>Groundhog Day</li>
  <li>Memento</li>
</ol>
```

Save this as profile.html and load it into your browser. Let's take a look at each part:
`<h1>Matthew Levine</h1>`

This is the top-level heading. How does this differ from the `<title>`? The title doesn't appear in the body, so we often see a similar `<title>` and `<h1>`.

`<img src="matthewlevine.jpg" width="80" height="80" alt="Photo of Matthew Levine">`

This should show an image of the author, but it's broken. There are some important attributes in the `<img>` element you need to know:
* src: This is the URL ("source") of the image.
* width & height: These are optional, but if you specify them in your HTML, the page won't jump around when the image loads
* alt: The "alternate" text, a short description. This is useful if the image is broken, or for users who can't see the image and rely on a description instead.

**Challenge:** find an image online (try Google Image Search), and put its full path into the src attribute, replacing the nonexisting "matthewlevine.jpg". How does it look? If it's the wrong size, what can you edit to fix this?

`<h2>Summary</h2>`
The `<h2>` elements are subheaders here. By default, they're smaller than `<h1>`s, but larger than body text.

`<p>I live in ... </p>`

A `<p>` element is a paragraph; this commonly container for body text, e.g. in a blog post.
```
<ol>
  <li>Sneakers</li>
  <li>Groundhog Day</li>
  ...
</ol>
```
The `<ol>` element is an "ordered list". This comes in handy when you're listing things that have a natural order, like a chronological list of places you've worked or a list of the winners of a race.

Below, you'll notice a `<ul>` element. This is for an "unordered list". This also contains list items, but should be used for lists that don't have a natural order. By default, these are usually bullet lists instead of numbered lists (but we can change that with styling).

The `<li>` element is a "list item". These go inside lists.

`<a href="http://plus.google.com/115182601594934760469">Google+</a>`

We've seen this before. The `<a>` element should contain an "href" attribute with the URL of the destination page. The content of the anchor should contain the link text.

Altogether, we've seen the following elements so far:
* title: the document title
* h1 - h6: headers
* p: paragraphs
* ul, ol: lists (unordered and ordered)
* li: list items
* a: anchors (links)
* img

A few other basic elements
* em: emphasis
* strong: strong emphasis
* blockquote: a block quote (used to excerpt long passages)
* div: a generic block
* span: a generic string of text

**Exercise:** Add these elements to your own profile. Run it through an html validator to make sure that you did it correctly. Add an extra section or two beyond what's in the example.

### Linking Pages Together
Say I wanted to create a photo page to link to my profile page, something like this:
```
<!DOCTYPE html>
<title>Matthew Levine's Photos</title>
<h1>Matthew Levine's Photos</h1>
<h2>Photos with My Brothers</h2>
<ul>
  <li><img src="brothers1.jpg" alt="Old brothers, new brothers"></li>
  <li><img src="brothers2.jpg" alt="Fooooooootball!!!!"></li>
  <li><img src="brothers3.jpg" alt="Groomsmen"></li>
</ul>
...
```
Now I want to link my profile to my new photo page. How do I do that?
If both my profile.html and photos.html pages are in the same directory, I can simply use the file names:

`<a href="photos.html" title="Matthew Levine's Photo Album">Photos</a>`
and:
`<a href="profile.html" title="Matthew Levine's Profile">Back to my profile</a>`

Try it! Create a new page for your photos. Link your photos page to your profile page and vice-versa.

If time allows: create a friends.html page. Include at least three friends, along with photos and links to their profiles on social networks. Make sure your friends page links to both photos and profile pages.



##  Resources
[W3 Schools HTML](http://www.w3schools.com/html/)
