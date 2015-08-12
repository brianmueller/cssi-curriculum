---
  layout: post
  title: Appengine Launching Exercise 1 & 2
  language: app-engine
---

## Roll Dice on the Web

We can put the Dice Roll Game from Day 5's labs, your dice-rolling program on the web.

Open the GoogleAppEngineLauncher and go to File | New Application....

Enter "dice" as the Application Name, browse to your dev directory in the "Application Directory" field, and enter "8082" in the Port field.

Click the "Run" button in GoogleAppEngineLauncher.

This creates a new dice directory with app.yaml and main.py files in it. Open this file to see what they look like. Go to `http://localhost:8082/` and see what happens.

### Task 1:
Copy your dice-rolling program into main.py and modify it so that it writes a list of die rolls when you go to `http://localhost:8082/roll.`

### Task 2:
Modify your program so when you go to http://localhost:8082/roll?times=5 it prints 5 dice rolls, when you go to http://localhost:8082/roll?times=30 it prints 30 dice rolls, etc..

## Prime App Challenge

When you finish these exercises, you can take the Prime Challenge. Modify the primes app from the 6.3 Logging and Debugging Lesson, according to the following specification:

### Basic Check

`/check` should check whether a given number is prime.

`/check` should continue to accept the n URL parameter and check whether it is prime, showing either "n is prime" or "n is not prime" (upper/lowercase doesn't matter).
If no parameter is provided, /check should show instructions for how to use it.

### Basic Generate

`/generate` should generate prime numbers up to a limit.

`/generate` must accept a limit URL parameter and output a series of whitespace-separated prime numbers up to (and including) the limit. For instance, `/generate?limit=15` should output "2 3 5 7 11 13".
If no limit parameter is provided, `/generate` should show instructions for how to use it.

### Home Page

The home page (/) should describe what the app does and provide some sample links to to /check and /generate pages with example parameters.

### Advanced Check

`/check` should behave gracefully regardless of the input. For instance, if the user tries to visit `/check?n=monkeys`, your app shouldn't throw a 500 error. I will try to break your app, so try to think of all the problematic input I might send.

### Advanced Generate

`/generate` should handle bad input data gracefully.

### Fast Check

`/check` should run as fast as possible. Note that the IsPrime method we've already introduced is inefficient, especially for large numbers. You can do better.

### Fast Generate

`/generate` should run as fast as possible.

Your apps can be evaluated on (a) how well your app meets this spec, (b) how well you handle bad input, and (c) how fast your functions run.
