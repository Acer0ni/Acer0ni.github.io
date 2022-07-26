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

## Addy

![addy-help](/project-pictures/addy-help.png)

I started this project as a way to break out of the rut I found myself in during the planning phase for a much larger app. With no concrete intentions other than exploring a few different APIs and building something cool, I started writing, researching, experimenting, and now I’m extremely happy to present the result of this endeavour: Addy the Discord Bot.

During my exploration with Addy there have been many hurdles and many lessons learned.

Here are some of the things I have learned from the journey so far:

- How to handle third party APIs with less than stellar documentation and design

- How to save data without making a database

- The python requests library, and how to handle it's response object

- Explored Python's dictionary and it's functions

Addy doesn’t have a central theme as she really was meant to be a personal project, thus each of her commands came about simply from asking myself “Wouldn’t it be cool if…?” Here are some of the things she can do now:

- Look up a player in Runescape3

- Create and add to a watch2gether room for you and your friends

- Offer a word of encouragement or tell you a quote from Brooklyn 99

Of course every new feature sparks ideas for other improvements and the list keeps growing, but here are the additions I would like to make in the near future:

- A backend to complement her, and allow to me save data more reliably.

- A way for her to play music in a voice channel (worried about the legality here).

- A Runescape item price look-up. (Their api is really bad, the easiest way to do this is to build a webcrawler and crawl their api once a week)

- If you have a cool idea for Addy, contact me and let me know!

If you are interested in seeing Addy in action, I have set up a [discord server](https://discord.gg/a5EXHbGwzH) for you to try. The browser version of discord doesn't require you to log in. Jump right in and type !help to see all of her commands. a more in depth explanation can be found [here.](https://github.com/Acer0ni/Addy-the-disc-bot/blob/main/README.md)

[Github repo](https://github.com/Acer0ni/Addy-the-disc-bot)

## Alien Invasion

![Imgur](https://i.imgur.com/o4OH62y.png)

Ever since I was little I have been fascinated by video games and everything about them. As I have been learning to code, naturally I have been very interested in how video games are made but with no experience building video games and less than a year of experience writing code, it seemed like a tall order. But I was still curious and ended up following a tutorial to build a Space Invaders inspired game from a tutorial I found in [Python crash course](https://nostarch.com/pythoncrashcourse2e) by Eric Matthes.

Additionally I built a high scores server and created a login and sign-up system for users. For more information, check out the [blog post](/posts/2022/alien_invasion/).

[Alien invasion repo](https://github.com/Acer0ni/alien-invasion)

[Backend repo](https://github.com/Acer0ni/alien-invasion-api)

## Budget Book

![BB-pic](/project-pictures/bb-pic.png)

Budgetbook is a minimalist budget tracking app. The user starts by inputting their monthly income, then adds expenses with dollar values which are automatically subtracted from the monthly total. Expenses can be edited and deleted, with the user’s remaining monthly balance updating automatically to match.

Budget book was our first time working with other developers on a major project. We set off to make a full Stack budgeting application that took in your monthly income and expenses, and told you how much remaining and let you set goals to work for i.e vacations.

I worked mostly on the back end for this project but did help on some of the front end logic with the api calls. the back end turned out pretty much how I expected it to after several iteration.

It seemed like everything was going alright early on, we had spent a bunch of time planning the front end thinking the back end would be self explanatory... it was not. We ran into issues immediately with the back end not returning things the front end devs thought they would, we fixed this by working very closely the rest of the week and over communicating.

This project really taught me the importance of having a solid design in both your front and back end and really to be clear in your api documentation.

[Github repo backend](https://github.com/Team-formerly-known-as/budget-book-backend)

[Github repo Frontend](https://github.com/Team-formerly-known-as/budget-book-frontend)

[Live site](https://team-formerly-known-as.github.io/budget-book-frontend/)
