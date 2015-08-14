---
  layout: post
  title: Software Architecture
  language: project
---

# What You Will Learn:
* As a group, write the bulk of the design doc for a previous CSSI App

# Why This is Important:
* Essentially you already know how to build each component of any webapp
* When each piece comes together they become amazingly powerful
* By the end of today, you will have submitted your design doc for your group. This is a great tool to help you plan your project and the components that will make it up. You have all the skills to make an amazing web app, and today is the first step to getting it done.

# The Design Doc
By the end of today your team will have decided on what app to build and outlined the steps to make sure you are successful. The design doc is [here](https://docs.google.com/a/google.com/document/d/12qPuYRBiP1AR6rJjbyzG2p_bm--bJ5SPVWK_cTpvA8w/edit?usp=sharing). You will copy and paste the template into your own new Google Doc on your own account. Then share it with your team.

# What makes Movie Spotter Work?

 [Movie Spotter](https://movie-spotter.appspot.com/home) is an app from CSSI - Cambridge last year.

Let's think through what the heart of their Design Doc might have looked like last year. Let's look at question 7 as an example:

# 7. List specific steps you will take and milestones you’ll need to hit.
* Day 1 - Build the basic search.html view. Need a `<form>` tag, `<input name=”search_movie”>` and logging in the console so we know that the parameter is stored.
* Day 2 - determine logic to process the `search_movie` parameter and output the matching information on the results page. If there are no matches, build a condition for that. In this case, just match it against a pre-built dictionary of movies and worry about API intergration later. `award_winning_movies = {Forrest Gump {year : “1994”, link=”www.forrestgump.com”}, Lion King {year : “1992”, link : “www.thereallionking.com”}`
* Day 3 - Make API Integration. Figure out how to get the dictionary from IMDB as the comparision dictionary
* Day 4 - Style up the views and make it pretty!

Since this is a mock-up, we can be happy understanding a) what each component will look like and b) what logic we will need to implement.

# Conclusion:
Notice we don’t need to fully understand HOW to implement our logic, but rather we should have a general understanding of what technology we can use.
