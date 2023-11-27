<img width="600px" class="text-center p-4" align="center" style="padding:20px" src="/Images/logo.png">

# Overview

**The Problem**: UH students who paint, draw, sculpt, photograph, and so on do not have a public place to showcase their art to other individuals. Although there is the Manoa Creative Production Discord server, it is not a convenient place for people to look at a specific person’s art, nor a place for sculptures, photographs, ceramics, etc.

**The Solution**: The UH Student Art Gallery allows users to post images of their art for anyone to view. Users will be able to add comments under artworks and star posts they like for easy reference.

# Table of contents

* [Overview](#overview)
* [User Guide](#user-guide)
* [Developer Guide](#developer-guide)
* [Developer History](#developer-history)
* [Deployment](#deployment)
* [Project Management Links](#project-management-links)
* [Team Profiles](#team-profiles)
* [Future Improvements](#future-provements)

# User Guide

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

<img width="600px" class="text-center p-4" align="center" src="/Images/M2/populated-profile-page.png">

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


# Developer Guide

This section provides information of interest to Meteor developers wishing to use this code base as a basis for their own development tasks.

## Installation

First, [install Meteor](https://www.meteor.com/install).

Second, visit the [Bowfolios application github page](https://github.com/bowfolios/bowfolios), and click the "Use this template" button to create your own repository initialized with a copy of this application. Alternatively, you can download the sources as a zip file or make a fork of the repo.  However you do it, download a copy of the repo to your local computer.

Third, cd into the bowfolios/app directory and install libraries with:

```
$ meteor npm install
```

Fourth, run the system with:

```
$ meteor npm run start
```

If all goes well, the application will appear at [http://localhost:3000](http://localhost:3000).

## Quality Assurance

### ESLint

BowFolios includes a [.eslintrc](https://github.com/bowfolios/bowfolios/blob/main/app/.eslintrc) file to define the coding style adhered to in this application. You can invoke ESLint from the command line as follows:

```
meteor npm run lint
```

Here is sample output indicating that no ESLint errors were detected:

```
$ meteor npm run lint

> rainbows-gallery@ testcafe-ci /Users/sienner/github/rainbows-gallery/rainbow-gallery/app
> eslint --quiet --ext .jsx --ext .js ./imports ./tests

$
```

ESLint should run without generating any errors.

It's significantly easier to do development with ESLint integrated directly into your IDE (such as IntelliJ).

#### End to End Testing

Rainbow Gallery uses [TestCafe](https://devexpress.github.io/testcafe/) to provide automated end-to-end testing.

In the [rainbows-gallery tests/ directory](https://github.com/rainbows-gallery/gallery-app/tree/main/app/tests) contains the TestCafe test definitions. The remaining files in the directory contain "page object models" for the various pages in the system (i.e. Home, Landing, etc.) as well as one component (navbar). This organization makes the test code shorter, easier to understand, and easier to debug.

To run the end-to-end tests in development mode, you must first start up a BowFolios instance by invoking `meteor npm run start` in one console window.

Then, in another console window, start up the end-to-end tests with:

```
meteor npm run testcafe
```

You will see browser windows appear and disappear as the tests run.  If the tests finish successfully, you should see the following in your second console window:

```
$ meteor npm run testcafe

> rainbows-gallery@ testcafe-ci /Users/sienner/github/rainbows-gallery/rainbow-gallery/app
> testcafe chrome tests/*.testcafe.js

 Running tests in:
 - Chrome 86.0.4240.111 / macOS 10.15.7

 Bowfolios localhost test with default db
 ✓ Test that landing page shows up
 ✓ Test that signin and signout work
 ✓ Test that signup page, then logout works
 ✓ Test that profiles page displays
 ✓ Test that interests page displays
 ✓ Test that projects page displays
 ✓ Test that home page display and profile modification works
 ✓ Test that addProject page works
 ✓ Test that filter page works


 9 passed (40s)

 $
```

You can also run the testcafe tests in "continuous integration mode".  This mode is appropriate when you want to run the tests using a continuous integration service like Jenkins, Semaphore, CircleCI, etc.  In this case, it is problematic to already have the server running in a separate console, and you cannot have the browser window appear and disappear.

To run the testcafe tests in continuous integration mode, first ensure that BowFolios is not running in any console.

Then, invoke `meteor npm run testcafe-ci`.  You will not see any windows appear.  When the tests finish, the console should look like this:

```
$ meteor npm run testcafe-ci

> rainbows-gallery@ testcafe-ci /Users/sienner/github/rainbows-gallery/rainbow-gallery/app
> testcafe chrome:headless tests/*.testcafe.js -q --app "meteor npm run start"

 Running tests in:
 - Chrome 86.0.4240.111 / macOS 10.15.7

 rainbow-gallery localhost test with default db
 ✓ Test that landing page shows up (unstable)
 ✓ Test that signin and signout work
 ✓ Test that signup page, then logout works
 ✓ Test that profiles page displays
 ✓ Test that interests page displays
 ✓ Test that projects page displays
 ✓ Test that home page display and profile modification works
 ✓ Test that addProject page works
 ✓ Test that filter page works


 9 passed (56s)

$
```

All the tests pass, but the first test is marked as "unstable". At the time of writing, TestCafe fails the first time it tries to run a test in this mode, but subsequent attempts run normally. To prevent the test run from failing due to this problem with TestCafe, we enable [testcafe quarantine mode](https://devexpress.github.io/testcafe/documentation/guides/basic-guides/run-tests.html#quarantine-mode).

The only impact of quarantine mode should be that the first test is marked as "unstable".

## Continuous Integration

![ci-badge](https://github.com/bowfolios/bowfolios/workflows/ci-bowfolios/badge.svg) //Kobe add ours here

Rainbow Gallery uses [GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions) to automatically run ESLint and TestCafe each time a commit is made to the default branch.  You can see the results of all recent "workflows" at [https://github.com/rainbows-gallery/gallery-app/actions](https://github.com/rainbows-gallery/gallery-app/actions).

## Development History

The development process for Rainbow Gallery conformed to [Issue Driven Project Management](http://courses.ics.hawaii.edu/ics314f19/modules/project-management/) practices. In a nutshell:

* Development consists of a sequence of Milestones.
* Each Milestone is specified as a set of tasks.
* Each task is described using a GitHub Issue, and is assigned to a single developer to complete.
* Tasks should typically consist of work that can be completed in 2-4 days.
* The work for each task is accomplished with a git branch named "issue-XX", where XX is replaced by the issue number.
* When a task is complete, its corresponding issue is closed and its corresponding git branch is merged into master.
* The state (todo, in progress, complete) of each task for a milestone is managed using a GitHub Project Board.


# Deployment
[Link](http://143.198.63.208/)

# Project Management Links 
* [M1](https://github.com/orgs/rainbows-gallery/projects/2/views/2)
* [M2](https://github.com/orgs/rainbows-gallery/projects/3)
* [M3](https://github.com/orgs/rainbows-gallery/projects/4)
 
# Contract Link 
[Link](https://docs.google.com/document/d/1cbQv4htZbSGHQxj_0gbgDfSVIsTfvkACISIYMw3NIY0/edit)

# Team Profiles 
* [Sienne Rodwell](https://sienner.github.io)
* [Tatum Umiamaka](https://tatumumi.github.io)
* [Kobe Uyeda](https://github.com/KobeUyeda)
* [Eric Zhou](https://github.com/eric-z4)

# Link to our Organization
[Link](https://github.com/rainbows-gallery)

# Future Improvements 
* Ability to edit profile photo
* Abilitly to delete your posts
* Admin ability to delete all posts
* Cleaner, more modern design
* Star functionality

