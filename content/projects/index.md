+++
title = "Projects"
date = "2022-01-07T12:28:01-08:00"
author = "Larry Flint"
authorTwitter = "0xaceroni" #do not include @
cover = ""
tags = [""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = true
draft = false
+++
## Forum api
![db-icon](/project-pictures/db-picture.png)This is a database for a user-generated chat forum that is ready to be paired with a front-end UI. It uses the Django-Ninja framework, Postgres, and cookie based authentication. Intended for use as a technology forum, but is suitable for multiple industries.

This project started off as a full stack app, intending to be my capstone project for my bootcamp. It was meant to be a technology forum for me and my cohorts to compile our resources. We had five days to complete this project.

Not knowing anything about Django-Ninja coming in, or anything about cookie based authentication, I spent more time studying than coding, and did not finish the front end. However, I did end up with a fully functional secure api with cookie based authentication.

One immediate challenge was the lack of Django-Ninja docs written on a beginner level. So there was a lot of struggle trying to fit django-ninja into what i already knew about DRF.

I had a lot of fun with Django-Ninjas auto-docs. They made testing very easy. My most valuable lesson from this project came in the form of setting realistic expectations when incorporating a new technology into a build. Django-Ninja did make the process much quicker once I had done enough research to fully understand it, however I underestimated the amount of time it took to get to that point which caused a delay in finishing the project.


[Github repo](https://github.com/Acer0ni/coding-forum)

[Live site](https://forum.pwnschool.org/api/docs)

## Budget Book

![BB-pic](/project-pictures/bb-pic.png)

Budgetbook is a minimalist budget tracking app. The user starts by inputting their monthly income, then adds expenses with dollar values which are automatically subtracted from the monthly total. Expenses can be edited and deleted, with the user’s remaining monthly balance updating automatically to match.

Budget book was our first time working with other developers on a major project. We set off to make a full Stack budgeting application that took in your monthly income and expenses, and told you how much remaining and let you set goals to work for i.e vacations.

I worked mostly on the back end for this project but did help on some of the front end logic with the api calls. the back end turned out pretty much how I expected it to after several iteration.

It seemed like everything was going alright early on, we had spent a bunch of time planning the front end thinking the back end would be self explanatory... it was not.  We ran into issues immediately with the back end not returning things the front end devs thought they would, we fixed this by working very closely the rest of the week and over communicating.

This project really taught me the importance of having a solid design in both your front and back end and really to be clear in your api documentation.

[Github repo backend](https://github.com/Team-formerly-known-as/budget-book-backend)

[Github repo Frontend](https://github.com/Team-formerly-known-as/budget-book-frontend)

[live site](https://team-formerly-known-as.github.io/budget-book-frontend/)

## Wait and See

![waitnsee](/project-pictures/waitnsee.png)

The goal of this project was to create a classic “idle” game where the player’s gold level increases at a set rate, and can be used to purchase periodic upgrades for a character. 

This was one of my first React projects and it was a tremendous learning experience. There were a multitude of features that I had planned on including, but it became apparent very quickly that I had misjudged the time it would take to implement everything. 

I was able to build a functioning game that has multiple character attributes that can be “trained” to level up, and creates a custom avatar based off of the player’s chosen username. The gold system works as planned, increasing at a steady rate. 

The major blocker here was bug-fixing the gold increment system. It was very difficult to get the gold amount to increase at a set rate, and this took up a lot of development time, leading to multiple features being dropped. Features that I plan on implementing in a future update include a Shop and Equipment page, rudimentary turn-based combat, and a fully functioning database to store each player’s unique character statistics.

[Github repo](https://github.com/Acer0ni/idle-game)

[live site](https://aceroni.com/idle-game)
