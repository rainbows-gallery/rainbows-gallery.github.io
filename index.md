<img width="600px" class="text-center p-4" align="center" style="padding:20px" src="/Images/logo.png">

# Overview

**The Problem**: UH students who paint, draw, sculpt, photograph, and so on do not have a public place to showcase their art to other individuals. Although there is the Manoa Creative Production Discord server, it is not a convenient place for people to look at a specific person’s art, nor a place for sculptures, photographs, ceramics, etc.

**The Solution**: The UH Student Art Gallery allows users to post images of their art for anyone to view. Users will be able to add comments under artworks and star posts they like for easy reference.

# Outline

## Landing

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/Landing.png">

This image shows the landing page of our application. Each of these photos can be clicked to view in greater detail. Until you log in, however, you will not be able to comment or star posts. 

## Sign Up 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/SignUp.png">

This is the current rendering of the sign up page. When starting up, the site asks for entry of a username, email, and password. The "Already have an account?" link is functional and takes you directly to the sign in page. 

## Log In 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/LogIn.png">

This is the current log in page. It requests a username or email from the user. 

## About 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/about-page.png">

Immediately upon signing up for the first time, you will be taken to an about page that helps explain how to use the app.

## Profile

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/empty-profile.png">

If just signing up for the first time, this is what your page will look like prior to adding any posts. If you would like to add posts to your profile, you can go into the "Add Post" tab in the Navbar. 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/populated-profile.page.png">

Once you have added posts to your profile, this is what it will look like!

## Add Post

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/add-post-fill-in.png">
<img width="600px" class="text-center p-4" align="center" src="/Images/M2/add-post-sucess.png">

To add a post, click on the top box to look for a file. Fill in the description beneath the photo, then click submit. In a few seconds, you will receive an indicator that the post was successfully submitted. 

## Feed

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/Feed-NotFollowingAnyone.png">

Originally, if you are not following anyone, this is what your feed will look like. In order to start following accounts, search for other accounts in the search bar. 

## Search 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/search-results-page.png">

To search for accounts, simply enter any string into the Navbar then click enter. A page with all profiles with a potential match to the string you entered will appear. Click on the account shown to be taken to that user's profile page. 

## Someone Else's Profile 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/admin-profile-notYours.png">
<img width="600px" class="text-center p-4" align="center" src="/Images/M2/follow-functionality.png">

When you view someone else's account, you will have the option to follow them. To follow that account, simply click follow. Once you are following the account, their posts will populate in your feed.

## Feed 

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/landing-after-add-follow.png">

After you follow someone, their posts will populate in your feed. 

## Approach

The landing page will list the features of the web app, such as the gallery, posting artworks, and adding comments.

Regular users can login with their UH account, which allows them to view the whole gallery, post images of their artworks, view their posts, and add comments to other user's posts. Note that users who are not logged in are unable to access the gallery or perform the other listed actions.

Admins monitor the gallery and can delete any inappropriate posts and comments.

The gallery will initially show the most recent artworks. Users can filter for specific artworks (e.g. sculptures, digital art, hand-drawn, etc.) or user’s artworks. Alternatively, they could sort by date, alphabetically, or usernames.

Possible mockup pages include:
* Landing page
* Login
* Sign-Up
* Home
* Profile
* Studio
* Search
* Photo Interaction

# Use Case Ideas

* New user goes to landing page, browses through the art gallery, can sign up.
* User goes to landing page, logs in, gets to home page, browses the art gallery, post their own art, edit their profile, or search for other profiles.

# Beyond the Basics

Some potential advance features include:
* Implement profile pages for users
* Allow users to filter out certain artwork
* Design a role for professors or experts separate from admins and regular users

# Deployment
[Link](http://143.198.63.208/)

# Project Management Links 
* [M1](https://github.com/orgs/rainbows-gallery/projects/2/views/2)
* [M2](https://github.com/orgs/rainbows-gallery/projects/3)

# Contract Link 
[Link](https://docs.google.com/document/d/1cbQv4htZbSGHQxj_0gbgDfSVIsTfvkACISIYMw3NIY0/edit)

# Team Profiles 
* [Sienne Rodwell](https://sienner.github.io)
* [Tatum Umiaka](https://tatumumi.github.io)
* [Kobe Uyeda](https://github.com/KobeUyeda)
* [Eric Zhou](https://github.com/eric-z4)

# Link to our Organization
[Link](https://github.com/rainbows-gallery)

# How to Run Our App Locally

* Ensure you have [npm](https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager) installed and accessible
* Clone our gallery-app repository onto your local device
* cd into the the gallery-app/app folder
* run meteor npm install
* run meteor npm run start 
