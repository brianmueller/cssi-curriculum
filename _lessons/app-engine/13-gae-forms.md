---
  layout: post
  title: Forms in App Engine
  language: app-engine
---
# What You Need to Know:
+ Introduction to the Web
+ Python Basics and Classes
+ How to Launch an App Engine App
+ How to Serve Static Templates
+ How to use logic in templates

# What you Will Learn:
+ How to create an HTML form
+ How to render the user's input
+ The HTTP methods GET or POST

# HTML Forms

We are going to create a [MADLIBS][http://www.madglibs.com/] app to learn HTML forms. Create a new App Engine project called "madlibs".

HTML form elements are used to collect user input.

***Form method***:The method attribute specifies the HTTP method (GET or POST) to be used when submitting the forms.
***Action***:The action attribute tells which page to return to once the submit button is pressed. Since the handler takes care of the response, don't worry about the action attribute and leave it blank.
***Input type***:There are many different input types like text, radio, checkbox and submit. Find more input types on [w3schools](http://www.w3schools.com/html/html_form_input_types.asp)
***Name***: The name attribute allows us to access the form elements

# Create a main.html file
Create a templates folder with a main.html  file. Create a new HTML form:

```html
<html>
  <body>
		<h1>Adventures at CSSI</h1>
    <form method="post" action ="">
		 <h3>Enter a name: <input type="text" name="noun1"/></h3>
		 <h3>Enter an activity: <input type="text" name="activity"/></h3>
		 <h3> Choose one: </h3>
		 <input type="radio" name="teacher" value="Matthew">Matthew
     <br>
     <input type="radio" name="teacher" value="Victoria">Victoria
		 <h3>Enter a Celebrity's Name:<input type="text" name="celebrity"/></h3>
		 <h3>Enter a TV Show:<input type="text" name="show"/></h3>
    <h3><input type="checkbox" name="fun" value="FUNNNN!!!!!!!!!!!"> Check here if you are having fun at CSSI<br>
		<p><input type="submit" value="Submit"></p>
 </form>
  </body>
</html>

```

# Adding the  Post Method
If you use a POST method in your template, you need to add a way for your handler to take care of those post requests.


```python
import jinja2
import webapp2

env = jinja2.Environment(loader=jinja2.FileSystemLoader('templates'))

class MainHandler(webapp2.RequestHandler):
    def get(self):
    	main_template = env.get_template('main.html')
    	self.response.out.write(main_template.render())
    def post(self): ## here's the new POST method in the MainHandler
    	self.response.out.write("You have submitted your madlib")
```

In the code above
* When the handler receives a GET request, it's response is to render a template
* When the handler receives a POST request, it's response is to write a message.

# Adding a Results Template
Most likely, you'll want to add a new HTML page that gets rendered after the user submits their form.

Add your results.html file in the templates folder. Then in your MainHandler, be sure to make sure your template gets rendered after a POST request.

```python
class MainHandler(webapp2.RequestHandler):
    def get(self):
    	main_template = env.get_template('main.html')
    	self.response.out.write(main_template.render())
    def post(self):
    	results_template = env.get_template('results.html')
    	self.response.out.write(results_template.render())
```

# LINKING the HTML Form and the Handlers
In order to grab the values from our form, we just need to take advantage of the self.request.get() method and grab our values from the user.


```python
class MainHandler(webapp2.RequestHandler):
    def get(self):
    	main_template = env.get_template('templates/main.html')
    	self.response.out.write(main_template.render())
    def post(self):
    	results_template = env.get_template('templates/complete.html')
    	## the variables that are sent to results.html are user_answer_1 and user_answer_2
    	## they contain the input values from the main.html form with names answer1 and answer2
    	template_variables = {'noun1':self.request.get("noun1"),'activity':self.request.get("activity"),'teacher':self.request.get("teacher"),'celebrity':self.request.get("celebrity"), 'show':self.request.get("show"), 'fun':self.request.get("fun")}
    	self.response.out.write(results_template.render(template_variables))
```

#### Using the Template Variables
When your template variables get passed from the handler to the template, you can use them by surrounding them with mustaches `{% raw %}{{ }}{% endraw %}`

```html
<html>
<head>
	<title>Your CSSI Story!</title>
</head>
<body>
	<p>{% raw %} Once upon a time {{noun1}} wanted to learn to {{activity}}
  at Google. So {{noun1}} flew to Google and met {{teacher}}.
  To {{noun1}}'s surpise {{celebrity}} was also in the class!
  Together {{noun1}} and {{celebrity}} decided to work on a project about {{show}}.
  {{noun1}} had so much {{fun}}{% endraw %}</p>
</body>
</html>

```
# Exercise: Create your own Madlib!

* Add a new form on the same main.html
* Grab the users input and render the results on the results.html page
