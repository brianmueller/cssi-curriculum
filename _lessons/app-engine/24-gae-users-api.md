---
  layout: post
  title: App Engine Users API
  language: app-engine
---

# What You Will Learn:
+ Understand how AppEngine provides its own API libraries
+ Use the AppEngine Users API module

# Why This is Important:
Many applications have users sign in, so that they can interact with their own data. Creating a login system from scratch is difficult, and it forces your users to create an account on your site. If you use the App Engine Users API, you get the power of Google's user system - your users can log in with their Google Account.

# App Engine Users API
The AppEngine Users module actually connects to Google’s User authentication service.  The setup is very easy for a developer and allows you to have authenticated (signed in and verified) users that you can trust; they’re backed by Google.

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

Underneath, the library is sending requests and getting responses, just like you would with any other API. The abstraction of the library makes your code simpler and easier to understand.
