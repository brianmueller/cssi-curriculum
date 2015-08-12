---
  layout: post
  title: Template Variables with Fortune Teller
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
