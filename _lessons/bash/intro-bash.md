---
layout: post
title: Intro to the Command Line
language: command-line
---

# What You Need to Know:
+ Intro to the web
+ Github account setup
+ Learn.co walkthrough
+ Intro to HTML
+ Intro to CSS

# Student What You Will Learns:
Students will be able to navigate their system’s file structure using the CLI (command line interface) in terminal.
Understand and explain what a terminal is and why we use it
Navigate and manipulate directories

# Why This is Important?
Back in the day (the 1980s!), computers only had a terminal to control them. Later on, Graphical User Interfaces (GUIs) were created to make computers more accessible and intuitive for those who weren't as computer savvy. Developers continue to use the terminal instead of the GUI because it speeds up development and allows for more fine-grained control.

# Command Line
* Open Terminal- Either click the icon, or hit Command + space and type Terminal, then click enter. A small white rectangle will appear with the name of your computer, a tilde (~) and your username followed by a $.
You’ll see a tilde: ~. This means you’re in your user's home directory. Directory is another word for folder.

* Enter pwd : pwd means print working directory - it tells us where we are.
* Enter ls : check what directories are within the directory where you are standing by using
* Enter cd: change directories by using the cd command. Change to Desktop directory.
* Enter mkdir : makes a new directory. Make a new directory in development called around-the-world.
* Enter cd around-the-world: to change directories into around-the-world
* Enter mkdir France: creates a directory called France inside of around-the-world
* Enter cd France: to change directories into France
* Enter mkdir Paris: to create a directory called Paris inside of France
* Enter cd Paris: to change directories into Paris
* Enter touch eiffel_tower.txt: to create a text file called eiffel_tower in the Paris directory
* Enter touch berlin_wall.txt: to create a text file called berlin_wall in Paris directory
* Enter touch pyramids.txt: to create a text file called pyramids in Paris directory
* Enter rm berlin_wall.txt: To remove the berlin_wall
* Enter mv : mv pyramids.txt france/around-the-world or my pyramids.txt ../.. You have to list the path of directories in order to move the file to the final destination
* Enter cd .. to move up the tree of directories. cd ../.. will bring you up two parent directories

# Student Challenge:
1. Create a directory called "Egypt" in the "around-the-world" directory
1. Create a directory called "Cairo" inside the "Egypt" directory
1. Create a file called "pyramids.txt"
1. Move "pyramids.txt" into the "Cairo" directory. Hint: List the path from around-the-world to Cairo
1. **Stretch:** Create a new country, city, and landmark file in the "around-the-world" directory


# Tips and tricks:
 If you start typing a directory name or file name you can click `Tab` and the command line will automatically fill in the rest of the directory/file name. If you click `Tab` twice it will show you all of the directories/files inside your current directory.

 Navigating your computer from the command line is a lot about muscle memory. The more practice you have the faster you will get!

# Conclusion
As we learn to build complicated applications, being able to swiftly navigate your computer using the command line will make your life much easier. The command line will be important not just for navigation, but you'll also use it to do things like boot the local server for your web apps, write scripts to automate tasks, and execute other important functions on your computer.

##  Resources
* [Level Up - Command Line Tutorial](http://leveluptuts.com/tutorials/command-line-basics)
