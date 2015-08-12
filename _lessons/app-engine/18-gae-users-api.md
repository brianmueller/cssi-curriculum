---
  layout: post
  title: App Engine Users API
  language: app-engine
---

##  What You Will Learn:
+ Understand how AppEngine provides its own API libraries
+ Use the AppEngine Users API module

##  Why This is Important?


###  Calling the Giphy API from a handler

This code will display the *raw* data the the API returns. Interesting, but not terribly useful.

```python
import json
from google.appengine.api import urlfetch

class MainHandler(webapp2.RequestHandler):
    def get(self):
        data = urlfetch.fetch(
     "http://api.giphy.com/v1/gifs/search?q=+ryan+goslin&api_key=dc6zaTOxFJmzC&limit=10").content
        self.response.out.write(data)
```

###  App Engine Users API

The AppEngine Users module actually connects to Google’s User authentication service.  However for a developer the setup is very easy and allows you to have authenticated (signed in and verified) users that you can trust; they’re backed by Google.

Using this API Library is as simple as importing the `users` module from `google.appengine.api` and using the built in methods that are provided. Here's a very simple example of how that works.

```python
from google.appengine.api import users
import webapp2
class MyHandler(webapp2.RequestHandler):
    def get(self):
        user = users.get_current_user()
        if user:
            greeting = ('Welcome, %s! (<a href="%s">sign out</a>)' %
                        (user.nickname(), users.create_logout_url('/')))
        else:
            greeting = ('<a href="%s">Sign in or register</a>.' %
                        users.create_login_url('/'))

        self.response.out.write('<html><body>%s</body></html>' % greeting)
```
