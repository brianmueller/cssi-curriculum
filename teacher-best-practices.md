# Best Practices for Teaching at CSSI

###Delivering content:

+ Why is your lesson important- Every lesson should start with a WHY. Why is this topic important, relevant and exciting?! Find ways to connect with student's background knowledge and every day life.
+ Chunking lectures- Stop after each new skill and ask the class to rank their understanding from 1-5 or show a thumbs up and thumbs down. Rule of thumb is with every new skill students should have at least 10 minutes of practice.
+ Talk aloud- When you are coding to talk through your thought process. When you run into an error DON'T PANIC, model debugging and searching for documentation.

###Check for student understanding:

+ Fist to Five- Ask students how comfortable they feel by showing 1-5, one being they need help from a teacher, 3 being they need more practice, and 5 being they could teach this to another student. Consider introducing the eyes closed fist of five which can be more illuminating and helpful.
+ Awkward silence- After you ask a question, allow the silence to linger a little longer than is comfortable can get students to speak up. If no one speaks up that is a sign that the class didn't understand the concept. Go back and reteach the last skill.
+ Calling on Students- Avoid calling on the same students that always raise their hands. Call on quiet students with review questions, call on table teams to answer questions as a group, and have students turn to their partners to answer the question.
+ Affirm and Redirect- When students give the incorrect answer, acknowledge their answer is wrong but affirm their thought process. "That's not it, but I can see how you came up with that answer."
+ Loop back with students- When a student gets the wrong answer, feel free to ask another student but try to come back to the same student and ask the same question again to ensure they understand the concept.

###Individual lab work:

+ Don't give away the answer- Coach students towards answering their own question rather than giving them the answers. Encourage them to search online for documentation or direct them towards where their error message might be.

###Group work:

+ Have students pair program as much as reasonable. Half of the class has their laptops closed and students talk through their thoughts as they code. It works best if you explicitly assign partners for coding.

###Culture and motivation:

+ Encourage rubber ducky debugging. Have students explain their code before you giving trying to help find a solution to their code.

###Logistics:

+ Use the same technology and environment (editor, terminal, etc.) as the students
+ Incorporate live coding in your lessons when possible. Slides are great for reference but they should not be the majority of your lesson.
+ Practice with git and Github before project week. It's super helpful to be familiar with the bugs that students will see before they see them.
+ Begin each day with a review session or independent lab time.
+ Insist on organizing folder structures from day 1. When using Atom make sure to only have the file that is meant to be changed open.
+  Many students did not attend breakout sessions if they were phrased as review or beginners. Phrase breakout sessions to be topical rather than review/advanced
+ Develop a glossary for all the new terms students learn for each language. It can be a shared google doc or written on poster paper.

# CSSI Curriculum Notes

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

Labs
The empire state lab could be a good code-along (CHI)
CSS labs would be stronger if they had specific styles/layouts to try to emulate rather than completely open ended. (NYC + SEA)
The github lab was confusing -- it had errors, lacked detail and I never got the "push to make a new page" to work.(CAM)
The HTML / CSS lab about the album cover forced very heavy use of presentational HTML, using headers in a non-semantic way and generally undercutting the whole message about separation of concerns. It would be a great lab if everything done with headers had been done with paragraphs instead! The CSS file there was full of weird browser-specific stuff that the kids shouldn't need to know or see. (CAM)
Labs to potentially incorporate from vrk@google.com (NYC):
HTML: https://screenshot.googleplex.com/wV4kEYSvrvk.png
Basic CSS: https://screenshot.googleplex.com/L8wVXoi8qeC.png
Intermediate CSS: https://screenshot.googleplex.com/b7YuGbLP9Xu.png
Advanced CSS: https://screenshot.googleplex.com/O3nrgkkdNAf.png

Instructional Delivery Methods
The lessons should be less deck heavy and more practice driven. While decks are useful references, the Instructor should spend more time in the editor than in the deck (MTV+CAM)
split screen so that code and browser are up (CHI)
Possibly make the username.github.io first (before making the profile_page.html and style.css pages) so that we don’t have to move files around (CHI + MTV)
I think some of the material needs a strong narrative. For example, the CSS section talks about the different selectors, but it was tough for me to translate that into a narrative or metaphor for the students (granted that is sometimes a hard thing to do!) (CHI)
Might want to consider setting up a CSSI specific yaqs/stackoverflow group to encourage students in searching for answers online, becoming a part of the online coder community, get used to asking questions and learn how to properly frame a question that will help them.

Resources
Intro to CS Deck
CSS Deck


## JavaScript/jQuery
+

## App Engine
+
