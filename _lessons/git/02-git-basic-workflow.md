---
  layout: post
  title: Github Quick Guide
  language: git
---

## When you have done some work and want to make a commit and push up your changes to your Forked Repo on Github:
1. In Terminal, make sure you are currently in the directory of the project that you want to push (`pwd` will tell you what directory you are currently in if you aren't sure)
2. `git add .`
3. `git commit -m "your commit message goes here"`
4. `git push -u origin master`

*You only need to include the -u in # 4 if it is the first time you are pushing a commit to this specific repo.*

Now your changes have been added to the Forked Repo in your Github account. At any time you can enter **git status** to see whether you have any changes that are not yet committed or whether your local repo is current with the master.


## If you want to create a pull request (to tell the original owner of the repo to check out your changes)
1. Go to your Forked Repo in your profile on Github
2. Click the little green button with the arrows on it.
3. Click green **Create pull request** button
4. Leave a message for the owner of the repo
5. Click green **Create pull request** button at the bottom of the message.

## Whenever you come back to work on a repo that someone else might also be committing changes to
1. Make sure you are currently in the right directory
2. **git pull**


Git pull is important to make sure you have the most up to date version of the repo on your local computer. This is most important when multiple people are working on and committing changes to the same repo.

## We will continue to build on our Github knowledge over the next few weeks.

##  Resources

* [Blog -Github for Beginners](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1)
