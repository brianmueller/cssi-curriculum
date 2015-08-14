---
layout: post
title: Intro to APIs
language: apis
---
#  What You Will Learn:
+ Understand how APIs connect services on the web
+ Understand how Client Libraries wrap API functionality
+ Connect to any public facing API
+ Access the returned data from an API

# Why This is Important:
APIs (Application Programming Interfaces) are a major part of the internet and allow amazing things to happen easily. There are TONS of cool ways to connect other applications to extend our app's functionality. Want to include GIFs based on user searches? Show Tweets related to your site? We can do this and much, much more using APIs!

# What is an API?
+ API stands for "Application Programming Interface".
+ In a nutshell, an API is a way for developers to interact with someone else's service.
+ On the web, APIs are usually service that sends data when you request it. It's a way for the developers of existing applications to allow other people to get their data in a controlled way.

# Sending a request
In Python, we use a library called urllib2 to get data over the internet. Let's start by getting the html from a very familiar page - www.google.com!

```python
import urllib2
print urllib2.urlopen("http://www.google.com").read()
```

Save and run this code - you'll see a big mess of html printed out on the command line!

What do the different pieces of this script do?

1. `import urlib2` loads the urllib2 library so we can use it
2. `urlib2.urlopen()` is the function for fetching data from a webpage - we pass in a string parameter with the url to fetch.
3. urlopen opens the url like a file. `.read()` turns the file into a string.
4. `print` prints the string! It's a bit of a mess, but that's okay!

# Getting Useful Data
The google homepage may be super useful in the browser, but getting the pure HTML from the page doesn't do much for us. Let's look at [OpenWeatherMap](http://openweathermap.org/api) data instead - it has live weather data around the world, and the API is pretty easy to learn.

From looking at the documentation, we see that we can get weather data for a city by searching for it with a url query. For instance,

```python
import urllib2
url = "http://api.openweathermap.org/data/2.5/weather?q=London"
data = urllib2.urlopen(url).read()
print data
```

This will print out what looks like an ugly mess of data, but is actually very well structured.

```javascript
{"coord":{"lon":-0.13,"lat":51.51},"weather":[{"id":802,"main":"Clouds","description":"scattered clouds","icon":"03d"}],"base":"cmc stations","main":{"temp":292.72,"pressure":1022,"humidity":56,"temp_min":291.15,"temp_max":294.15},"wind":{"speed":6.7,"deg":80},"clouds":{"all":40},"dt":1439405840,"sys":{"type":1,"id":5091,"message":0.0039,"country":"GB","sunrise":1439354510,"sunset":1439407681},"id":2643743,"name":"London","cod":200}
```

It's a JavaScript object, almost the same thing as a Python dictionary! In fact, we can turn it into a Python dictionary with a single command.

```python
import json
import urllib2
url = "http://api.openweathermap.org/data/2.5/weather?q=London"
data = urllib2.urlopen(url).read()
data_dictionary = json.loads(data)
print data_dictionary
```

This will print the same data, but after it has been turned into a Python dictionary. JSON is JavaScript Object Notation, and `import json` gives us access to a popular library for dealing with JSON, with functions for tasks like turning a JSON-formatted string into a Python dictionary.

# Getting Data from the Data
We've turned the response from the OpenWeatherMap API into a Python dictionary, but we still haven't done anything with it! Let's get the temperature.

Take a look at the data. `temp` is a key of a dictionary inside our main dictionary. The key `main` maps to a dictionary with some of the main information about the weather - temperature, pressure, and humidity.

```python
import json
import urllib2
url = "http://api.openweathermap.org/data/2.5/weather?q=London"
data = urllib2.urlopen(url).read()
data_dictionary = json.loads(data)
print data_dictionary['main']['temp'] # Get temp out of main
```

The default unit of temperature from the API is Kelvin. If we look in the API documentation, we find that we can specify `units=Imperial` as an additional url parameter to get Fahrenheit temperature, like this:

```python
url = "http://api.openweathermap.org/data/2.5/weather?q=London&units=Imperial"
```

When we run the code again, we get the more familiar Fahrenheit temperature. Celsius is available if we set `units=Metric`.

# Client Wrapper Libraries for APIs
Sometimes developers will provide you with a class/module/library that makes connecting to an API much easier.  They will make sure that the correct language for that API is used and all you have to do is use the (hopefully) simple methods that they provide.  

# Learning new APIs
Every API is a little bit different, but in general we can follow a process for connecting to them.

1. Read the documentation.
2. Setup an "API call" - going to get the data
3. Deciding what to do when you get the data back

Sometimes, APIs are well documented and we can follow the instructions easily. Other times, they're not so well documented and we'll have to play around a bit more.

It's often a good idea to explore an API in the browser before trying to get the data out in python.

# Conclusion

APIs are the way that web applications talk to each other. They will allow you use and incorporate advanced functionality and leverage existing services in your applications.

# Resources
+ APIs are a great way to add new functionality to your project
+ Make sure you read the documentation for APIs, they all work a little differently
+ There are great tools out there to help you work with APIs such as [hurl](https://www.hurl.it/), [postman](https://www.getpostman.com/), and [apiary](https://apiary.io/). The [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=en) Chrome extension formats JSON in the browser for easy-on-the-eyes API exploration in the browser.

# List of APIs that don't need Authentication
From [here](https://shkspr.mobi/blog/2014/04/wanted-simple-apis-without-authentication/)

- [Wikipedia API](https://www.mediawiki.org/wiki/API:Main_page)
- [BBC Radio 1 API](http://www.bbc.co.uk/developer/technology/apis.html)
- [OpenStreetMap Overpass API]( http://wiki.openstreetmap.org/wiki/Overpass_API)
- [OpenWeatherMap](http://openweathermap.org/)
- [Open APIs From Space](http://open-notify.org/)
- [Pokemon API](http://pokeapi.co/)
- [Text To Speech API](http://tts-api.com/)
- [Google Books API](https://developers.google.com/books/?hl=en)
- [UK Police Data](http://data.police.uk/docs/)
- [Iceland APIs](http://docs.apis.is/)
- [University of Maryland Data](http://umd.io)
- [US Gov Data](https://www.data.gov/)
- [Football (Soccer) Data](http://api.football-data.org/index)
- [UK Postcodes](http://postcodes.io/)
- [Yahoo Weather](https://developer.yahoo.com/weather/)
- [Giphy](https://api.giphy.com/)
- [Open CNAM Caller ID](https://www.opencnam.com/)
- [Reddit](http://www.reddit.com/dev/api)

Some Endpoints on other APIs that don't require Authentication:
- [Spotify Search](https://developer.spotify.com/technologies/metadata-api/search/)
- [Flickr Feeds](https://www.flickr.com/services/feeds/)
