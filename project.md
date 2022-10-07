---
layout: default
title: Project Information
nav_order: 4
---

# Project Information
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Project Options and Requirements 

Your team must choose one of these project options.  You have a great deal of agency within these options, but you must stick to the core use cases of the project. 

You __must__ meet any common and project specific requirements listed below.

## Common Requirements

All projects must do the following, regardless of idea chosen:

* All projects must incorporate Google user accounts as the primary way that someone logs into the system.  You will need to use the Google account API to make this work.  There are several libraries that are built for Django to work with Google accounts with tutorials.  You should not limit logins to just @virginia.edu accounts!  (this will lock out the faculty :-( )
* All users must have an account of some kind where they can store their personal information relevant to the app.
* All users must be able to maintain a list of "friends" in the app, where they can view key information about the other user.  See the project options for details.
* All projects must incorporate the SIS / Class Listing API that we will provide, which will contain (mostly) up-to-date data from SIS that mirrors what you would currently see from Lou's List.
* All projects must be built using the prescribed language (Python 3), framework (Django 4), build environment (GitHub Actions CI), source control management (GitHub), and cloud hosting (Heroku).  No exceptions to these will be granted.
* You __must__ use the PostgreSQL database engine for production on Heroku and continuous integration (on GitHub Actions).  You are allowed to use SQLite for local testing so you do not have to install PostgreSQL on your own maching, but another option is to change your `settings.py` file point to the PostgreSQL DB on Heroku at all times.  

## Project Options

We are doing things a bit differently for Fall 2022.  This semester, we are doing a "greatest hits" of previous project ideas! 

### Project Option 1: New Lou's List
{: .no_toc }
This app will be the Lou's List we all know and love, but your own version.  The primary goal is to allow students to quickly view and search for classes.
- Students must be able to view and search classes, separated into logical categories.
- Students must be able to save a prospective schedule for a given semester.  The system should prevent time conflicts and prevent signing up for multiple sections of the same course.
- Students should be able to "friend" other students to see their schedule and leave a comment on their schedule.

### Project Option 2: Study Buddy
{: .no_toc }
This website would be used to help find study buddies in your classes a one-off "find someone for a specific class on a specific night" (i.e., not consistent study groups).
- Students must be able to list which UVA courses they are in.
- Students should be able to toggle which class they are looking for a study buddy for at any given time (i.e., I'm only looking for help with CS 2150 right now, but not any of my other classes)
- Students must be able to communicate with other students within the website (i.e., just listing email or phone number isn't enough. You can either implement messaging, embed chat rooms, whatever)
- Students must be able to schedule study times with 1 or more other students, and be able to see all upcoming "study sessions"

### Project Option 3: Textbook Exchange
{: .no_toc }
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

_Major Artifact_: [Scrum Master Final Report](https://docs.google.com/document/d/1FrquNE0XdZ8HURgwZlBUE2L1bQgFSVJNTpShobGoJgk/edit?usp=sharing), due at the end of the semester   

__Requirements Manager__ - The Requirements Manager is responsible for keeping up with "what" it is you are building.  This person will spearhead the requirements elicitation process (which takes place in the first couple weeks of the project) as their major activity.  Note that the Requirements Manager doesn't do the whole process - they just lead the effort.  Everyone else has to participate as well!  Then throughout the semester they will update the burndown chart, monitoring the state of the project.

* Reasons to be the Requirements Manager: You are interested in learning how requirements are created; you want to find out what your fellow stduents are excited about with your project; you like updating a spreadsheet; you like knowing "what's coming next" in the project.
* Reasons to not be the Requirements Manager: You have no interest in interacting with other people to find out what they want in a system; your first couple weeks of the semester are super hectic and you don't have the time for the elicitation process.

_Major Artifact_: [Requirements Elicitation Document](https://docs.google.com/document/d/1rEbq_Bs-Og6RWXxXj60z16H9d8pPH5U0p9tU1sJPMQk/edit?usp=sharing)  , due within the first few weeks of the semester    

__Testing Manager__ - The Testing Manager is responsible for ensuring that the system is thoroughly tested, for developing the overall testing plan/philosophy of the team, and spearheading the beta testing effort at the end of the semester.  The Testing Manager's artifact document is the Beta Testing Report, due near the end of the semester. The Testing Manager then also responsible for overseeing the testing of the team philosophy throughout the semester, ensuring unit tests are being written.  Note that the Testing Manager does not write every test case in the system - they just keep up with what everyone else is doing and lend support as needed.

* Reasons to be the Testing Manager: You want to learn more about testing procedures; you love seeing that unit test result bar turn green; you took HCI or something similar and are interested in setting up user testing.
* Reasons not to be the Testing Manager: You don't see the value in writing tests; you can't stand the idea of having to write two documents (even if one is short); you don't want to work with your fellow students in doing in-person testing.

_Major Artifact_: [Beta Testing Report](https://docs.google.com/document/d/1WeYzWvaci_gUgCSTPG1ZJEcyT0mrKCGk99gY1Nk7dMc/edit?usp=sharing), due near the end of the semester    

__DevOps Manager__ - The DevOps Manager is the support tech for the team in a sense.  They are responsbile for the management and support of all the systems we are using in the class, namely GitHub, GitHub Actions, and Heroku.  They should be a person that is relatively comfortable tinkering with computers and settings.  The DevOps Manager does not have to have all the answers, but would be the contact person for going to the staff to get help on any particular issues.

* Reasons to be the DevOps Manager: You are familiar with the tools mentioned already, or you are really interested in learning more about them; you like to tinker with settings to get things working "just right"; you have the patience to help those on your team who might need assistance getting their environments working.
* Reasons not to be the DevOps Manager: You do not feel comfortable helping others with technical issues; you are very unfamiliar with the tools above and would rather just have a "turnkey" solution for doing your work this semester.

_Major Artifact_: [DevOps Report](https://docs.google.com/document/d/1j267fqoF1T5-j_ypzNARd_UxWgZJ1bKknN4lkngIwxo/edit?usp=sharing), due near the end of the semester  

__UX Designer__ - The UX (user experience) Designer is responsible for the overall look-and-feel of the project.  They are responsible coming up with the design of the overall app and managing the styling on all pages (most likely with Bootstrap).  This person would hopefully have the most HTML/CSS/JS experience of the team, but that is not necessarily required.

* Reasons to be the UX Designer: You are familiar with HTML/CSS/JS and/or Bootstrap and you enjoy thinking about how you want people to interact with your application.  You are a person who wants to make sure you turn in a "good looking" app.
* Reasons not to be the UX Designer: You have absolutely no experience with web design and, in fact, you think Geocities pages from the late 90s was the peak of web design.  For some fun examples, see [https://www.cameronsworld.net/](https://www.cameronsworld.net/).

_Major Artifact_: [Usability Assessment](https://docs.google.com/document/d/14Etg_MLCcdhoi5cPVgN0Lt83PAKddsYrjQFmU27exn4/edit?usp=sharing), due near the end of the semester  

## Artifact Document Templates

### Team Documents
{: .no_toc }
[Project Management Spreadsheet](https://docs.google.com/spreadsheets/d/1_bVYwIopHF9e6xaJOeq-w44JzG-eo3sve7luAiylNZc/edit?usp=sharing)    
[Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing)    
[Final Submission Pledge](https://docs.google.com/document/d/1EjrrG_wKoX-rdav_xYNtYJBIjlr10w0UnP_yHcZofMY/edit?usp=sharing)

### Scrum Master
{: .no_toc }
[Scrum Master Final Report](https://docs.google.com/document/d/1FrquNE0XdZ8HURgwZlBUE2L1bQgFSVJNTpShobGoJgk/edit?usp=sharing)

### Requirements Manager
{: .no_toc }
[Requirements Elicitation Document](https://docs.google.com/document/d/1rEbq_Bs-Og6RWXxXj60z16H9d8pPH5U0p9tU1sJPMQk/edit?usp=sharing)    
[Project Management Spreadsheet](https://docs.google.com/spreadsheets/d/1_bVYwIopHF9e6xaJOeq-w44JzG-eo3sve7luAiylNZc/edit?usp=sharing)   

### Testing Manager
{: .no_toc }
[Beta Testing Report](https://docs.google.com/document/d/1WeYzWvaci_gUgCSTPG1ZJEcyT0mrKCGk99gY1Nk7dMc/edit?usp=sharing)

### DevOps Manager
{: .no_toc }
[DevOps Report](https://docs.google.com/document/d/1j267fqoF1T5-j_ypzNARd_UxWgZJ1bKknN4lkngIwxo/edit?usp=sharing)

### UX Designer
{: .no_toc }
[Usability Assessment](https://docs.google.com/document/d/14Etg_MLCcdhoi5cPVgN0Lt83PAKddsYrjQFmU27exn4/edit?usp=sharing)

## Sprint Information

For each sprint check, your team must meet the minimum requirements shown below for each sprint to earn full XP.  Faculty will not override a TA's decision except in extreme circumstances.  

Each sprint is graded out of 25 XP.  In general, the following grading standard applies:

* 25 XP: Excellent progress toward completing the project on time and meeting all requirements.
* 20 XP: Good progress toward completing the project, but at least one requirement looks a bit uncertain.
* 15 XP: Fair progress toward completing the project, but team will need to step up to finish successfully.
* 10 XP: Poor progress toward completing the project and the team definitely needs to refocus.  Some measurable work was accomplished, however.
* 5 XP: Little progress was made toward completing the project during this sprint.
* 0 XP: Project is in danger.

### Sprint 1: Project Organization

__Due:__ September 11 or 12

__Goal:__ Have your initial meeting as a team and determine who will be doing what on the team.  This meeting can be any time between when your team is formed and your first official meeting with your TA on either September 11 or 12.  The Scrum Master of each team MUST complete this form with the team as a part of the Sprint: [Team Declaration Form](https://docs.google.com/forms/d/e/1FAIpQLSdEtNhCrBrrMNgE0O3sb-NXnBmHW_RdHfYz4VDgi5LLySQvEw/viewform?usp=sf_link).  Also, Scrum Masters should initialize the team GitHub repo through GitHub Classroom at [https://classroom.github.com/a/bVrk55Um](https://classroom.github.com/a/bVrk55Um).  Please use your assigned team number for the identifier when prompted (e.g. A-03).  Other team members can then go to that link and accept the assignment, selecting the proper team.

__Requirements:__  Complete the Team Declaration form above ASAP.  Initialize your GitHub repo and have all team members join.

__TEAM EVALS:__ No Team Evals this week.

__How To Submit:__ Scrum Masters should fill out a [Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing) and submit it to Gradescope BEFORE meeting with your TA so they can reference it.  Scrum Masters *must* select their team members in Gradescope when submitting so all members will earn the XP for the sprint.  (No, you won't have much to report this week, but think about what's coming up and discuss that.)

### Sprint 2: Requirements Elicitation

__Due:__ September 25 or 26

__Goal:__ Spend most of this sprint working as a team to elicit the full requirements for your system.  Note that while the final Requirements Document is the responsibility of the Requirements Manager, ALL TEAM MEMBERS are expected to contribute to gathering and refining the final set of requirements.  Some coding can be performed if desired, such as some design work or starting on Google Account integration.  For the project code itself, create a base Django project, put the code in GitHub, and have it hosted on Heroku.  Basically, you're taking the lessons you learned from the setup of the Django Practice Assessment and putting it to use here to show that you have a working foundation to build off of.

__Requirements:__ The team must have a working basic Django app hosted on Heroku.  The team can also show and discuss the progress and initial results of their requirements elicitation activity.  The team _does not_ need to have a finalized requirements document at this point, but must be able to show that they have started the elicitation process and have at least some data.  The Requirements Manager will receive a separate score for the actual document.  Also, teams should be able to discuss ideas for the design of their application.

* [Example Requirements Document from Spring 2020](https://docs.google.com/document/d/1l39MWsVEX8LWcQ16Wo5-PXyaKhfm_O6j-1Uj6wj8RUU/edit?usp=sharing)
* ["Excellent" Example from Fall 2020](https://docs.google.com/document/d/1aqeWWhA1QztrM_6iAI1PF3FjP8VTvOqCXhe5w9D9GaU/edit?usp=sharing)
* ["Great" Example from Fall 2020](https://docs.google.com/document/d/12a8MTkqiUZbnDIs-xRfmCQUb8ozs3jHamdcwp6fuqSc/edit?usp=sharing)
* ["Good" Example from Fall 2020](https://docs.google.com/document/d/1RxUBAEFjk0HpQ1aFOOX830nenFBX_Idao3vRVBYop1A/edit?usp=sharing)

__TEAM EVALS:__ At the end of Sprints 2-6 and at the end of the semester, you will need to fill out an evaluation for _each member_ of your team! You can find the evaluation form her: [CS 3240 - F22 - Student Team Sprint Evaluations](https://docs.google.com/forms/d/e/1FAIpQLScHXBZy1i5eAWs7w_2GCmM_vX3VCm8Lgq3Lm0hXyGrnB2uchg/viewform?usp=sf_link)

__How To Submit:__ Scrum Masters should fill out a [Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing) and submit it to Gradescope BEFORE meeting with your TA so they can reference it.  Scrum Masters *must* select their team members in Gradescope when submitting so all members will earn the XP for the sprint.  The main branch of your GitHub repo should be live on Heroku.

### Sprint 3: Login Integration

__Due:__ October 9 and 10

__Goal:__ All projects must have a user account feature for students to login with.  To accomplish this, you are to integrate Google login to your app.

__Requirements:__ A user with a Google Account (not just a Netbadge account!) can login to the system and the system shows in some way that that user has indeed logged in.  You cannot lock your app to just @virginia.edu accounts (otherwise the professors can't login...).  GitHub Actions CI MUST be operational with at least one test case in order to earn full XP.  As you are just getting started with testing, this is more showing us that you have the process setup and that you have some passing tests.  You do not have to have login fully tested at this point.

__TEAM EVALS:__ At the end of Sprints 2-6 and at the end of the semester, you will need to fill out an evaluation for _each member_ of your team! You can find the evaluation form her: [CS 3240 - F22 - Student Team Sprint Evaluations](https://docs.google.com/forms/d/e/1FAIpQLScHXBZy1i5eAWs7w_2GCmM_vX3VCm8Lgq3Lm0hXyGrnB2uchg/viewform?usp=sf_link)

__How To Submit:__ Scrum Masters should fill out a [Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing) and submit it to Gradescope BEFORE meeting with your TA so they can reference it.  Scrum Masters *must* select their team members in Gradescope when submitting so all members will earn the XP for the sprint.  The main branch of your GitHub repo should be live on Heroku.

### Sprint 4: First Major Feature w/ SIS API

__Due:__ October 23 or 24

__Goal:__ All projects must make use of our SIS API for reading information about classes.  For this sprint, create the infrastructure for doing this, showing that you can read information and display it to the screen in a meaningful way in the context of your app (i.e. not just dumping it on the screen). 

__Requirements:__ In the opinion of the TA, significant work was accomplished this week utilizing the SIS API, such that it is visible and mostly usable in the system.  GitHub Actions CI MUST be operational with at multiple test cases in order to earn full XP.  You should be moving more toward having a robust test suite at this point.

__TEAM EVALS:__ At the end of Sprints 2-6 and at the end of the semester, you will need to fill out an evaluation for _each member_ of your team! You can find the evaluation form her: [CS 3240 - F22 - Student Team Sprint Evaluations](https://docs.google.com/forms/d/e/1FAIpQLScHXBZy1i5eAWs7w_2GCmM_vX3VCm8Lgq3Lm0hXyGrnB2uchg/viewform?usp=sf_link)

__How To Submit:__ Scrum Masters should fill out a [Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing) and submit it to Gradescope BEFORE meeting with your TA so they can reference it.  Scrum Masters *must* select their team members in Gradescope when submitting so all members will earn the XP for the sprint.  The main branch of your GitHub repo should be live on Heroku.

### Sprint 5: Next Major Feature

__Due:__ November 6 or November 7

__Goal:__ Move forward with the next major features of your application, showing that you are making significant progress.  Your app should be "functional" at this point, such that a user can login and use some of the basic features.

__Requirements:__ In the opinion of the TA, significant work was accomplished this week other major features of the application, such that it is visible and mostly usable in the system.  GitHub Actions should still be working.

__TEAM EVALS:__ At the end of Sprints 2-6 and at the end of the semester, you will need to fill out an evaluation for _each member_ of your team! You can find the evaluation form her: [CS 3240 - F22 - Student Team Sprint Evaluations](https://docs.google.com/forms/d/e/1FAIpQLScHXBZy1i5eAWs7w_2GCmM_vX3VCm8Lgq3Lm0hXyGrnB2uchg/viewform?usp=sf_link)

__How To Submit:__ Scrum Masters should fill out a [Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing) and submit it to Gradescope BEFORE meeting with your TA so they can reference it.  Scrum Masters *must* select their team members in Gradescope when submitting so all members will earn the XP for the sprint.  The main branch of your GitHub repo should be live on Heroku.

### Sprint 6: Beta Version

__Due:__ November 13 or 14

__Goal:__ After Sprint 6 is complete, you are going to have other students test your system.  So you need a working system with most all of your functionality ready to go.  The app may not be fully polished and still needs a bit of work, but it needs to be usable from beginning to end.

__Requirments and Full Beta Version:__ In the opinion of the TA, you have an app that is ready for other students to test out (e.g. it doesn't crash, it looks reasonably good, it has most features, etc.).  You will earn 25 XP for the sprint check plus 100 XP as the first half of your overall project score of 250 XP (basically, if you have a working app at this point, we know your final project grade will be at least 100/250 XP, so we can give you those points now).

__TEAM EVALS:__ At the end of Sprints 2-6 and at the end of the semester, you will need to fill out an evaluation for _each member_ of your team! You can find the evaluation form her: [CS 3240 - F22 - Student Team Sprint Evaluations](https://docs.google.com/forms/d/e/1FAIpQLScHXBZy1i5eAWs7w_2GCmM_vX3VCm8Lgq3Lm0hXyGrnB2uchg/viewform?usp=sf_link)

__How To Submit:__ Scrum Masters should fill out a [Sprint Report](https://docs.google.com/document/d/1kS3_apbNgVBV3OoWcyJLbU66r8Hcl45fF-PHEqKH0as/edit?usp=sharing) and submit it to Gradescope BEFORE meeting with your TA so they can reference it.  Scrum Masters *must* select their team members in Gradescope when submitting so all members will earn the XP for the sprint.  The main branch of your GitHub repo should be live on Heroku.

## Final Grading Information

The final project is worth a total of 250 XP.  (100 XP will be awarded after Sprint 6 for your Beta version and the remaining 150 XP will be awarded by the professors after final demos.)  Like the other assessments in this course, grading is overall wholistic - that is, there is no specific point-for-point breakdown for the rubric.  One reason for this is that this is simply not how software is delivered in real-life.  There are basically only four outcomes:

* You meet the expectations of the customer within reason and both parties are satisfied with the outcome;
* You exceed the expectations of the customer, potentially generating more good will, a good reference, or more future business;
* You do not quite meet the expectations of the customer, leaving some room for improvement;
* You ship a system that simply does not work to the expectations of the customer.

We will grade your projects in a similar vein, with some flexibility for minor adjustments.

Thus, the grading levels will be:

* Above and Beyond - Min XP: 250 / Max XP: 255
* Complete - Min XP: 200 / Max XP: 250
* Lacking - Min XP: 150 / Max XP: 200
* Insufficient - Min XP: 0 / Max XP: 150

Aspects that will determine the exact grade within a range include but are not limited to:

* UI design
* Overall flow of application
* Special features
* Obvious bugs that should have been corrected
* Polish

__TEAM EVALS:__ All team members will complete a final, overall team evaluation at the end of the course.

__The final version of the project must be in GitHub and hosted on Heroku no later than 11:59 PM EST on Tuesday, December 6!__