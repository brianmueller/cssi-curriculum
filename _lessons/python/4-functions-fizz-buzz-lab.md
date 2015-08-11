---
  layout: post
  title: 4-functions-fizz-buzz-lab
  language: 
---


#  Test Driving FizzBuzz

_warning the test code is currently in the implementation file_

A classic programming problem is [FizzBuzz](http://c2.com/cgi/wiki?FizzBuzzTest). It is considered the [Stairway to Heaven](http://www.codinghorror.com/blog/2007/02/fizzbuzz-the-programmers-stairway-to-heaven.html) of programming because there are so many different ways to play it and everyone plays it.

The goal of fizzbuzz is to build a program that can take a number and if the number is evenly divisible by 3, it should return "Fizz", if it's divisible by 5, it should return "Buzz", and if it's divisible by both 3 and 5, it should return "FizzBuzz".

##  Defining Our Expectations

Let's approach solving this problem from a TDD approach. That means what we don't care about is "how", but rather, we care about "what". What will the program do if it works correctly, not how will it do it. We are going to write our expectations first, then our implementation.

Before we look at the Python Unit Test syntax, let's just express our tests naturally.

1. We expect fizzbuzz(3) to return "Fizz"
2. We expect fizzbuzz(5) to return "Buzz"
3. We expect fizzbuzz(15) to return "FizzBuzz"
