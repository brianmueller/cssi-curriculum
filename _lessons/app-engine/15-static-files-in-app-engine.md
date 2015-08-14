---
  layout: post
  title: Serving Static Files
  language: app-engine
---

# Challenge - Add Styling to your HelloWorld App
* Create a new file called style.css.
* Add some simple styling in the style.css file (font color, an image border, background color)
* Link the style.css sheet to helloworld.html
* View your styled page on localhost:8080
* Show us when you’re done.

[The solution is below, only cheaters would scroll down to look!]

![gif of a cheating runner](http://media.giphy.com/media/BUOlQ1H5RCR1K/giphy.gif)

####  Lesson Notes
Unlike other environments, merely linking the CSS file by using `<link rel="stylesheet" type="text/css" href="style.css">` doesn't quite work.

GAE doesn't know where to look for our style.css file unless we configure it in the app.yaml file. Our stylesheet is an example of a static file.
Images, JavaScript code, video, and Flash animations are also examples of static files that we need to tell AppEngine how to access.  

###  Configuring app.yaml for Static Files
* Static files need to be kept in their own directory.
* In app.yaml, add a handler that routes to that directory and declare that directory as static using static_dir

```
handlers:
- url: /img
  static_dir: img

- url: /.*
  script: main.app
```
In this example, a directory name "img" contains all of our locally stored image files.

# Exercise: Upload Your Personal Page onto Google App Engine

Move your profile page HTML and CSS files into the webapp2 framework. Doing this will allow you to add some additional features (like custom user messages, blog posts and comments) to your already awesome profile page.

+ Add templates for all of your profile project html files (blog, home, pictures)
+ Add handlers for each of those pages and make sure the render the correct templates
+ Change your routes so that `localhost:8080/blog` goes to the correct place

You will need to remember:

+ The webapp2 framework
+ template.render()
+ static_dir
+ Optionally use self.request.get() to pass in a template variable and have your page respond.

Challenge yourself:

* Use self.error(404) to add an error msg for an unknown url
* Add template variabes
* Add a form
* Add conditional or loop logic
* Use geolocation. [Read up](http://www.developerdrive.com/2012/01/using-html5-to-determine-user-location) on detecting user's location with html and apply it to your profile page
