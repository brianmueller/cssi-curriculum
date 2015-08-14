# Best Practices for Teaching at CSSI
### Instructional Strategies

|Teaching Strategies|How to Do it|CSSI Example|Video Example:|
|---|-----|---|--|
| Check for Understanding(CFU)|Checks for Understanding are pre-planned questions that assess whether students are understanding the material you present. Ask a question after every new skill to make real time decisions about moving forward or reteaching a concept.|If the number 24 is in between quotes is it consider a string or a number? Why? |https://www.youtube.com/watch?v=atTFFzcvqfE |
|Temperature Check |Temperature checks are different ways to get student feedback from the entire class instead of just one student. This can be a simple “thumbs up” or “thumbs down” or a “fist to five” After taking the temperature, make sure you act on it: you can do a turn and talk or jot down student’s names to check in with them later|“We just learned javascript objects. Show me a fist to five (1 if you need help from a teacher 2 If you need help from a partner 3 you are doing okay 4 You feel confident in your understanding 5 You can teach this to someone else) Turn to a partner and whoever has the highest number explain the concept.|https://www.youtube.com/watch?v=z-Foqskz-1M|
|Stretch It|Rather than stopping after a student gives you the correct answer, follow up with questions that extends knowledge.  Ask students how they got the answer, what is another way to get the answer, what is the evidence, how to apply the same skill in a new situation, and what more specific vocabulary words they can use.| Teacher: What does HTML do? Student: It add’s the text to a webpage Teacher: What else can HTML do? Student: You can add headings, paragraphs, images, and links.|https://www.youtube.com/watch?v=Bvi3RNJwZbQ&list=PLUwH7So8QQPZ4W_t-Gfc8vfi5_9yN7cZD   |
|Cold Call|Call on students regardless of whether they’ve raised their hands. It increases engagement because students don’t know when they will be called on, so there is a strong incentive to do the work to be prepared to be called on. Cold Calling is not a “gotcha” technique for students who are not paying attention. It should be framed in a positive light.|For example, you ask a question, pause, and then call on a student, “Tell us one example of a datatype, please, Darren.” Notice how the name comes after the question so that all students are still thinking about the answer in case they need to share|https://www.youtube.com/watch?v=PY4l9J7V0QQ|
|Think-Pair-Share|Think-pair-share (TPS) is a collaborative learning strategy in which students work together to solve a problem or answer a question about an assigned reading. This technique requires students to (1)think individually (2) pair with classmates and discuss (3) share students share out to the class | Take a moment to think about situations where it would make sense to use a file script vs the interactive mode. When I say go, pair with a partner and together come up with at a scenario where you might want to use a file and one where you might want to use the interactive mode. |https://www.youtube.com/watch?v=KAPyC-NrUS8 |
|Think-Aloud|With this strategy, teachers narrate aloud their thoughts as they are demonstrating a concept.The purpose of the think-aloud strategy is to model for students how skilled learners think through a challenge.|Think-alouds are like talking out your pseudo code.“To write a conditional statement, first I need to start my conditional statement with “if.” That is the way that recognize that this will be my conditional statement. Then I need to write my condition.”|https://www.youtube.com/watch?v=oi7RfnlkTL4 |
|Wait Time|Wait a few seconds before calling on a student to answer. By waiting three to five seconds you are more likely to improve the quality of answers and the number of students who volunteer to answer.|Ask a question: What  does URL Fetch do? Even as students hands raise wait an additional 3 seconds to allow for think time| https://www.youtube.com/watch?v=YB0WElra8Eo |
|No Opt Out |When a student doesn’t know the right answer to your question tell them “I’ll come back to you” and ask another student the same question. Once the other student says the right answer come back to the original student and ask him/her to repeat the answer. This ensure that they have the correct answer.|What does CSS page do, Carol? Carol: I don’t know What does CSS page do, John? John: It provides styling for our webpage. So Carol, why is CSS important?? Carol: It’s where we get our styling!|https://www.youtube.com/watch?v=R_DfdnuBV4k |
|Circulate|Move around the classroom to both engage students and hold them accountable. Whenever the opportunity arises, try to move away from the front of the classroom and teach from the back of the room.| Whenever you are not coding or demonstrating, try to pace around the room. Ask for students to drive the coding and teach from the back of the room!|   |

###Delivering content:

+ Why is your lesson important- Every lesson should start with a WHY. Why is this topic important, relevant and exciting?! Find ways to connect with student's background knowledge and every day life.
+ Chunking lectures- Stop after each new skill and get a class temperature check (thumbs up/thumbs down or a fist to five). Consider reteaching the skill if students are confused or have students turn and talk to their partners.
+ Talk aloud- When you are coding to talk through your thought process. When you run into an error DON'T PANIC, model debugging and searching for documentation.
+ Be creative about naming variables especially when data is being passed in multiple places rather than just using x and y.

```python  
def add (dog,cat):
  return dog + cat

platypus= 50
giraffe= 20

add (platypus,giraffe)
```

### Check for student understanding:

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
