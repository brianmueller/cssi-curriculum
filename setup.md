---
layout: default
title: Setup
---

To do the exercises in the CSSI curriculum, you'll need certain programs installed - these might be installed already, but check to make sure!

+ Python: Check with `python --version` from Terminal
+ Git: Check with `git --version` from Terminal
+ Text Editor: We have standardized around [Atom](https://atom.io/). Once Atom is installed, check that the Shell Commands have been enabled by typing `atom --version` from Terminal. If you do not get any output, click `Atom->Install Shell Commands` in the menu bar.
+ [Google App Engine SDK](https://cloud.google.com/appengine/downloads?hl=en): Check that the SDK has been installed - you should have an icon in your Applications. You'll also need the command line tools. Check that they are installed by running `dev_appserver.py` it will give a big error message if they are installed, or tell you that it is not found otherwise. Click `GoogleAppEngineLauncher->Make Symlinks` to install them if they aren't.
+ All work should be saved in a folder at `~/cssi`. Try `cd ~/cssi` - if you get a "No such file or directory" error, create the folder with `mkdir ~/cssi`, and then `cd ~/cssi` to navigate there.
