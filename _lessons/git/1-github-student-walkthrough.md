---
  layout: post
  title: Github Walkthrough
  language: git
---

#### Why This is Important
How many of you have used Google Docs? It’s a great way to store documents online and makes it easy to collaborate with other people. It works best for files like word documents and spreadsheets, but it isn’t equipped to store code.

Thankfully, there’s GitHub, which is basically the Google Docs of code. It allows developers to save code, go back to previous versions and even work on code at the same time.

Forking and cloning is a huge part of a developer workflow, so we wanted to teach you guys how it actually works.

#### Forking and Cloning
A repository is simply a place where the history of your work is stored like a folder on Google Drive. When you make a new copy of someone else's work, this is called forking. Let's practice.

We're going to fork the Spoon-Knife repository.

* Click [here](https://github.com/octocat/Spoon-Knife) to open a new tab with the repo.  
* Click “Fork” button to copy the GitHub repository
* At “Where should we fork this repository?” popup, select own account.
* GitHub then redirects to a page with your username/lab-name in URL.

Your account now has a copy on GitHub, but we can’t edit it on your computer in Atom just yet. We need to get our copy of Spoon-Knife and copy or "clone" it to our local machine.

In the right sidebar of the repository page on Github, click to copy the URL for the repository. The url should be something like: https://github.com/YOUR-USERNAME/LAB-REPOSITORY.git. This copies the url

* In terminal, in your Development directory, enter git clone and paste the URL.
Cloning a repository just means it is copied onto your computer from your github account.
Terminal will prompt you to enter your username and password. Even if you can't see your password's characters, keep typing - they're purposely hidden.

#### Github pages
Let's get a page online for the world to see!

Github, which is so cool for storing our files and the history of our commits, also has an awesome Pages feature, which lets us publish simple websites for free, all from the command line.

* Open Chrome and go to www.github.com
* At the top right click the "+" new repository
* Name your repository "firstname_lastname", make the repository public, and initialize with a README
* Copy the repository URL
* Open your terminal
* cd into your dev folder
* type `git clone https://github.com/username/firstname_lastname.git`
* cd into your my_profile_project
* mv your html and css page into your "firstname_lastname" repository
* cd into your "firstname_lastname" repository

Now we need to make a special branch or version of our work called gh-pages. This is the way that github knows we want to make a Github page form our files.

* `git checkout -b gh-pages`
* `git push origin gh-pages` (You may need your username and password again)

Now you have your very own website!!!!!! Congrats - time to send the link to the world

### Conclusion / So What?
Two words: Open Source. There are over eight million people who use GitHub to store their code. Having a free account on GitHub means that anyone in the community can fork or clone your repositories and make changes to or contribute to your codebase. It’s all about people building publicly accessible applications together.







##  Resources

* [Site Point - Git for Beginners](http://www.sitepoint.com/git-for-beginners/)
