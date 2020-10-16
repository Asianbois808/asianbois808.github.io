# Table of Contents

* [Overview](#overview)
* [Milestones](#milestones)
* [User Guide](#user-guide)
* [Developer Guide](#developer-guide)

# Overview

This application is a reimplementation of <a href="https://bowfolios.github.io/">BowFolios</a> using React Native to support mobile users. Users are able to view and modify profiles, projects, and interests, which can be useful for organizing achievements and connecting with others who share similar interests.

# Milestones

## <a href="https://github.com/Asianbois808/Assignment-1/milestone/1">Milestone 1</a>

## <a href="https://github.com/Asianbois808/Assignment-1/milestone/2">Milestone 2</a>

## <a href="https://github.com/Asianbois808/Assignment-1/milestone/3">Milestone 3</a>

We will try our best to ensure that the app is completely functional and no errors are present. 

# User Guide

## Landing Page

The landing page will allow the user to sign in, sign up, or access one of the other pages by opening the menu on the top left.

<img src="/pics/landing.png" width="35%" height="35%">

## Your Profile Page

The profile page is only shown to users that are logged in and allow them to update their profile.

<img src="/pics/your-profile.png" width="35%" height="35%">

## Menu Bar

The menu bar is where the user will find all the different pages that can be accessed within BowFolios.

<img src="/pics/menu.png" width="35%" height="35%">

## Sign In Page

Returning users with a previously registered account will be able to sign.

<img src="/pics/sign-in.png" width="35%" height="35%">

## Sign Up Page

New users can create an account.

<img src="/pics/sign-up.png" width="35%" height="35%">

## Profiles Page

Lists all registered profiles along with associated interests/projects.

<img src="/pics/profiles.png" width="35%" height="35%">

Shows an example Profile card.

<img src="/pics/profiles-card.png" width="35%" height="35%">

## Projects Page

Shows existing projects and associated profiles.

<img src="/pics/projects.png" width="35%" height="35%">

Shows an example Project card.

<img src="/pics/projects-card.png" width="35%" height="35%">

## Interests Page

Able to view interests and associated profiles.

<img src="/pics/interests.png" width="35%" height="35%">

Shows an example Interest card.

<img src="/pics/interests-card.png" width="35%" height="35%">

## Add Project Page

Registered users can create new projects.

<img src="/pics/add-project.png" width="35%" height="35%">

## Filter Page

Select interests to filter and view specific users.

<img src="/pics/filter.png" width="35%" height="35%">

## Authentication and Database Model

### Firebase Auth

For the authentication, we used Firebase's Auth API which handles the user information behind the scenes. Because of it, we no longer have to worry about using a database to store emails and passwords—Firebase Auth takes care of it.

### Firebase Firestore

When making the database, one of the problems (and it was addressed in the bowfolios site) we encountered was to make the Profiles, Projects, and Interests primary collections
relate to each other. Since the database that we used is Firebase's Firestore is NoSQL, we had to create three secondary collections namely ProfilesProjects, ProfilesInterests, and ProjectsInterests to simulate a join() relationship between the three primary collections. Each of the secondary collections would contain documents that has the unique identifier of the primary collections it's trying to join. For instance, the unique identifier for the Profiles collection is the email, while for the Projects collection, it would be the project name. Therefore, the secondary collection ProfilesProject would have documents that have email and project name fields.

# Developer Guide

1. To begin, install React Native and Android Emulator (guide can be found <a href="https://www.youtube.com/watch?v=Hf4MJH0jDb4">here</a>).

1. Now, retrieve the Bowfolios source code from our GitHub repository <a href="https://github.com/Asianbois808/Assignment-1">here</a>.

2. Clone the repository to GitHub Desktop.

3. Right click the repository and click "Open with Command Prompt"

4. Once in the cmd, type `cd bowfolios` to change directory to the app folder.

5. In the app folder, type `npm install` to install the needed plugins to run the app.

6. Next, type `npx react-native run-android` to run the program.


