---
layout: default
title: Project Information
nav_order: 4
---

# Project Information
{: .no_toc }

## Project Options and Requirements 

Your team must choose one of these project options.  You have a great deal of agency within these options, but you must stick to the core use cases of the project. 

You __must__ meet any common and project specific requirements listed below.

## Common Requirements

All projects must do the following, regardless of idea chosen:

* All projects must incorporate Google user accounts as the primary way that someone logs into the system.  You will need to use the Google account API to make this work.  There are several libraries that are built for Django to work with Google accounts with tutorials.  You should not limit logins to just @virginia.edu accounts!  (this will lock out the faculty :-( )
* All users must have an account of some kind where they can store their personal information relevant to the app.
* All users must be able to maintain a list of "friends" in the app, where they can view key information about the other user.  See the project options for details.
* All projects must incorporate the SIS / Class Listing API that we will provide, which will contain (mostly) up-to-date data from SIS that mirrors what you would currently see from Lou's List.
* All projects must be built using the prescribed language (Python 3), framework (Django 4), build environment (GitHub Actions CI), source control management (GitHub), and cloud hosting (TBD).  No exceptions to these will be granted.
* You __must__ use the database engine for production on the cloud hosting and continuous integration (on GitHub Actions).  You are allowed to use SQLite for local testing so you do not have to install Postgres on your own maching, but another option is to change your `settings.py` file point to the Postgres DB on Heroku at all times.  

## Project Options

We are doing things a bit differently for Fall 2022.  This semester, we are doing a "greatest hits" of previous project ideas! 

### Project Option 1: New Lou's List
This app will be the Lou's List we all know and love, but your own version.  The primary goal is to allow students to quickly view and search for classes.
- Students must be able to view and search classes, separated into logical categories.
- Students must be able to save a prospective schedule for a given semester.  The system should prevent time conflicts and prevent signing up for multiple sections of the same course.
- Students should be able to "friend" other students to see their schedule and leave a comment on their schedule.

### Project Option 2: Study Buddy
This website would be used to help find study buddies in your classes a one-off "find someone for a specific class on a specific night" (i.e., not consistent study groups).
- Students must be able to list which UVA courses they are in.
- Students should be able to toggle which class they are looking for a study buddy for at any given time (i.e., I'm only looking for help with CS 2150 right now, but not any of my other classes)
- Students must be able to communicate with other students within the website (i.e., just listing email or phone number isn't enough. You can either implement messaging, embed chat rooms, whatever)
- Students must be able to schedule study times with 1 or more other students, and be able to see all upcoming "study sessions"

### Project Option 3: Textbook Exchange
Instead of selling your books back to the bookstore, post them here and try to either trade them or sell them to someone else!
- Students must be able to list their books available along with the course/instructor based upon the SIS / Class Listing API.
- Students must be able to search by book title, ISBN, course, or instructor.
- Students must be able to "favorite" books they find that they may be interested in.  The favorites list should be associated with the student's account.
- Students must be able to message / propose a trade / propose a sale with another student who has posted a textbook.

## Team Roles

Each member of your five person team will take on one of these roles.  Each role has different responsibilities, but ALL ROLES require that you be an active contributor to the code of the project.  In other words, if you take on Scrum Master, that doesn't mean you don't have to contribute as much code as someone else.

__Scrum Master__ - The Scrum Master could also be called the Team Leader, but it's not really a "leader" position, per se, in that they are not making major decisions about the project itself.  The Scrum Master is responsbile for keeping everyone on track, facilitating all team meetings, and monitoring team status / issues.  The course staff will come to the Scrum Master first if there are any team issues or questions, and similarly the Scrum Master needs to know what's going on with the team and can communicate with the staff if someone is falling behind, etc.

* Reasons to be the Scrum Master: You like keeping schedules; you like keeping things organized; you don't mind being the point of contact with the staff.
* Reasons not to be the Scrum Master: You are not the most organized person; you don't think you can stay on top of what the team is working on; you don't like talking to the staff.

_Major Artifact_: Scrum Master Final Report, due at the end of the semester   

__Requirements Manager__ - The Requirements Manager is responsible for keeping up with "what" it is you are building.  This person will spearhead the requirements elicitation process (which takes place in the first couple weeks of the project) as their major activity.  Note that the Requirements Manager doesn't do the whole process - they just lead the effort.  Everyone else has to participate as well!  Then throughout the semester they will update the burndown chart, monitoring the state of the project.

* Reasons to be the Requirements Manager: You are interested in learning how requirements are created; you want to find out what your fellow stduents are excited about with your project; you like updating a spreadsheet; you like knowing "what's coming next" in the project.
* Reasons to not be the Requirements Manager: You have no interest in interacting with other people to find out what they want in a system; your first couple weeks of the semester are super hectic and you don't have the time for the elicitation process.

_Major Artifact_: Requirements Elicitation Document, due within the first few weeks of the semester    

__Testing Manager__ - The Testing Manager is responsible for ensuring that the system is thoroughly tested, for developing the overall testing plan/philosophy of the team, and spearheading the beta testing effort at the end of the semester.  The Testing Manager has two documents to create: the Test Plan and Beta Testing Document.  The Test Plan is a short, two-page document that outlines what the testing philosophy of the team will be (i.e. every file must have X test cases, every person must write X tests, etc.).  The Testing Manager then is responsible for overseeing that philosophy throughout the semester, ensuring unit tests are being written.  Note that the Testing Manager does not write every test case in the system - they just keep up with what everyone else is doing and lend support as needed.

* Reasons to be the Testing Manager: You want to learn more about testing procedures; you love seeing that unit test result bar turn green; you took HCI or something similar and are interested in setting up user testing.
* Reasons not to be the Testing Manager: You don't see the value in writing tests; you can't stand the idea of having to write two documents (even if one is short); you don't want to work with your fellow students in doing in-person testing.

_Major Artifact_: Beta Testing Report, due near the end of the semester    

__DevOps Manager__ - The DevOps Manager is the support tech for the team in a sense.  They are responsbile for the management and support of all the systems we are using in the class, namely GitHub, GitHub Actions, and Heroku.  They should be a person that is relatively comfortable tinkering with computers and settings.  The DevOps Manager does not have to have all the answers, but would be the contact person for going to the staff to get help on any particular issues.

* Reasons to be the DevOps Manager: You are familiar with the tools mentioned already, or you are really interested in learning more about them; you like to tinker with settings to get things working "just right"; you have the patience to help those on your team who might need assistance getting their environments working.
* Reasons not to be the DevOps Manager: You do not feel comfortable helping others with technical issues; you are very unfamiliar with the tools above and would rather just have a "turnkey" solution for doing your work this semester.

_Major Artifact_: DevOps Report, due near the end of the semester  

__UX Designer__ - The UX (user experience) Designer is responsible for the overall look-and-feel of the project.  They are responsible coming up with the design of the overall app and managing the styling on all pages (most likely with Bootstrap).  This person would hopefully have the most HTML/CSS/JS experience of the team, but that is not necessarily required.

* Reasons to be the UX Designer: You are familiar with HTML/CSS/JS and/or Bootstrap and you enjoy thinking about how you want people to interact with your application.  You are a person who wants to make sure you turn in a "good looking" app.
* Reasons not to be the UX Designer: You have absolutely no experience with web design and, in fact, you think Geocities pages from the late 90s was the peak of web design.  For some fun examples, see [https://www.cameronsworld.net/](https://www.cameronsworld.net/).

_Major Artifact_: Usability Assessment, due near the end of the semester  

## Artifact Document Templates

Coming Soon!

## Sprint Information

For each sprint check, your team must meet the minimum requirements shown below for each sprint to earn full XP.  Faculty will not override a TA's decision except in extreme circumstances.  

Each sprint is graded out of 25 XP.  In general, the following grading standard applies:

* 25 XP: Excellent progress toward completing the project on time and meeting all requirements.
* 20 XP: Good progress toward completing the project, but at least one requirement looks a bit uncertain.
* 15 XP: Fair progress toward completing the project, but team will need to step up to finish successfully.
* 10 XP: Poor progress toward completing the project and the team definitely needs to refocus.  Some measurable work was accomplished, however.
* 5 XP: Little progress was made toward completing the project during this sprint.
* 0 XP: Project is in danger.