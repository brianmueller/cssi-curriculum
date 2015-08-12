---
  layout: post
  title: Cheatsheet: Git
  language: git
---

# Git

[Official Github Cheatsheet](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)
[Git-tower Cheatsheet](http://www.git-tower.com/blog/git-cheat-sheet/)

## Create
+ `git clone <repo-clone-url>` : Clone an existing repository into your current directory
+ `git init` : Create a new local repository

## Local Changes
+ `git status` : Show changed files
+ `git diff` : Show differences between modified files and the original
+ `git add .` : Add all current changes to the next commit
+ `git commit -m "<change message>"` : Commit added files with a message

## Update and Publish
+ `git push origin master` : Push the `master` branch to your `origin` remote repository
+ `git push <remote> <branch>` : Push the specified branch to the specified remote

## Global Configs
+ `git config --global user.name "John Doe"` : Configure the name associated with commits from your computer
+ `git config --global user.email johndoe@example.com` :Configure the email associated with commits from your computer
