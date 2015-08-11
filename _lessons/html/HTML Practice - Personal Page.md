---
  layout: post
  title: HTML Personal Webpage
  language: html
---

# Lab Setup

## Making Your Github Pages Repository
  1. Open Chrome and go to www.github.com
  2. At the top right click the “+” new repository
  3. Name your repository “username.github.io”. It will be public by default.
      * make sure to  replace username with your username
  4. "Initialize this repository with a README " should be checked by default. Leave this checked so that you will be able to clone your new repository.
  5. Click the green "Create Repository" button.  
  6. In the right sidebar of the repository page on GitHub, look for the text "HTTPS clone URL". Click the clipboard button to  copy your repository's URL.

## Working On Your Github Pages  
  1. Open your terminal
  2. Move into your ~/cssi folder: 'cd cssi'
  3. Clone your repository onto your local machine: `git clone **https://github.com/username/username.github.io.git**``
    * make sure to  replace username with your username
  4. cd into your “username.github.io.git” repository
  5. Make your new homepage index.html: `touch index.html`
  6. Open your files on atom: `Open . -a "atom"``
  7. Copy the boiler plate code below and you will have your first html page!

# Boilerplate code:
```html
<!DOCTYPE html>
<html>  
  <head>
    <title>My personal webpage!</title>  
  </head>  
  <body>
    <h1>Heading</h1>
    <p>Some text about you!</p>
  </body>
<html>
```
# Add, Commit and Push your Files
11. Add your directory : `git add .`
12. Commit your changes to your local machine: `git commit -m “first commit”`
13. Push your changes up to Githib: `git push`
14. Check out http://username.github.io for your webpage!

# Adding Sections
Add content to your site. You can include are: a short bio, your hobbies, facts about your future college etc.
Your html webpage should include
+ a title (h1 tag)
+ a subheader (using h2-h6 tags)
+	a p tag with a short descriptive paragraph
+	an image (consider using your android Avatar if you can’t find a quick picture that you like)
+	An list of links to your g+ page, your github page, or another social media page (you will need the <li> tags and the <a> tag)

# Adding pages
Add additional pages to your site by creating separate html files
+ Create a new page, like a favorite page: `touch favorites.html`
+	To link to pages in the same site, use an `<a>` tag.
+	Link the pages using relative paths. If your .html pages are in the same directory,  a link on the index.html to favorites.html looks like this
`<a href="my_website/favorites.html">My Favorites</a>`
+ This is a relative link.
+ Don't forget to add your new file: `git add favorites.html`
