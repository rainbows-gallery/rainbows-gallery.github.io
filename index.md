<img width="600px" class="text-center p-4" align="center" style="padding:20px" src="/Images/logo.png">

# Overview

**The Problem**: UH students who paint, draw, sculpt, photograph, and so on do not have a public place to showcase their art to other individuals. Although there is the Manoa Creative Production Discord server, it is not a convenient place for people to look at a specific person’s art, nor a place for sculptures, photographs, ceramics, etc.

**The Solution**: The UH Student Art Gallery allows users to post images of their art for anyone to view. Users will be able to add comments under artworks and star posts they like for easy reference.

# Outline

## Landing

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/Landing.png">

This image shows the landing page of our application. Each of these photos can be clicked to view in greater detail. Until you log in, however, you will not be able to comment or star posts. 

## Photo Interaction

<img width="600px" class="text-center p-4" align="center" src="/Images/M1/PhotoInteract.png">

This page presents when a user clicks on an image. This page shows the image in a larger size, the username which uploaded the image, a short description of the image. This page also allows for commenting on the post, as well as "starring" or sharing the image.

## Sign Up 

<img width="600px" class="text-center p-4" align="center" src="/Images/M1/SignUp.png">

This is the current rendering of the sign up page. When starting up, the site asks for entry of a username, email, and password. The "Already have an account?" link is functional and takes you directly to the sign in page. 

## Sign In 

<img width="600px" class="text-center p-4" align="center" src="/Images/M1/SignIN.png">

This is the current sign in page. It requests a username or email from the user. Username log in does not currently work for defaults, but works if a new account is created. The "Don't have an account?" link is functional and takes you directly to the sign up page. 

## Home 

<img width="600px" class="text-center p-4" align="center" src="/Images/M1/Home.png">

The current rendering of home is nearly identical to the landing page with the exception of navbar items. In the future, continuous image rendering will be implemented, to provide images from followed users upon scrolling down. 

## Profile
<img width="600px" class="text-center p-4" align="center" src="/Images/pages/profilepage.png">

The profile page displays the user's title, username, a short artists statement, and a gallery of all the images the user has posted. From this page the user has the ability to navigate to the edit profile page. Currently, there is no implemented rendering of the Profile page. 

### Edit Profile
<img width="600px" class="text-center p-4" align="center" src="/Images/pages/editprofile.png">

The user may change their title, username, and their short description on the edit profile page. Currently, there is no implementation of the edit profile page. 

## Studio
<img width="600px" class="text-center p-4" align="center" src="/Images/pages/studioMockup-Figma.png">

This is what the studio page may look like. Users will use the studio page to add artwork to their profile and the gallery. Currently, there is no implementation of the studio page. 

## Search
<img width="600px" class="text-center p-4" align="center" src="/Images/pages/search-page-mockup.png">

This page displays any profiles whose username matches what was entered into the search bar. The user is able to click on one of the entries and view the other user's profile. Currently, there is no implementation of the search page. 


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
