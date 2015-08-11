---
  layout: post
  title: Lab: Python String Methods - Invitation Maker
  language: python
---

<img src="https://s3.amazonaws.com/after-school-assets/weasley.jpg" width="150" align="left" hspace="10">
Ron Weasley is graduating from Hogwarts! He's got Percy Weasley's graduation invitations from a few years ago, which Percy wrote out by hand before sending them via owl post. Percy could have saved a lot of time by using the magic of programming to automate this task. Help Ron get these invitations printed quickly so he can spend more time playing Quidditch.

How can you automate this task? There are the few ways we can do this...

####  str.replace
The `str.replace` method is a handy python tool that allows you to substitute a word or letter for another word or letter within a string. That means *every time the word or letter appears in the string, it will be substituted out.* Let's take a look at how that works.

We have a fact about a bug assigned to a variable `wrong_fact`:

```python
wrong_fact = "Ladybugs can taste with their feet."
```
But wait, that's not a fact about ladybugs, but butterflies! Let's swap out the word "Ladybugs" for "Butterflies" using the str.replace method.

`str.replace` takes two `parameters`. *The first one is the word you want to replace, and the second one is the word you want to replace it with*:

```python
right_fact = wrong_fact.replace("Ladybugs","Butterflies")
```

The `return value` (aka what this action produces after it's called) will be "Butterflies can taste with their feet." Then, if we type `right_fact` into our console, we'll see the fact correctly printed.

###  Chaining str.replace

What if you have a sentence that you want to substitute more than one word in? We can do that by calling `str.replace` more than once on the same line, through a process called `method chaining` in which you *call one method right after another*. Take a look:

```python
wrong_fact = "Cats fail to recover about 50 percent of the nuts they bury."
true_fact = wrong_fact.replace("Cats", "Squirrels").replace("50", "74")

```

###  Challenge 1 (using str.replace):
Create a new python file where you will code your solution. In terminal, type `touch invitation.py`.

Copy the variable definition below, which is the original invitation that Percy used for his graduation, and paste it into `invitation.py`.

```python
percy_invitation = "The family of Percy Weasley proudly invite you to their graduation commencement on Saturday the 22nd of May 1993. Festivities will be held at The Burrow. See you then!"
```

Ron plans to have his party on May 18th, 1997 (Sunday). In `invitation.py` use chained str.replaces to customize the invitation for Ron. Remember to use puts to output your solution to the screen.

###  Challenge 2 (using string interpolation):
It's 1998 and time for Ginny's graduation. Ron wants to help his little sis out. Instead of using str.replace, let's use string interpolation to change the content of the invitation. Create a file for Ginny's invitation. In terminal, type `touch ginny_invitation.py`. You'll code your solution in that file.

Copy Percy's invitation into ginny_invitation.py again.

```python
invitation = "The family of Percy Weasley proudly invite you to their graduation commencement on Saturday the 22nd of May 1993. Festivities will be held at The Burrow. See you then!"
```

Now that you know what string interpolation is, assign the following content from Percy's invitation to variables in `ginny_invitation.py`:

1. name, 'Percy'
2. the day, 'Saturday'
3. the date, '22nd'
4. the year, '1993'

Now that we have Percy's information, it's time to change the value of these variables to reflect Ginny's info. Ginny plans to have her party on May 17th, 1998 (Sunday).

Use string interpolation and the variables you just created to customize Percy's invitation for Ginny. As in Challenge 1, you'll want to use puts to print out your solution to the screen.
