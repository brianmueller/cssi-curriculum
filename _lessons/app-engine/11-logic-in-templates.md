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

##  FakeMail App

To learn how to add logic to your template you we are going to create "FakeMail" app. Create a new AppEngine project called fakemail.

## Your main.py file
We will create an email class with the properties title and unread.
```python
import jinja2
import webapp2

env=jinja2.Environment(loader=jinja2.FileSystemLoader('templates'))

class Email(object):
    def __init__(self, title, unread):
        self.title=title
        self.unread=unread
```
Then inside your MainHandler, create an email variable with a list of emails.

```python
class MainHandler(webapp2.RequestHandler):
    emails = [Email('Important!', True),
    Email('Weekend plans', True),
    Email( 'Lunch?', False)]

[{'subject':'hello world', 'content' : 'I love coding'},
{'subject':'hello world2', 'content' : 'I love coding 1'}
{'subject':'hello world3', 'content' : 'I love coding2'}
{'subject':'hello world4', 'content' : 'I love coding3'}]
{'subject':'hello world5', 'content' : 'I love coding4'}


    def get(self):
        template = env.get_template('main.html')
        variables = {'name':self.request.get('name'),
                    'emails':self.emails}
        self.response.write(template.render(variables))

app = webapp2.WSGIApplication([
    ('/', MainHandler)
], debug=True)
```

### Jinja2 Syntax
To add logic to a template, variables go between mustaches `{{variables}}` and code is embedded between curly brackets and percent signs {%raw %} {% code %} {% endraw %}
```python
<h1>{{name}}'s cart </h1>
<table>
{% raw %}
  {% for item in items:%}
    <tr>
      <td>{{ item }}</td>
    </tr>
    {% endfor %}
{% endraw %}
</table>
```

###  Looping through Dictionaries
```python
#  template variale in main.py
template_vars = {"pets" : {'willie':'horse', 'wilbur':'pig'}}
# in pets.html
<table>
      {% raw %}
      {% for key, value in pets.items() %}
            <tr>
              <td>{{key}}</td>
              <td>{{value}}</td>
            </tr>
      {% endfor %}
      {% endraw %}
</table>

```
###  Looping through Nested Dictionaries
```python
#  a template variable, pets in main.py

template_vars = {"pets" : {'willie': {'kind': 'dog', 'owner': 'eric'},
        'walter': {'kind': 'cockroach', 'owner': 'eric'},
        'peso': {'kind': 'dog', 'owner': 'chloe'},}}

#  in  pets.html
<h1> Our pets</h1>
{% raw %}
{% for pet_name, pet_information in pets.items() %}
    <p>
     {{pet_name.title()}} is a {{pet_information['kind']}} who is owned by {{pet_information['owner']}}.
    </p>
{% endfor %}
{% endraw %}
```

### Logic in Templates Exercise


###  Stretch Lab
