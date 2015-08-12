---
  layout: post
  title: Fortune Teller Challenge
  language: resources
---

At the end of these exercises, you will have an App Engine application that performs [cold reading](https://en.wikipedia.org/wiki/Cold_reading) simulations. Set up a basic application, then read the requirements below and implement each path as specified. Note that the requirements may be vague, ambiguous, or just incomplete. Think about how you are deciding between different ways of implementing things.

## Paths

**Fortune Cookie**

Path: /fortunecookie

Requirements:

1. When a user goes to this path, they shall see an image of a fortune cookie and receive a random fortune.

2. There shall be at least ten different fortunes.


**Magic 8-Ball**

Path: /8ball

Requirements:

1. When a user goes to this path, they shall be prompted to enter a question.

2. If the user submits input that is not a question, no response shall be produced.

3. If the user submits input that is a question, the Magic 8‐Ball produces a response at random.

4. Responses shall be output in blue text in the middle of a black circle. The circle shall be made using only CSS.

5. Ten of the possible responses that the Magic 8‐ball can give shall be positive. Five of the possible responses that the Magic 8‐ball can give shall be negative. Five of the possible responses that the Magic 8‐ball can give shall be neutral. If you want, you can use the standard [responses](http://en.wikipedia.org/wiki/Magic_8_ball# Possible_answers).

**Whirlybird**

Path: /whirlybird

Requirements:

+ Colors

a. When the user visits /whirlybird, they shall be prompted to pick a color.

b. There shall be four colors: red, green, blue, and yellow.

c. Each color shall be represented by a button of that color.

d. The buttons shall be square.

e. The buttons shall be arranged in 2x2 grid.

f. The user shall select a color by clicking its associated button.

+ Numbers

a. Once the user selects a color, they shall be prompted to pick a number.

b. The user shall be allowed to pick any number between one and eight, inclusively, by clicking a button labeled with the number.

+ Fortunes

a. Once the user has selected both a color and a number, they shall be presented with a fortune.

b. Each fortune shall be at least two sentences long.

c. The sum of number the user selected and the number of letters in the color the user selected shall uniquely identify the fortune they receive. Which is to say, if that sum is equal for two different selections, the fortunes produced shall be the same.


**Horoscopes**

Path: /horoscope

Requirements:

1. When the user visits /horoscope for the first time, they shall be prompted to enter

2. Once a user submits their birthday, they shall not be prompted to enter it again.

3. Users who have previously entered their birthday:
their birthday.

4. Horoscopes shall be grouped into the twelve Western sidereal astrological signs as defined by: http://en.wikipedia.org/wiki/Zodiac# The_twelve_signs. That is to say, any two users who share the same astrological sign shall be presented with the same daily horoscope.

 a. shall receive a daily horoscope.

 b. shall be told which astrological sign their birthday corresponds to.

5. Two users who do not share the same astrological sign shall never be presented.

6. A user shall not be presented with the same horoscope two days in a row.

**Tarot Cards**

Path: /tarot

Requirements:

1. When the user visits /tarot, they shall be prompted to select either “Love” or "Wealth".

2. The Reading

a. Once the user makes a selection, they shall be presented with six cards.

i. The cards shall be selected at random from a standard tarot deck.

ii. None of the cards should be duplicates.

iii. Each card should be represented onscreen by a corresponding image. You can use these pictures, but you don’t have to: http://www.tarot.com/tarot/decks/8‐bit/box. iv.

The cards shall be arranged in three rows.

1. The topmost row shall contain one card. It shall represent “The Present” and shall be thusly labeled.

2. The middle row shall contain two cards. It shall represent “The Future” and shall be thusly labeled.

3. The bottommost row shall contain three cards. It shall
represent “The Past” and shall be thusly labeled.

b. Once the user makes a selection, they shall also be presented with a paragraph of text explaining the cards that were selected for them.

i. Each card shall have a unique interpretation.

ii. The tense of the explanation of each card shall be determined by the row in which the card appears. Cards that appear in the topmost row shall be explained in future tense. Cards that appear in the middle row shall be explained in the present tense. Cards that appear in the
bottom row shall be explained in the past tense.

3. A user shall only be able to request one reading per hour.

General Requirements

1. Only logged‐in users shall be able to visit this application’s app

2. All paths shall handle incorrect input. If a user does not know what they are doing or makes a mistake, the page shall not crash.

3. Every page shall have a header with a navigation menu that links to all of the paths.

Extra Credit

1. Update the horoscopes path so that the user selects their birthday from a calendar.
