# Google CSSI Curriculum
This is the CSSI Curriculum site code.

## Developing the site
The site uses Jekyll, so that we can write curriculum in markdown (mostly just plain text) and then get it turned into HTML pages automatically. Development is pretty easy, especially if you are just adding content - things should 'just work'.

### Getting Started
Check that ruby is installed, and check your version. Any version > 2 should work, but if you are hitting errors, it could be your version. Tested on version 2.2.0.

```
gem install jekyll
git clone https://github.com/google-cssi/cssi-curriculum.git
cd cssi-curriculum
jekyll serve
```

Jekyll will build the site and make it available at localhost:4000 (by default - check the output to see which port it chooses for you). By default, it will also watch for changes, so when you save changes to the files, Jekyll will rebuild the site and your changes will be there on refresh.

# August 2015 CSSI Curriculum Notes

## Git + Github

+ Emphasize the concept of source control
+ An kinesthetic example: boxes and envelopes

## Commandline

## Python

### Pacing and Order

+ Strings methods need to be taught before function labs because many function labs include string methods.

### Content

+ Math operators and string methods are boring to teach in isolation; they don't represent basic, reusable concepts but instead targeted solutions for particular problems.  For reference, structuring the material this way makes sense but for introducing them it makes more sense to not have the instructor present them but to have a guided lab introduce them.
+ One way to introduce loops, lists and conditionals is to using the running example of "print all the days in the year (Jan 1 .. Dec 31)" and then worked on simplifying that to introduce loops and lists (and then conditionals to get st/nd/rd/th suffixes).

### Instructional Delivery Methods

+ If the room allows, try to have the split screens: a terminal window (or reference slides) and an IDE atom window. If this isn't possible, consider sharing a Drive folder with the students so they could see the up-to-date code .
+ Use the whiteboard to draw out concepts. For example explain how a list is like a shelf of library books. Each book has a title and an index position.

### Labs

+ The calculator lab has been changed to “make your own 80’s console game”. Students had 60 mins, students presented their game, their code, what they learned, and what they would do with 10 more mins
+ We added a more pre-defined class practice

###
Resources
[Python Day 1 Slides](https://docs.google.com/presentation/d/1iBtVKKKOnQnkRm8l6fdNZ4yTraAUJY3E9P4NN1yp1NU/edit#slide=id.p)
[Python Day 2 Slides](https://drive.google.com/a/google.com/file/d/0B6pApRDFq-1xeXE1QmNwVHVqQjVtV3hNcGV3bkRJdzdmMm1N/view)
[Python Reference](https://docs.google.com/presentation/d/1Bkp06RgtEz11yv9zi7Ox5KfFE1Cd7560z_Of-OgFMqI/edit#slide=id.g18ddb800f_00)

## HTML/CSS

### Pacing and Order

+ Students will be creating a repository on github named "username.github.io" on github.com with an index.html. The will clone it and work off of this file for their personal page lab.
+ Added a more explicit an explicit lesson on display + positioning and the box model.

### Content

+ Consider introducing elements that are by default inline vs block when teaching HTML. It is not a hard concept for students to grasp (Block: expands whole page, flows up and down; Inline: extends content and flow left to right)
+ HTML forms are not introduced until AppEngine week since forms without backend don’t have much use.

### Labs
+ The empire state lab can be used as a code-along for CSS positioning/display and box model:
https://github.com/google-cssi/hs-empire-state-css-challenge

+ Added activities from Victoria:
HTML: https://screenshot.googleplex.com/wV4kEYSvrvk.png
Basic CSS: https://screenshot.googleplex.com/L8wVXoi8qeC.png
Intermediate CSS: https://screenshot.googleplex.com/b7YuGbLP9Xu.png
Advanced CSS: https://screenshot.googleplex.com/O3nrgkkdNAf.png
Additional CSS activities: https://github.com/google-cssi/advanced-css-review

### Instructional Delivery Methods

+ In the HTML and CSS lessons, the Instructor should spend more time in the editor than in the deck
+ Split screen so that code and browser are up

### Resources

+ [Rachel's CSS Slides](https://docs.google.com/presentation/d/1ujMCHKYeun-dwxhsoEsVqis0-47Kyng0TJKBKjwHgnM/edit)

+ [Victoria's Advanced CSS Slides](https://docs.google.com/a/google.com/presentation/d/1wBTSbcPq-WvEd1PntsDpBcXIoAg94BrdZjIFxvfA5Cs/edit?usp=drive_web) (Slides are in a different order than CSS lesson.)

## JavaScript/jQuery


## App Engine
