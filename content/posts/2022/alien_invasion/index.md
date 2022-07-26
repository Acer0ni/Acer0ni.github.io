+++
title = "Alien invasion"
date = "2022-07-07T12:35:47-07:00"
author = "Larry Flint"
authorTwitter = "0xaceroni" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = true
draft=true
+++

![Imgur](https://i.imgur.com/7L395bz.png)

Ever since I was little I have been fascinated by video games and everything about them. As I have been learning to code, naturally I have been very interested in how video games are made but with no experience building video games and less than a year of experience writing code, it seemed like a tall order. But I was still curious and ended up following a tutorial to build a Space Invaders inspired game from a tutorial I found in [Python crash course](https://nostarch.com/pythoncrashcourse2e) by Eric Matthes.

The idea started to form as the tutorial walked me through setting up high scores for the game. Still, a problem that bugged me immediately was that there was no persistence there so as soon as I exited the app the high scores were gone forever and I would never be able to brag to my friends about my sweet new score. After the tutorial was finished I went back and refactored it to save the high scores locally but that still seemed hollow to me in today's connected world. After a little research on how bigger games handle this problem, I learned that my plan wouldn't be perfect – anyone with an account could make an API call directly to the server and have an impossibly high score. Real online games handle this a lot of the time by keeping state server side to make sure there is nothing fishy going on. This would require a full refactor and be outside of the score for this project. With a notepad full of ideas and notes, I started writing a server that takes care of authentication and keeps track of the high scores. With plenty of ideas for the future, such as seasonal high scores, a personal top ten, and some sweet power-up for your ship in the game, I decided to focus on getting this first idea shipped

I began designing the server component for it, that being the part that I had done before. I used Django to keep track of the users and cookie-based authentication which did the brunt of the work for me. I ended up only needing four routes to make this happen: signup, a login, a submit score, and a get score to make this game run but ended up adding a get users and get all scores for testing purposes and it seemed like they would be helpful to have in the future

Once the server was done, it was time to hook the game up to it, and honestly, I was at a loss. I knew exactly as much of Pygame as the tutorial had taught me, which unfortunately for me was not the same knowledge I needed to do what I wanted to do. Improvements like adding multiple screens to the game, having error boxes pop up, and making requests to an API were all beyond the scope of the tutorial and just beyond my knowledge level. I spent a few days thinking about the overall design of the game and how I could slip a login screen into it without refactoring the whole thing. Once I felt I had a clear path I jumped in and started coding. I knew I needed to make a screen with text boxes for username and password and buttons to navigate through the different screens, a similar screen to register an account, and a few well-placed requests. At the end of the project, it ended up pretty much how I had planned in the beginning.

![Imgur](https://i.imgur.com/bKzbbmR.png)

![Imgur](https://i.imgur.com/o4OH62y.png)

## Deployment

While the coding of the project went well the deployment was rocky, because the server was going to be hosted remotely I decided that dockerizing it would be the best path. Docker is a great tool that I have used once before and was happy to get some more experience with so that part was pretty straightforward. Pairing it with Nginx so that it could talk to the container took me a while and I needed a fair bit of help to get it done. The deployment process looks roughly like this.

- pull the project from the repo on the server
- build the docker container
- set up Postgres
- run the docker container
- set up Nginx
- ???
- profit

Editor’s Note: The challenges with Nginx were primarily deploying the application in a container but running Nginx on the host as a reverse proxy for multiple applications.

## Distribution

I thought distributing the game would be easy. Until I started writing the readme for the repo and as I write my technical docs as if I was explaining them to my grandma I knew I was losing a lot of potential users if my install instructions included the command line. I looked around and found [Pyinstaller](https://pyinstaller.org/en/stable/) and learned how to use that. After two days of making sure I have the right python version installed and studying which flags to use to get a single executable (including the fact that even if Pyinstaller said that my game was one file I still had to make sure to package my assets into the root directory) I finally had it. Executables for both Mac and windows, which I had to build on their respective machines. I moved the binary to my wife's computer and tried to run it… only to be met with a windows defender alert. So I ran it through [virus total](https://www.virustotal.com/gui/file/42bddc5b361faa09bc1b346dc8c83d752e3041cb4b3da3d1a9bb010bac4094d3?nocache=1) and found that 6 security vendors flagged it as malware. It turns out a package that pyinstaller uses was flagged as [malware](https://github.com/pyinstaller/pyinstaller/issues/6754). It seems this is a known problem and I am not the first person to encounter it. I decided that I had sunk enough time into this part of the project and decided to try to build binaries in a later version.

## Conclusion

Looking back, this project gave me more experience building an API with authentication and gave me a reason to use Docker and Nginx again. I feel I need a lot more experience with the deployment side of development, so it was valuable to practice it here. But I think I would not do a project like this by myself again. I found myself spending too much time doing things that I didn't enjoy, like lining everything up, and not enough time doing what I did enjoy, building functional features.

[Github Repo](https://github.com/Acer0ni/alien-invasion)
