---
  layout: post
  title: Teamwork with Git - Merging
  language: git
---

## Merging
It can be complicated bringing together files when different changes have been made to the same starting point. Git helps you decide which versions to keep, and which ones to get rid of. Let's walk through a scenario that you'll run into as a team.

You create a repository for your team. Your local files are in sync with the version you push up to Github. Life is good.

Your team gets to work. You make some local changes, add and commit them. You make more changes, and add and commit them. Your teammates do the same, working on their parts of the project.

Uh-oh. Your teammate pushed changes up to Github. Now the version that you are working on is weirdly out of sync. The history of your files diverged from the history of the files on the remote repository.

You want all the changes to still exist - you don't want to erase your changes or the ones that your teammate made.  

<img src="https://www.atlassian.com/git/images/tutorials/collaborating/using-branches/08.svg" width=500px >

This happens all the time. Thankfully, git has an answer for this problem. **Merging**.

We'll talk about two kinds of merges. In one case, you and your teammate each edited different files, so there are no questions about which changes are 'right'. In the other, you have each made changes to the same file, so there is the extra step of resolving the merge conflict - deciding whose changes to keep. Git allows us to make very fine-grained decisions about which parts of which changes we want to keep - if we want some of one and some of the other, we can do that.

Let's start with the commands to run in the first scenario, without any merge conflicts.

Without any merge conflicts, here is a sample session.

```
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean

$ git pull
Merge made by the 'recursive' strategy.
 python-user-mini-app.md | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)

$ git status
On branch master
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean

$ git push
Counting objects: 5, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 632 bytes | 0 bytes/s, done.
Total 5 (delta 3), reused 0 (delta 0)
To https://github.com/google-cssi/student-labs.git
   2827bdc..1e389bb  master -> master

$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```
We use $ git pull to fetch the files from the remote and merge them into our branch. Nothing was in conflict, so git was able to merge the changes automatically. After we pulled, we pushed our changes up to the shared repository, so that everyone can be in sync.

First, let's see the error that happens when we try to push without pulling first. Next, we'll take a look at what happens when we have conflicting edits to the same file.

Assuming your teammate has pushed changes up, and you have committed changes.

```
$ git push
To https://github.com/google-cssi/student-labs.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/google-cssi/student-labs.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
The remote repository rejected our changes! It tells us we need to pull down the changes first, before we can push our own up. Let's do that:

```
$ git pull
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (1/1), done.
Unpacking objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 3 (delta 2), pack-reused 0
From https://github.com/google-cssi/student-labs
   1e389bb..00c80da  master     -> origin/master
Auto-merging python-user-mini-app.md
CONFLICT (content): Merge conflict in python-user-mini-app.md
Automatic merge failed; fix conflicts and then commit the result
```
Uh-oh! Last time, the automatic merge worked. This time, git notified us that there are conflicting files. We have to resolve the conflicts before the merge can finish.

Let's check git status to see what we have to do.

```
$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 1 different commit each, respectively.
  (use "git pull" to merge the remote branch into yours)
You have unmerged paths.
  (fix conflicts and run "git commit")

Unmerged paths:
  (use "git add <file>..." to mark resolution)

	both modified:   python-user-mini-app.md

no changes added to commit (use "git add" and/or "git commit -a")
```
Helpfully, the process for resolving conflicts is the normal git workflow - we edit the files that were in conflict and add and commit them. In this example, the conflict is in python-user-mini-app.md.  So let’s open python-users-mini-app.md in Atom and take a look at the conflict.
 (This is just a piece of the larger file - we only care about the section marked off by <<<< and >>>> marks.)

```
The second thing to remember is that `raw_input()` also takes one line of input, so once the user presses enter, their input data is complete.

###  The Challenge: A Visit to My Favorite City
<<<<<<< HEAD
You're going to build a program that plans tourists' visits to your favorite city. Create a new file with `touch trip.py` in terminal. Open `trip.py` with Atom to start writing your program - `open -a Atom trip.py`.
=======
 Let's build an application to plan a tourist's visit to your favorite city. You are going to need to create a new Python file by entering `touch trip.py` into your terminal. Open `trip.py` with Atom to start writing your program.
>>>>>>> 00c80daf87af9e36c33fa71b4fb643804fb572f6

You'll want to ask the user where they would like to stay
```
Git has put the two versions of the text next to each other. Your version is on top - the HEAD, and the version from your teammate's commit is below. Those strange numbers and letters are the id for that commit. The <<<, ====, and >>>> marks separate the conflict from the rest of the file.

We can see the different versions side-by-side. In order to resolve the conflict, we edit the document to be the way we want it to end up. We can delete one version and keep the other, keep parts of both, or write something new. Whatever we do, we need to remove the separator marks, and add and commit the changes. Here's how I resolved this conflict:

```
The second thing to remember is that `raw_input()` also takes one line of input, so once the user presses enter, their input data is complete.

###  The Challenge: A Visit to My Favorite City
Let's build an application to plan tourists' visits to your favorite city. Create a new file with `touch trip.py` in terminal. Open `trip.py` with Atom to start writing your program - `open -a Atom trip.py`.

You'll want to ask the user where they would like to stay
```
Notice, there is only one version of the text there now, and the marks are gone. In order to finish the merge, I need to add and commit this change.

```
$ git add python-user-mini-app.md
$ git commit -m "resolved conflict between the versions"
[master 8d1b454] resolved conflict between the versions
```
Great! Now my local version has the updates from me and my teammate. I can share the merged version the way I share anything - push!

```
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean
$ git push
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 784 bytes | 0 bytes/s, done.
Total 6 (delta 4), reused 0 (delta 0)
To https://github.com/google-cssi/student-labs.git
   00c80da..8d1b454  master -> master
```
Hooray! We resolved the merge conflict, and no one's edits got erased.

* [Getting Git Right](https://www.atlassian.com/git/)
