---
  layout: post
  title: Lab: Python Input and Output - Jukebox
  language: python
---
##  Instructions

You're going to write a jukebox that introduces itself to the user and then asks for input.

There are a number of ways to accept user input. As an example, let's build a program that asks a user for their name and says hello to that user using the gets command.

```python
def say_hello(name):
  return "Hi {}".format(name)

users_name= raw_input("Enter your name: ")

print(say_hello(users_name))
```

Your jukebox should have four options: List, Play, Search, and Quit.

1. Open your jukebox.py file

2. First things first, give the user a menu of options.

3. The list option should output a list of songs that the user can play. It should call a method named `list_songs` that takes in the list of songs.

4. The play command should ask the user which song to play. It should call a `play_song` method that takes in the list of songs. The user should select the song number. Once the user has selected the song they want to play, the jukebox should output 'Playing Phoenix - 1901' or whatever the song name is.

5. The search option should ask for a search term and then print a list of songs that match that term. It should be housed in a `search_songs` method that does the user prompting and takes in a songs list as an argument. Use a [list comprehension](https://docs.python.org/3/tutorial/datastructures.html# list-comprehensions) in this method.

6. If the user types in `quit`, the jukebox should say goodbye and the program should shut down.

Think about the following things:
  * How to keep the program running until the exit command is
executed (Hint: Loop maybe? Loop upon a condition)
  * How to normalize the user's input so LIST and list are the
same. (Hint, maybe downcase and strip it)
  * How to give the songs an "index" so that when you list them
out, you can refer to them by position so the user can just
type play 1 and then you find the first song. (Hint, check
out a method called each_with_index)

Bonus:
  * Get the songs to play!
