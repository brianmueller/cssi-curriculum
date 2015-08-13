---
  layout: post
  title: Datastore Intro
  language: app-engine
---

##  What You Will Learn:

+ Understand what Datastore does and why it is useful
+ Store, query, and delete data in Datastore from an AppEngine app
+ Use the Datastore viewer to see the contents of your Datastore
+ Create new data models to solve a problem

##  Why This is Important / Why Should You Care?

The apps we've created so far have been kind of dumb. They can't remember anything between one request and a second request, unless we keep track with a query string or in the post request directly before. A *database* solves that problem by giving you a way to save information for later retrieval.

*Datastore* is a database provided as part of App Engine. We can use it in our App Engine apps to store data in one request and then retrieve it in another request.

##  Lesson Plan

### Getting Started
You can work in an existing app, a new python script or the Interactive Console - which can be found by going to your administrative port for any existing app. You can find this port number in the third column of the  GoogleAppEngineLauncher GUI.

After you click on Interactive Console, you'll see a lot of default imports and a pprint statement.
You won't need the pprint statement and will need to make sure that ndb is being imported.

Regardless of how you choose to practice using datastore, you will need to import ndb using the command below. ndb stands for new database.
```python
from google.appengine.ext import ndb
```

###  Creating a Model

Before we actually store data, you need to figure out how to structure it. The structure of our data is called a model. This is like a giant spreadsheet. Each column of the spreadsheet is a property and each row is a new entity.

For example, let's pretend we wanted to think-through the model for a Student. A student will have a name, a university, and a birthday. Students don’t have to provide their birthday though. These parts of a student (name, university, birthday) are called properties. Notice that properties have a type. In this case, we are using strings (for name and university) and an integer (for the age). Properties can also be required or optional.

```python
class Student(ndb.Model):
  name = ndb.StringProperty(required=True)
  university = ndb.StringProperty(required=True)
  age = ndb.IntegerProperty(required=False)
```



###  Creating an *Entity* from the model

An entity is like a row in a table, it is a new instance of a model. In this case, we're going to make a new student, student1. In order to store that new instance, we need to use the .put() method.

```python
student1 = Student(name="Adina Wallis", university="U. Mich.")
student1.put()
```

We create the Student *entity* on the first line and then we store it in the database with the method call to `put()`.

###  Running the code with App Engine
In order to see your database changes reflected immediately in your website run the server with the following command:

```
dev_appserver.py --datastore_consistency_policy=consistent [path to your App Engine code]
```

If you are in the folder that has all your App Engine code then the `[path to your App Engine code]` is `.`, period.

If you prefer to work from the GUI instead, you will need to refresh the page after you put things in the database to see the new items on the page.  

###  Datastore Viewer

App Engine conveniently provides a way to look at the actual data in the datastore.  This is like looking at the entire 'spreadsheet' of the database. All you need to do is navigate to `http://localhost:8000/datastore` in your browser.

###  Adding another student

Below is a full example of how you can add a new student, cool_kid to your datastore. Notice that student1 is no longer within our code. This is because everytime the code is executed, a new student1 will be created unless we comment the .put method out.

```python
from google.appengine.ext import ndb

class Student(ndb.Model):
    name = ndb.StringProperty(required=True)
    university = ndb.StringProperty(required=True)
    age = ndb.IntegerProperty(required=False)

student1 = Student(name="Adina Wallis", university="U. Mich.")
#student1.put()
cool_kid = Student(name="The Fonz",university="cssi")
cool_kid.put()
```

###  Datastore Keys

When we store something in the datastore using the `put()` method it returns a *key* which allows us to retrieve the stored entity immediately after it is stored.

```python
#student1 = Student(name="Adina Wallis", university="U. Mich.")
#student1.put()
#cool_kid = Student(name="The Fonz",university="cssi")
#cool_kid.put()
student2 = Student(name="Christina Ernst", university="University of Illinois")
student2_key = student2.put()
```

###  Getting an Entity with a Key with .get()

To retrieve an entity with a key we use the `get()` method. (put...get... get it!)

```python
print student2_key.get().name
```

###  Querying from the Datastore with .query()

To access all of the students that we may have stored we would make a `query()` on the `Student` model, and then fetch it. Like so:

```python
student_query = Student.query()
student_data = student_query.fetch()
```

This is like forming the question "Do you have any Students?" with `.query()` and then asking the question and getting a response with `fetch()`. The fetch() method returns a list and can be iterated upon just like any list. So student_data[2] would give us the third student in datastore. However, datstore does NOT return a specific order. So just because Adina Wallis was the first student we put into datastore, she will not necessarily be the first student in the student_data list.

####Ordering Query Results with .order()
If you want to return your results in an order, you can chain a .order() method after the .query() method, where the pararmeter is the property you want to sort by. By default, the order is ascending. You can reverse the order by putting a negative sign before the property
```python
#sorts all students by name from A-Z
Student.query().order(Student.name).fetch()
#sorts all students by university from Z-A
Student.query().order(-Student.university).fetch()
```

####Filtering Queries using .filter()
If we want our query to be filtered based on a certain result, we can add our filters as a parameter to the .query() method. You will also need to use .filter()

Notice that we are using double equal signs because this is a comparison, not a variable assignment.

```python
adina = Student.query(Student.name=="Adina Wallis").fetch()
```
`adina` is a list containing any object with a name of Adina Wallace. If we wanted to change a proeprty of that object, we can access it just like any other object property, by using . and then the property name - so .university or .name.

However, since .fetch() is a list, we need to access the first element by using an index -  `adina[0].university` will return "U. Mich.".

#### Updating Properties
To update an object's property after you have already put that object in datastore, you need to query to find that object, and then you can index through the object like any other object.

Let's say we wanted to change The Fonz' university to specify which CSSI site he was attending. We first query the Student class, to find the exact object where the name is The Fonz.

Then we access his university property and reassign it to "CSSI Chicago". Finally we need to .put() the object so that the changes are actually stored in datastore.

```python
the_fonz = Student.query(Student.name=="The Fonz").fetch()[0]
the_fonz.university="CSSI Chicago"
the_fonz.put()
```

####  `.get()` vs `.fetch()`

There is another method similiar to `fetch()` that also retrieves data from the datastore which is `get()`.  The difference being `fetch()` can get multiple records while `get()` retrieves a single one.

###  Deleting a record

Once you have an object (in this case `the_fonz`) you can use the key to delete it from the database:

```python
the_fonz.key.delete()
```


### Keys and IDs
Keys and ID's allow both developers and the servers that host your data a way to keep track of each new object (entity) that you add to your models. IDs are unique, short strings that allow developers to access a specific entity. Keys are unique, longer strings that help AppEngine actually store and access that data. Both of these automatically get generated whenever a new entity is created in datastore.

#### IDs
Each entity that you create has an id property.  This  is a 12 digit id that is autogenerated by Datastore, unless you manually assign the id when you first created the object.[StackOverflow on Manually Assigning ID's](http://stackoverflow.com/questions/13058327/google-app-engine-ndb-custom-key-id) It is generally best to let AppEngine handle assigning IDs to new entities so that you can ensure they are all unique.

#### Keys
A key is like an ID in that it is unique to each new entity. It is also autogenerated by AppEngine whenever a new entity is put into datastore. The difference is that this key is a longer string, containing all sorts of characters. This key helps servers know where in the large cloud-network of servers the memory for your exact entity is being stored.


###  ndb.Key & get_by_id()

In some cases, you might have an id for an object - like if it was passed through a url or another script. In this case, you can build a key from a type (the name of the model) and id . This is called the Key object constructor.

This is really useful because you don't have to query and filter for the object, you can just build the key and then use the key to view and update the object's properties.

```python
key = ndb.Key('Student', id)
```

Now we can get that student from the database.

You can also get the id of a key and get an entity from the id using the methods `id()` and `get_by_id(ID)` like so:

```python
id = key.id()
student = Student.get_by_id(id)
```

We can also use a key in a url using the urlsafe() function:

```python
#  Get id and navigate to that url
self.redirect('/view_student?key=%s' % key.urlsafe())

#  Get an entity from an ID
key = ndb.Key(urlsafe=self.request.get("key"))
student = key.get()
```

##  Conclusion / So What?

Databases allow developers to store information in between user sessions. This opens up a world of possibility and allows for amazing and complex interactions with software. Websites and Apps can now remember things about their users.

##  Hints and Hurdles

+ Make sure you call `put()` when writing to the database or your *entity* won't get saved.

## Resources

+ [Slides by Luis Ibanez on Datastore](https://github.com/google-cssi/datastore-slides) : Just open index.html
+ [Review and walkthrough slides by Victoria Kirst](https://github.com/google-cssi/cssi-9-datastore-review)
