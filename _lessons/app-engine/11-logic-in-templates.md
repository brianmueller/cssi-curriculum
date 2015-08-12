---
  layout: post
  title: Logic In Templates
  language: app-engine
---
# What You Need to Know:
+ Introduction to the Web
+ Python Basics and Classes
+ How to Launch an App Engine App
+ How to Serve Static Templates

# What You Will Learn:
+ How to add logic to your templates with the properties title and unread

To learn how to add logic to your template you we are going to create "FakeMail" app. Create a new AppEngine project called fakemail.

## Your main.py file
We will create a variable called email_list with a list of dictionaries containing our inbox emails.

```python
import jinja2
import webapp2

env=jinja2.Environment(loader=jinja2.FileSystemLoader('templates'))

class MainHandler(webapp2.RequestHandler):
  emails= [{'subject':'Lunch?', 'unread' : True},
          {'subject':'Facebook notification', 'unread' : False},
          {'subject':'Help! send me money from your account!', 'unread': True},
          {'subject':'Meeting on Thursday', 'unread' : False}]
  def get(self):
      template = env.get_template('main.html')
      variables = {'name':self.request.get('name'),
                  'emails':emails}
      self.response.write(template.render(variables))

app = webapp2.WSGIApplication([
    ('/', MainHandler)
], debug=True)
```

### Jinja2 Syntax
To add logic to our html template, variables go between mustaches `{{variables}}`. The jinja2 syntax for embedding python code in our template is to use curly brackets and percent signs.

```python
<html>
  <body>
    <h1>FakeMail</h1>
    <h2>Welcome {{name}}</h2>
    <ul>
      {% for email in emails %}
        <li>
          {% if email.unread %}
            (unread)
          {% endif %}
          {{email.subject}}</li>
      {% endfor %}
    </ul>
  </body>
</html>
```

## Exercise FakeMail
Add logic in the code that searches whether the email has the words "help, money and account" and if so the email should be marked "spam".

##Stretch Exercise
Create an email class with the subject, unread, and spam properties instead of having a list of dictionaries with emails.
```python
class Email(object):
    def __init__(self, title, unread,spam):
```
