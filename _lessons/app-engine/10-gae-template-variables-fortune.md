---
  layout: post
  title: Fortune Teller Part.4 - Template Variables
  language: app-engine
---
# Template Variables with Fortune Teller
Path: /fortunecookie
Change your fortune cookie handler so that `http://localhost:8080/fortunecookie?/num=2` displays the 2nd fortune in your list. However be sure that the default,  `http://localhost:8080`, still gives a random fortune.


Path: /8ball
Create a dictionary with three keys: "positive", "neutral" and "negative". Their corresponding values are a list of 8ball responses. `http://localhost:8080/8ball?/type=pos` will give the 2nd response from your positive list of 8 ball responses.

You can make your own lists of responses, or use the [default values](https://en.wikipedia.org/wiki/Magic_8-Ball#Possible_answers), which contain 10 positive, 5 neutral and 5 negative answers.


#  Reminders
#### **Passings variables to a template:**

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


#### **Getting variables from a URL**

A url can pass variables through its query string which starts after the question mark character. An ampersand (&) indicates a new variable:

`http://amazon.com/home?item_name="bannana%phone"&seller_id=19`

To access those variables, use the self.request.get() method:

`template_vars = {"item": self.request.get('item_name')}`

You can also set a default value by adding an optional second argument, `default_value`:

`self.request.get('feeling', default_value='happy')}`

# **STRETCH CHALLENGE**
* Read up on detecting user's location with html [here](http://www.developerdrive.com/2012/01/using-html5-to-determine-user-location/)
* How could you use this browser feature and some python logic to display a different message based on where the user was located? How could you do it solely in javascript?
