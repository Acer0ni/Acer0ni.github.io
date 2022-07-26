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

Ever since I was little I have been fascinated by video games and everything about them. As I have been learning to code, naturally I have been very interested in how video games are made but with no experience building video games and less than a year of experience writing code, it seemed like a tall order. But I was still curious and ended up following a tutorial to build a Space Invaders inspired game from a tutorial I found in [Python crash course](https://nostarch.com/pythoncrashcourse2e) by Eric Matthes.

the idea started to form as the tutorial walked me through setting up high scores for the game. Still, a problem that bugged me immediately was that there was no persistence there so as soon as I exited the app the high scores were gone forever and I would never be able to brag to my friends about my sweet new score. after the tutorial was finished I went back and refactored it to save the high scores locally but that still seemed hollow to me in today's connected world. After a little research on how bigger games handle this problem, my plan wouldn't be perfect, anyone with an account could make an API call directly to the server and have an impossibly high score. Real online games handle this a lot of the time by keeping state server side to make sure there is nothing fishy going on. This would require a full refactor and be outside of the score for this project. With a notepad full of ideas and notes I started writing a server that takes care of authorization and keeps track of the high scores with plenty of ideas for the future like seasonal high scores, a personal top ten, and some sweet power-up for your ship in the game.

Once I decided to focus on the high score feature I began designing the server component for it, that being the part that I had done before, and honestly not too much to say about it. I used Django to keep track of the users and cookie-based authentication which did the brunt of the work for me. I ended up only needing four routes to make this happen, signup, a login, a submit score, and a get score to make this game run but ended up adding a get users and get all scores for testing purposes and it seemed like they would be helpful to have in the future

Once the server was done, it was time to hook the game up to it, and honestly, I was at a loss. I knew exactly as much of Pygame as the tutorial had taught me, which unfortunately for me was not the same knowledge I needed to do what I wanted to do like adding multiple screens to the game, having error boxes pop up, and making requests to an API. I spent a few days thinking about the overall design of the game and how I could slip a login screen into it without refactoring the whole thing. Once I felt I had a clear path I jumped in and started coding. at the end of the project, it ended up pretty much how I had planned in the beginning.

## Deployment

While the coding of the project went well the deployment was rocky, because the server was going to be hosted remotely I decided that dockerizing it would be the best path. Docker is a great tool that I have used once before and was happy to get some more experience with so that part was pretty straightforward. Pairing it with Nginx so that it could talk to the container took me a while and I needed a fair bit of help to get it done. The deployment process looks like this.

- pull the project from the repo on the server
- ????
- profit
- set up Nginx
- build and run the container
- probably be wrong and had to rewrite this

Editor’s Note: The challenges with Nginx were primarily deploying the application in a container but running Nginx on the host as a reverse proxy for multiple applications.

## Distribution

I thought deploying the game would be easy. Until I started writing the readme for the repo and as I write my technical docs as if I was explaining them to my grandma I knew I was losing a lot of potential users if my install instructions included the command line. I looked around and found Pyisntaller and learned how to use that. After two days of making sure I have the right python version installed and studying which flags to use to get a single executable(including the fact that even if Pyinstaller said that my game was one file I still had to make sure to package my assets into the root directory) I finally had it. an executable for Mac and windows, which I had to make on their respective machines, or I thought I did. I moved the binary to my wife's computer and tried to run it. only to be met with a windows defender alert. So I ran it through [virus total](https://www.virustotal.com/gui/file/42bddc5b361faa09bc1b346dc8c83d752e3041cb4b3da3d1a9bb010bac4094d3?nocache=1) and found that 6 security vendors flagged it as malware as it turned out a packager that pyinstaller uses were flagged as malware. it seems this is a known problem and I am not the first person to encounter it. I decided that I had sunk enough time into this part of the project and decided to try to binary in a later version

[Github Repo](https://github.com/Acer0ni/alien-invasion)
