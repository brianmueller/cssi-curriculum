---
  layout: post
  title: Lab - Users API - Admin Page
  language: app-engine
---

If you've ever maintained a blog with a popular service like tumblr or wordpress, you might be familiar with the feature: if a random person visits your page's url, they see your profile or posts. If you, the site administrator, log in and visit your home page, you get an admin dashboard, where you can create, edit, and delete posts.

## Instructions
Create a new App Engine app. Create a handler that checks whether a user is logged in. If they are logged in, check if their userid is equal to yours - the admin user. If so, show an admin page.

If they are not logged in or the user id is not the admin user, show a landing page. The landing page should display the userid if they are logged in, and a link to login if they are not.

## Stretch
Practice your templates and datastore!
+ Display posts on the landing page
+ Allow admins to create posts on the admin Page
+ Allow admins to edit and delete posts

## Super Stretch
+ Allow users to create their own blogs with posts - they should be the admins of their own pages, and other users should see the posts.
