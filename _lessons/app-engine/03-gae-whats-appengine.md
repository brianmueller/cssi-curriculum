---
  layout: post
  title: Breaking Down Google App Engine
  language: app-engine
---
# What You Need to Know:
+ Introduction to the Web
+ Python Basics and Classes
+ How to Launch an App Engine App

# What You Will Learn:
+ Client server relationships
+ Understanding GET and POST requests
+ Understanding the MVC framework

# Why This is Important:
**Google App Engine** is a Platform as a Service (PaaS) offering that lets you build and run applications on Google’s infrastructure. You upload your files through the App Engine interface and your app gets hosted on Google's servers. App Engine connects the back-end and front-end for you.

Before we continue to make our own webapps, we need to speak very briefly about how anyone on the internet can access the code that you write at home.

# Clients and Servers
The internet is a network of computers that communicate with each other using HTTP, which defines how data is deliverd. We won't cover HTTP too much during CSSI but you can read more about it [here](http://www.tutorialspoint.com/http/http_overview.htm).

The computers can either be clients, servers or often times both.

![Client and Server Diagram](https://mdn.mozillademos.org/files/4291/client-server.png)

The webapps you build will
* Get data from a client -  a request
* Use a server to send data back -  a response.

A server is a computer that waits (listens) for requests and sends back responses. Clients are usually individuals on their web browser, and their requests might be typing in a certain URL or submitting certain information.

# Requests
When building apps on App Engine you will need to consider how your users will interact with your app.

There are two ways that a client (users) can make a request (send data): **GET** and **POST**
 + GET - data is stored within a URL
 + POST - data is submitted and temporarily stored

You will learn how to deal with both of these types of requests later today.

# MVC
In week 1, we learned front-end languages: HTML, CSS and JS and a back-end language: Python. Webapps need a way to connect the front-end, the back-end and will often need a database.

The way that many people refer to the connections between everything a webapp might need is MVC or Model-View-Controller.

<img src="http://lh3.ggpht.com/aviadezra/SHj6gLRSkSI/AAAAAAAAALg/0xkCGOXuefc/image_thumb3.png?imgmax=800" width=300px>

+ **Models** (Back-end data - Datastore in App Engine)
  + Stores the data
+ **Views** (Front-end - HTML Template in App Engine)
  + The front end, this is what the user sees.
+ **Controller** (Back-end logic - our Python scripts in App Engine)
 + The  the code that is in charge of making the back end  communicate to the front end

This MVC - model view controller - framework is the way that most modern web applications are organized.
Keeping the functionality of our application in these separate directories helps us stay organized as our apps become more and more complex.

# Handlers and Routes

A handler is the way that the back and front end interact in Google App Engine.

```python
class MainHandler(webapp2.RequestHandler):
    def get(self):
        self.response.write('Hello world!')

class CountHandler(webapp2.RequestHandler):
    def get(self):
        for i in range(1, 101):
            self.response.write(i)

app = webapp2.WSGIApplication([
    ('/', MainHandler),
    ('/count', CountHandler),
], debug=True)
```

Each handler is a block of code that is set up to send a certain response. MainHandler and CountHandler both respond in different ways. Handlers can respond to GET requests - like in the code above, but they can also respond to POST requests.

In order to set up the type of response to send to the user, you need to write routes. A route is a like a map that shows which handler to run for each url.
* If the user's request was `localhost:8080` , then the MainHandler would respond with `Hello World`
* If the user's request was `localhost:8080/count` , then the MainHandler would respond by printing a bunch of numbers!
