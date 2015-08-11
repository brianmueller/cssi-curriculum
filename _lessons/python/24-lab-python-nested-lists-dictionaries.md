---
  layout: post
  title: Lab: Python Nested Lists and Dictionaries
  language: python
---

## Nesting Habits
<img src="https://s3.amazonaws.com/after-school-assets/nesting.jpg">
lists inside of lists! dictionaries inside of dictionaries! lists inside of dictionaries! dictionaries inside of lists inside of dictionaries! Oh my!

###  1: lists in lists
```python
sandwich = [["rye", "sourdough", "baguette"],[["ham", "salami", "turkey"],["swiss", "munster", "cheddar"]],["mayo", "mustard", "tabasco"]]
```
The `sandwich` list above is a series of nested lists. What do I get if I ask for:
+ `sandwich[0][1]` ?
+ `sandwich[1]` ?
+ `sandwich[1][0][0]` ?

What code should I write to return each of these?:
+ ["mayo", "mustard", "tabasco"]
+ "cheddar"
+ "sourdough"

Make me a salami sandwich with swiss cheese on rye bread with mustard and mayo. Thank you.

###  2: dictionaries in dictionaries
```

city_info = {'new_york' : { 'mayor' : "Bill DeBlasio",
							'population' : 8337000,
							'website' : "http://www.nyc.gov"
							},
			 'los_angeles' : { 'mayor' : "Eric Garcetti",
							'population' : 3884307,
							'website' : "http://www.lacity.org"
							},
			 'miami' : { 'mayor' : "Tomás Regalado",
							'population' : 419777,
							'website' : "http://www.miamigov.com"
							},
			 'chicago' : { 'mayor' : "Rahm Emanuel",
							'population' : 2695598,
							'website' : "http://www.cityofchicago.org/"
							}
		}
```
The `city_info` dictionary above is a series of nested dictionaries. What do I get returned if I ask for:
+ `city_info["los_angeles"]` ?
+ `city_info["chicago"]["mayor"]` ?

What code should I write to return each of these?:
+ The population of New York
+ The website for Miami city government
+ The mayor of Los Angeles
+ A dictionary with all information on Chicago

Bonus: Use a loop with another loop to return a string for each key value pair belonging to a city. For example, for Miami you should see:

```
"The mayor of miami is Tomás Regalado"
"The population of miami is 419777"
"The website of miami is http://www.miamigov.com"
```
