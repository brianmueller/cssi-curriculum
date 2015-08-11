---
  layout: post
  title: Template Variables Challenge
  language: app-engine
---
##  Reminders
### Passings variables to a template:

Pass a dictionary of key:values as an argument to template.render():

  `template.render({"first_name": "Jay-Z"})`

Often times you'll want to do this as two seperate steps in order to make your code easier to read  
* Make a dictionary of values
```python
my_variables = {"first_name": "Beyonce",
                  "last_name": "Knowles",
                  "home_town": "Houston",
                  "profession": "Hero"}
```
* Pass that dictionary as an argument to template.render():

   `template.render(my_variables)`


### Getting variables from a URL

A url can pass variables through its query string which starts after the question mark character. An ampersand (&) indicates a new variable:

`http://amazon.com/home?item_name="bannana%phone"&seller_id=19`

To access those variables, use the self.request.get() method:

`template_vars = {"item": self.request.get('item_name')}`

You can also set a default value by adding an optional second argument, `default_value`:

`self.request.get('location', default_value='Chicago')}`

##  AppEngine Template Variables Mini Challenge
###  CHALLENGE
* Modify helloworld.py to read a new template parameter called `greeting` and pass it to the helloworld.html template.
* Edit your HTML so that it displays the greeting and the name.
* A url like `http://localhost:8080/helloworld?name=Norah&greeting=Howdy` should say "Howdy Norah!"

###  STRETCH CHALLENGE
* Read up on detecting user's location with html [here](http://www.developerdrive.com/2012/01/using-html5-to-determine-user-location/)
* How could you use this browser feature and some python logic to display a different message based on where the user was located? How could you do it solely in javascript?
