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

#  What you will Learn:
Students will be able to navigate their system’s file structure using the CLI (command line interface) in terminal.
Understand and explain what a terminal is and why we use it
Navigate and manipulate directories

# Why This is Important?
Back in the day (the 1980s!), computers only had a terminal to control them. Later on, Graphical User Interfaces (GUIs) were created to make computers more accessible and intuitive for those who weren't as computer savvy. Developers continue to use the terminal instead of the GUI because it speeds up development and allows for more fine-grained control.

# Command Line
* Open Terminal- Either click the icon, or hit Command + space and type Terminal, then click enter. A small white rectangle will appear with the name of your computer, a tilde (~) and your username followed by a $.
You’ll see a tilde: ~. This means you’re in your user's home directory. Directory is another word for folder.

Follow these steps to create a directory about the world and practice command line commands

* `pwd`: pwd means print working directory - it tells us where we are.
* `ls`: check what directories and files are within the current directory
* `cd ~/cssi`: change directories by using the cd command. Change to `~/cssi` directory.
* `mkdir around-the-world`: Make a new directory in `~/cssi`` called `around-the-world`
* `cd around-the-world`: to change directories into `around-the-world`
* `mkdir france`: creates a directory called `france` inside of `around-the-world`
* `cd france`: to change directories into `france`
* `mkdir paris`: to create a directory called `paris` inside of `france`
* `cd paris`: to change directories into `paris`
* `touch eiffel_tower.txt`: to create a text file called `eiffel_tower.txt` in the `paris` directory
* `touch berlin_wall.txt`: to create a text file called `berlin_wall.txt` in `paris` directory
* `touch pyramids.txt`: to create a text file called `pyramids.txt` in `paris` directory
* `ls`: check what directories and files are within the current directory, verify that your 3 files are there
* `rm berlin_wall.txt`: To remove the berlin_wall.txt
* `pwd`: pwd means print working directory - it tells us where we are, we should be in the `paris` folder
* `cd ..`: moves us into the parent folder of `paris` which is `france`
* `mv paris/pyramids.txt pyramids.txt`: move the `pyramids.txt` file from the `paris` folder into *this* folder
* `cd ..:` to move up the tree of directories. `cd ../..` will bring you up two parent directories

# Student Challenge:
1. Create a directory called `egypt` in the `around-the-world` directory
1. Create a directory called `cairo` inside the `egypt` directory
1. Create a file called `sphinx.txt` in the `around-the-world` directory
1. Move `sphinx.txt` into the `cairo` directory. Hint: List the path from `around-the-world `to `cairo`
1. **Stretch:** Create a new country, city, and landmark file in the "around-the-world" directory


# Tips and tricks:
 If you start typing a directory name or file name you can click `Tab` and the command line will automatically fill in the rest of the directory/file name. If you click `Tab` twice it will show you all of the directories/files inside your current directory.

 Navigating your computer from the command line is a lot about muscle memory. The more practice you have the faster you will get!

# Conclusion
As we learn to build complicated applications, being able to swiftly navigate your computer using the command line will make your life much easier. The command line will be important not just for navigation, but you'll also use it to do things like boot the local server for your web apps, write scripts to automate tasks, and execute other important functions on your computer.

##  Resources
* [Level Up - Command Line Tutorial](http://leveluptuts.com/tutorials/command-line-basics)
* [Image of Possible folder structure](http://i.imgur.com/ViRtnaF.png)
